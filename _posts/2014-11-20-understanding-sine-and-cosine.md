---
title: Understanding Sine And Cosine
permalink: understanding-sine-cosine
---

<p class="meta">20 November 2014 - Berkeley</p>

Do you want to understand what $sinx$ and $cosx$ are once and for all? Do you want to look at the formula
$sin^2x + cos^2x=1$ and know exactly how to prove it? If the answer is yes, continue reading.

So, what is $sinx$?
Let's say we have a right triangle with the sides `a`, `b`, `c` and the angle `x` between `c` and `b`.

![Triangle][tr]

Then, by definition

$$ sinx = \frac ac $$

That's it! You take an angle in the [right triangle][right_triangle], divide the opposite side by the longest side (the hypotenuse),
and you get the `sine` of this angle. Note that $sinx$ does not depend on the size of a right triangle,
as long as it contains the same angle $x$, since all such triangles are [similar][similar_triangle].

Cosine, tangent and cotangent are defined similarly:

$$
cosx=\frac bc\\
tanx=\frac ab\\
cotx=\frac ba
$$

These are just the **short way** to refer to the ratios of the sides of the right triangle. There is no magic.

Now, why is $tanx={sinx \over cosx}$?

$$
\frac{sinx}{cosx}=\frac{\frac ac}{\frac bc}= \frac ac * \frac cb=\frac ab=tanx
$$

Why is $tanx=\frac{1}{cotx}$?

$$
\frac{1}{cotx}=\frac{1}{\frac ba}=1 * \frac ab=\frac ab = tanx
$$

Can you prove that $cotx=\frac{cosx}{sinx}$?

Everyone has seen this formula before

$$
sin^2x + cos^2x=1
$$

It is called [Pythagorean trigonometric identity][pythagorean_trig]. Where this formula comes from is not usually
well explained. They make us remember it in high school. Let's see if we can prove it using the definitions
above and the [Pythagorean Theorem][pythagorean] which states that $a^2 + b^2=c^2$

$$
sin^2x + cos^2x=(\frac ac)^2 + (\frac bc)^2=\frac{a^2}{c^2} + \frac{b^2}{c^2}=\frac{a^2 + b^2}{c^2}
$$

Applying the pythagorean equation $a^2 + b^2=c^2$ to the numerator, we get

$$
\frac{a^2 + b^2}{c^2}=\frac{c^2}{c^2}=1
$$

And it proves that $sin^2x + cos^2x=1$.

[tr]: /images/right_triangle.png  "Triangle"
[pythagorean]: http://en.wikipedia.org/wiki/Pythagorean_theorem
[pythagorean_trig]: http://en.wikipedia.org/wiki/Pythagorean_trigonometric_identity
[pythagorean_trig]: http://en.wikipedia.org/wiki/Pythagorean_trigonometric_identity
[similar_triangle]: http://www.mathsisfun.com/geometry/triangles-similar.html
[right_triangle]: http://en.wikipedia.org/wiki/Right_triangle


