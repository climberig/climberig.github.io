---
title:  Delete Git Branches In One Command
permalink: git-branch-delete-all
---
<p class="meta">19 November 2014 - Berkeley</p>

If you use git as your source control, your workflow is probably similar to the following:

1. Create a local branch to develop a new feature
2. Write some code, push the changes to the new branch, repeat
3. Merge your branch to master
4. Start working on a new feature thus repeating all the steps above

After a week or so, when you run `git branch` command, the output might look like this:

{% highlight bash %}

$ git branch
  JIRA-3543-fix-user-login
  JIRA-4532-fix-security-bug
  JIRA-4532-implement-new-security
* JIRA-7653-implement-logout
  master
  temp
  testing

{% endhighlight %}

Assuming that all the work is done in the above branches, it's time to delete them all except for master. Using
the command `git branch -D branch_name` is tedious because you have to type in every branch name. Auto-completion
helps but some names have the same prefix, so you still have to type a lot. Ideally, you'd run a command like this:
{% highlight bash %}
git branch -D * except master
{% endhighlight %}

Let's create one by using shell functions, pipelines and sed!

{% highlight bash %}
#git branches cleanup
function gb_cleanup(){
 git checkout master                       #switch to master
 git branch |                              #get all branches
   sed "s/^ *//" |                         #remove leading spaces
     grep -v master |                      #filter out master
        xargs git branch -D                #delete each branch
 printf "git branch\n%s\n" "$(git branch)" #final output
}

{% endhighlight %}

Copy the above function to your .bashrc or .profile files, source the file and use it on every git repository by
typing `gb_cleanup`.

This is the output of running the function on the example above:

{% highlight bash %}

$ gb_cleanup
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.
Deleted branch JIRA-3543-fix-user-login.
Deleted branch JIRA-4532-fix-security-bug.
Deleted branch JIRA-4532-implement-new-security.
Deleted branch JIRA-7653-implement-logout.
Deleted branch temp.
Deleted branch testing.
git branch
* master

{% endhighlight %}


`gb_cleanup` can be improved to support more complicated use cases like deleting every branch that does (or does not)
match a regular expression which can be passed in as an optional argument to the function. I haven't found a need for
that though.

