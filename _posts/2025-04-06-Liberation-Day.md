---
title : Liberation Day and Beauty Contests
description : Thoughts on markets after the news shock.
date : 2025-04-06
image :
    path : https://www.pinsentmasons.com/-/media/images/seo-social-media/editorial-use-only/uncategorised/trump-and-reciprocal-tariffs-board_digital---seosocialeditorial-image.jpg?h=630&w=12&rev=6dc4d2243b654f65ab57c7d250c1de8d&hash=E73CBCF4AB7C623456C13FBACB6F696F
    alt : Trump holds up tariffs poster like a kid showing off his piece-of-shit school project.
math : true
---

<b><center>(work in progress)</center></b><br>

On Thursday I woke up to a message from my buddy. I checked the NYTimes app, and lo-and-behold, the world was aghast. The news have been filled with headlines about turmoil in markets ever since.

<center><b>Waking up Thursday</b></center>
![Text](../assets/img/misc/LD-text-long.png "Why is he such a dumbass?"){: width="600"}

<center><b>The top <a href="https://www.nytimes.com/live/2025/04/07/business/trump-tariffs-stock-market">NYT headline</a> this morning.</b></center>
![NYT](../assets/img/misc/LD-nyt.png "NYT headline this morning"){: width="600"}



This got me thinking about why markets move so quickly. When bad news breaks, a sell-off is triggered, prices fall, and the valuation of the stock market falls&mdash;all in the blink of an eye.

Following the "Liberation Day" annoucement, the S&P500 dropped xx% in one day, which translates to a $xx billions valuation loss. But this money is not just gone. (Though some love to use the term "value destruction." It's better for clicks, I guess.) Though global trade will suffer a shock from the tariffs, and there may be production and job losses in result, does the annoucement have any real effects? Though the stock market was spassing out, global trade has not fallen sharply on the exact day of the annoucement.

The question is then: why do stocks spaz out? Well, the financial markets&ndash;in my mind&ndash;are full of Patagonia-vested lemmings, who love to [fall off cliffs together.](https://www.youtube.com/watch?v=YNZ_K14iT-Q)

Why do lemmings commit mass suicide? Why do they hurtle together to the point of jumping off cliffs? Well first of all, [they don't](https://www.britannica.com/story/do-lemmings-really-commit-mass-suicide). Second, because it's a volume game, and Wall Street runs on fast money. And because there's a lot of money to be made, they compete to undercut each other by slivers. The result is the proverbial scene of "lemmings falling off cliffs." But it's not their fault. It's simply cold hard logic.

## Guess 2/3 with smart lemmings

As an illustration, take the famouse game theory problem where lemmings try to ["guess two-thirds of the average"](https://en.wikipedia.org/wiki/Guess_2/3_of_the_average). Here's a [video](https://youtu.be/qQ3kFydI_xQ?si=g3JYD4cjU2KsYEAQ&t=2128) of Yale students playing this game.

The Nash equilibrium to this game is, surprisingly, that all player choose zero.

Suppose $ N > 1 $ lemmings, enumerated by $ i $, each guess a number $ x_{i} \in [0, 1] $ from zero to one hundred. Lemmings win if their guess is the closest to $\alpha=\frac{2}{3}$ of the average $\bar x = \frac{1}{N} \overset{N}{\underset{i=1}{\sum}} x_i.$ The Nash equilibrium result is actually the same for any number $\alpha \in [0, 1)$ between zero and one.

But anyway, the goal is to guess a $ x_i \in [0, 1]$ as close to the target $ \alpha \bar x$ as possible.

Obviously, lemming $i$ should not choose $x_i=1$. Because even if all the other lemmings choose the maximum so that $\bar x = 1$, it must be that $\alpha \bar x < 1$ since $\alpha = \frac{2}{3} < 1$.

Some lemmings would definitely choose $x_i = 1$ in real life. But let's pretend all the lemmings are smart. Because the lemmings are smart and know all of this, each should instead choose $ x_i = \frac{2}{3} $, right? If you said yes, you would not be a smart lemming.

Because a smart lemming would remember that all the other lemmings are smart too, and know that they should also choose at most $ x_i \le \frac{2}{3} $, and not $ x_i > \frac{2}{3} $ like a not-smart person.

So the smart lemming $i$ knows that actually, the mean should be less than $\bar x < \alpha$. And therefore, he should actually choose at most $x_i \le \alpha^2 = \frac{4}{9}$. But... all the other lemmings know this too.

So it should choose at most $ x_i \le \alpha^3 $, right? Yes. But it should also at most choose $ x_i \le \alpha^4 $. And again, and again...

By this logic, it needs to infintely undercut the ceiling for the target $\bar x$. And since everyone else is also undecutting, $\bar x$ keeps moving down. Thus by this process, you get the Nash equilibrium that all lemmings should choose $x_i^* = \underset{\alpha \to \infty}{\lim}{\alpha}^n \bar X = 0$.

