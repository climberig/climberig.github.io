---
layout: post
title: Understanding Sine And Cosine
permalink: understanding-sine-and-cosine
---

<p class="meta">20 November 2014 - Berkeley</p>

Do you want to understand what $sinx$ and $cosx$ are once and for all? Do you want to look at the formula
$sin^2x + cos^2x=1$ and know exactly how to prove it? If the answer is yes, continue reading.

So, what is $sinx$?
Let's say we have a right angle triangle with the sides `a`, `b`, `c` and the angle `x` between `c` and `b`.

![Triangle][tr]

Then, by definition

$$ sinx = \frac ac $$

That's it! You take an angle in the **right angle** triangle, divide the opposite side by the longest side (the hypotenuse),
and you get the sine of this angle.

Cosine, tangent and cotangent are defined similarly:

$$
cosx=\frac bc\\
tanx=\frac ab\\
cotx=\frac ba
$$

These are just the **short way** to refer to the ratios of the sides of right angle triangle. There is no magic. Note, however,
that these functions are only defined in the **right angle** triangle. They are undefined and won't work in
other triangles.

Now, why is $tanx={sinx \over cosx}$?

$$
\frac{sinx}{cosx}=\frac{\frac ac}{\frac bc}= \frac ac * \frac cb=\frac ab=tanx
$$

Why is $tanx=\frac{1}{cotx}$?

$$
\frac{1}{cotx}=\frac{1}{\frac ba}=1 * \frac ab=\frac ab = tanx
$$

Can you prove that $cotx=\frac{cosx}{sinx}$?

Everyone have seen this formula before

$$
sin^2x + cos^2x=1
$$

It is called [Pythagorean trigonometric identity][pythagorean_trig]. Usually, it is not well explained
where this formula comes from. They usually make us remember it in high school.
Let's see if we can prove it using the definitions above and the [Pythagorean Theorem][pythagorean] which states that $a^2 + b^2=c^2$

$$
sin^2x + cos^2x=(\frac ac)^2 + (\frac bc)^2=\frac{a^2}{c^2} + \frac{b^2}{c^2}=\frac{a^2 + b^2}{c^2}

$$

Applying the pythagorean equation $a^2 + b^2=c^2$ to the numerator, we get

$$
\frac{a^2 + b^2}{c^2}=\frac{c^2}{c^2}=1
$$

And it proves that $sin^2x + cos^2x=1$.

[tr]: /images/right_angle_triangle.png  "Triangle"
[pythagorean]: http://en.wikipedia.org/wiki/Pythagorean_theorem
[pythagorean_trig]: http://en.wikipedia.org/wiki/Pythagorean_trigonometric_identity


