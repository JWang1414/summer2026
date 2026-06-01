Class notes:

Lecture 6 slides

21.
While it's possible to do this segment manually, it might be useful to remember the result:
$$
	f_{Y}(y) = \frac{1}{\lvert a \rvert } f_{X}\left( \frac{y-b}{a} \right)
$$
Where $Y=aX+b$ and $f_{X}\sim \text{Exp}(\lambda)$.

25.
$$
	f_{U}(u) = f_{Z}(u) + f_{Z}(-u)
$$
The above is true because our definition of $U=\lvert Z \rvert$ essentially splits the function of $Z$ into two segments. Each of the $f_{Z}$ functions here represent one half of the full function. Specifically, $f_{Z}(u)$ represents the case when $z\geq 0$ and $f_{Z}(-u)$ represents the case when $z< 0$.

The rest of this portion is pretty straight-forward

- When we encounter non-monotonic functions, we can try to split them up into exclusively the monotonic sections

27.
I believe the reason we use the segment $-1\leq X\leq \sqrt{ y }$ here is because we are holding the lower bound static as we vary $\sqrt{ y }$. Why we do this, I do not know

- Review textbook material afterwards

31.
Not sure what a convex function is, but it seems to include most common single variable functions