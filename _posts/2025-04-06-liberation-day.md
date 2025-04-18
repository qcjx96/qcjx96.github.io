---
title : Lemming Games on Liberation Day
description : Thoughts on stock markets after the news shock.
date : 2025-04-06
categories : [journal, economics]
tags : [liberation Day, lemmings, game theory, guess 2/3]
image :
    path : https://inaturalist-open-data.s3.amazonaws.com/photos/22672833/large.jpg
    alt : A derivatives trader.
math : true
---

On Thursday I woke up to a message from my buddy. I checked the NYTimes app, and lo-and-behold, the world was aghast. The news have been filled with headlines about turmoil in markets ever since.

This got me thinking about why markets move so quickly. When bad news breaks, a sell-off is triggered, prices fall, and the valuation of the stock market falls&mdash;all in the blink of an eye.

Following the "Liberation Day" announcement, the S&P500 dropped xx% in one day, which translates to a $xx billions valuation loss. But this money is not just gone. (Though some love to use the term "value destruction." It's good for clicks, I guess.) Though global trade will suffer a shock from the tariffs, and there may be production and job losses in result, does the annoucement have any immediate real effects? Though the stock market was spassing out, global trade has likely not fallen sharply on the exact day of the annoucement. I will try to verify this with data later.

<center>Trump holds up tariffs poster like a kid showing off his piece-of-shit school project.</center>
![Trump](https://www.pinsentmasons.com/-/media/images/seo-social-media/editorial-use-only/uncategorised/trump-and-reciprocal-tariffs-board_digital---seosocialeditorial-image.jpg?h=630&w=12&rev=6dc4d2243b654f65ab57c7d250c1de8d&hash=E73CBCF4AB7C623456C13FBACB6F696F "Good at that shit-eating grin.")

The question is then: why do the markets freak out? Well, the financial markets&mdash;in my mind&mdash;are full of Patagonia-vested lemmings who in some situations [jump off cliffs en masse.](https://www.youtube.com/watch?v=YNZ_K14iT-Q)

Why do lemmings hurtle together to the point of commiting mass suicide? Well, it's just an [urban myth](https://www.britannica.com/story/do-lemmings-really-commit-mass-suicide) built on a hoax. But the myth is still an apt metaphor. 

Finance is a volume game, and Wall Street runs on fast money. With so much money to be made, people continually compete to edge ahead or undercut each other. This process sometimes results in the market "falling off the cliff." But it's not their fault. It's just the game.

## Guess 2/3

To illustrate, take the famouse game theory problem where lemmings try to [guess two-thirds of the average guess](https://en.wikipedia.org/wiki/Guess_2/3_of_the_average). Here's a [video](https://youtu.be/qQ3kFydI_xQ?si=g3JYD4cjU2KsYEAQ&t=2128) of lemmings at Yale playing this game.

The [Nash equilibrium](https://en.m.wikipedia.org/wiki/Nash_equilibrium) to this game is, surprisingly, that all lemmings choose zero.

<center>A mergers and acqusitions advisor.</center>
![Lemming](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/Tunturisopuli_Lemmus_Lemmus.jpg/960px-Tunturisopuli_Lemmus_Lemmus.jpg "This little guy has a cocaine problem."){: width="500"}


Suppose $$ N $$ lemmings enumerated by $$ i = 1, 2, ..., N $$ each guess a number $$ x_{i} \in [0, 1] $$ from zero to one. Each lemming wins if his or her guess is the closest to $$ \alpha=\frac{2}{3} $$ of the average, 

$$
\begin{equation*}
X = \frac{1}{N} \overset{N}{\underset{i=1}{\sum}} x_i
= \frac{1}{N} (x_1 + x_2 + ... + x_N).
\end{equation*}
$$

Once, the goal is to guess as close to the target as possible:
$$
\begin{equation}
    x_i \to \alpha X.
\tag{target}
\end{equation}
$$

Obviously, lemming $$ i $$ should not guess $$ x_i=1 $$. Because even if all the other lemmings choose the maximum so that $$ X = 1 $$, he should choose less since

$$
\begin{equation*}
\alpha < 1 \implies \alpha \bar X < 1,
\end{equation*}
$$

where $$ \bar X $$ represents the rational upperbound of $$ X $$. Some lemmings would definitely guess $$ x_i = 1 $$ in real life, though. But let's pretend all the lemmings are smart.

Because the lemmings are smart and know all of this, each should instead choose

$$
\begin{equation*}
x_i \overset{?}{=} \alpha = \frac{2}{3}.
\end{equation*}
$$

Right?

If you said yes, you would not be a smart lemming. Because a smart lemming $$ i $$ would remember that every other other lemming $$ j $$ is smart too, and that $$ j $$ also knows she should choose at most $$ x_j \le \frac{2}{3} $$. Not $$ x_j > \frac{2}{3} $$ like a dumb person. So a smart lemming knows that actually $$ \bar X \le \alpha $$. And therefore, he should actually choose at most

$$
\begin{equation*}
x_i \le \alpha^2 \bar X \le \frac{4}{9}.
\end{equation*}
$$

But... another lemming $$ j $$ would know this too, and will also choose $$ x_j \le \frac{4}{9} $$.

So lemming $$ i $$ should choose at most $$ x_i \le \alpha^3 $$, right? Yes, but therefore $$ j $$ should choose this too. So then $$ i $$ should choose at most $$ x_i \le \alpha^4 $$, and so on...

By this logic, each lemming should infinitely undercut the ceiling for the target $$ \alpha \bar X $$ by a factor of $$ \alpha $$. And since everyone else is also undecutting, the target value collapses. Thus by this [process](https://en.m.wikipedia.org/wiki/Strategic_dominance#Iterated_elimination_of_strictly_dominated_strategies), you get that all lemmings $$ i = 1, 2, ..., N $$ should eventually choose

$$
\begin{equation*}
x_i^* = \underset{n \to \infty}{\lim}{\alpha}^n \bar X = 0.
\tag{solution}
\end{equation*}
$$

In this scenario, no lemming can improve his outcome if he changes any other value $$ x_i > 0 $$. Otherwise they will be further from $$ \alpha \bar X $$ than the other lemmings choosing $$ x_j = 0 $$.

This is the definition of a Nash equilibrium, which is $$ x_i^* = 0 $$ actually for any $$ \alpha \in [0, 1) $$ between zero and one.


## Beauty contests

<center>Three junior analysts at a private equity fund.</center>
![Lemmings](https://img.freepik.com/premium-photo/image-adorable-arctic-lemmings-key-prey-arctic-food-chain-concept-arctic-wildlife-lemmings-food-chain-ecosystem-animal-behavior_864588-70920.jpg?w=360 "They won't talk about what happened at the strip club last Friday.")