---
layout: post
title: Understanding Sine
permalink: understanding-sine
---

Hi, this is my math test \\( sin^2x \\).

{% highlight bash %}

function gb_cleanup(){
 git checkout master                  #in case you forgot to switch to master
 git branch |                         #get all branches
    sed "s/^ *//" |                   #remove leading spaces
      grep -v master |                #master should not be deleted!
         xargs git branch -D          #delete branches
 printf "git branch\n%s\n" "$(git branch)"
 }


{% endhighlight %}

$$a^2 + b^2=c^2$$