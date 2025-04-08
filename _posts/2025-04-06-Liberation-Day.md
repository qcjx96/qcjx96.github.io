---
title : Liberation Day and Lemming Games
description : Thoughts on stock markets after the news shock.
date : 2025-04-06
categories : [journal, incoherent rant]
tags : [liberation Day, lemmings, game theory]
image :
    path : https://inaturalist-open-data.s3.amazonaws.com/photos/22672833/large.jpg
    alt : A derivatives trader.
math : true
---

On Thursday I woke up to a message from my buddy. I checked the NYTimes app, and lo-and-behold, the world was aghast. The news have been filled with headlines about turmoil in markets ever since.

This got me thinking about why markets move so quickly. When bad news breaks, a sell-off is triggered, prices fall, and the valuation of the stock market falls&mdash;all in the blink of an eye.

Following the "Liberation Day" announcement, the S&P500 dropped xx% in one day, which translates to a $xx billions valuation loss. But this money is not just gone. (Though some love to use the term "value destruction." It's better for clicks, I guess.) Though global trade will suffer a shock from the tariffs, and there may be production and job losses in result, does the annoucement have any real effects? Though the stock market was spassing out, global trade has not fallen sharply on the exact day of the annoucement.

<center>Trump holds up tariffs poster like a kid showing off his piece-of-shit school project.</center>
![Trump](https://www.pinsentmasons.com/-/media/images/seo-social-media/editorial-use-only/uncategorised/trump-and-reciprocal-tariffs-board_digital---seosocialeditorial-image.jpg?h=630&w=12&rev=6dc4d2243b654f65ab57c7d250c1de8d&hash=E73CBCF4AB7C623456C13FBACB6F696F "Good at that shit eating grin.")

The question is then: why do the markets out? Well, the financial markets&mdash;in my mind&mdash;are full of Patagonia-vested lemmings, who love to [fall off cliffs together.](https://www.youtube.com/watch?v=YNZ_K14iT-Q)

Why do lemmings commit mass suicide? Why do they hurtle together to the point of jumping off cliffs? Well first of all, [they don't](https://www.britannica.com/story/do-lemmings-really-commit-mass-suicide). Second, because it's a volume game, and Wall Street runs on fast money. And because there's so much money to be made, they continually compete to undercut each other. The result is the proverbial scene of "lemmings falling off cliffs." But it's not their fault. It's simply cold, hard logic.

## Guess 2/3

To illustrate, take the famouse game theory problem where lemmings try to ["guess two-thirds of the average"](https://en.wikipedia.org/wiki/Guess_2/3_of_the_average). Here's a [video](https://youtu.be/qQ3kFydI_xQ?si=g3JYD4cjU2KsYEAQ&t=2128) of lemmings at Yale playing this game.

The Nash equilibrium to this game is, surprisingly, that all lemmings choose zero.

<center>A mergers and acqusitions specialist.</center>
![Lemming](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ef/Tunturisopuli_Lemmus_Lemmus.jpg/960px-Tunturisopuli_Lemmus_Lemmus.jpg "This little guy has a cocaine problem."){: width="500"}


Suppose $$ N $$ lemmings each enumerated by $$ i $$ guess a number $$ x_{i} \in [0, 1] $$ from zero to one. Each lemming wins if their guess is the closest to $$ \alpha=\frac{2}{3} $$ of the average, 

$$
\begin{equation*}
X = \frac{1}{N} \overset{N}{\underset{i=1}{\sum}} x_i
= \frac{1}{N} (x_1 + x_2 + ... + x_N).
\end{equation*}
$$

Actually, the Nash equilibrium is zero for any number $$ \alpha \in [0, 1) $$ between zero and one. But anyway, the goal is to guess as close to the target as possible:
$$
\begin{equation}
    x_i \simeq \alpha X.
\tag{target}
\end{equation}
$$

Obviously, lemming $$ i $$ should not choose $$ x_i=1 $$. Because even if all the other lemmings choose the maximum so that $$ X = 1 $$, he should guess less since

$$
\begin{equation*}
\alpha < 1 \implies \alpha \bar X < 1,
\end{equation*}
$$

where $$ \bar X $$ represents the rational upperbound of $$ X $ $$. Some lemmings would definitely choose $$ x_i = 1 $$ in real life, though. But let's pretend all the lemmings are smart.

Because the lemmings are smart and know all of this, each should instead choose

$$
\begin{equation*}
x_i \overset{?}{=} \alpha = \frac{2}{3}.
\end{equation*}
$$

Right?

If you said yes, you would not be a smart lemming. Because a smart lemming $$ i $$ would remember that every other other lemming $$ j $$ is smart too, and that he also know she should choose at most $$ x_j \le \frac{2}{3} $$. Not $$ x_j > \frac{2}{3} $$ like a dumb person. So a smart lemming knows that actually $$ \bar X \le \alpha $$. And therefore, he should actually choose at most

$$
\begin{equation*}
x_i \le \alpha^2 \bar X \le \frac{4}{9}.
\end{equation*}
$$

But... another lemming $$ j $$ would know this too, and will also choose $$ x_j \le \frac{4}{9} $$.

So lemming $$ i $$ should choose at most $$ x_i \le \alpha^3 $$, right? Yes. But he should then also choose at most $$ x_i \le \alpha^4 $$, and so on...

By this logic, each lemming needs to infinitely undercut the ceiling for the target $$ \alpha \bar X $$. And since everyone else is also undecutting, $$ \alpha \bar X $$ keeps collapsing. Thus by this [process](https://en.m.wikipedia.org/wiki/Strategic_dominance#Iterated_elimination_of_strictly_dominated_strategies), you get the Nash equilibrium that all lemmings should choose

$$
\begin{equation*}
x_i^* = \underset{n \to \infty}{\lim}{\alpha}^n \bar X = 0.
\tag{solution}
\end{equation*}
$$

## Beauty contests


<center>Three analysts at a private equity fund.</center>
![Lemmings](https://img.freepik.com/premium-photo/image-adorable-arctic-lemmings-key-prey-arctic-food-chain-concept-arctic-wildlife-lemmings-food-chain-ecosystem-animal-behavior_864588-70920.jpg?w=360 "They won't talk about what happened at the strip club last Friday.")