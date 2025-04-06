---
title : The Celebration
date : 2025-04-01
categories : [personal, economics]
tags : [dogme95, burnout, general equilibrium]
math : true
image :
    path : https://s3.amazonaws.com/criterion-production/editorial_content_posts/hero/7673-/zmxxJVXBv8FF43JFhwBV7UEOd6T0uC_original.jpg
    alt: Christian from "The Celebration" holds up two speeches
---


# NSFW section

<p style="color:MediumVioletRed;font-weight:bold;">(Warning: explicit content)</p>

I just watched Thomas Vinterberg's *The Celebration* (1998, *Festen* in Danish) and I really want a drink.

But I haven't had a drink for more than three weeks now. This is the longest time I haven't had a drink in about three years, and the only stretch I haven't had a drink for more than three days.

I don't want to say I've been sober three weeks, because then I'd really sound like an alcoholic. That was the word ("sober," not the other one) the doctor used on the phone call the other day, when I told him I had been burning myself with cigarettes and would like a referral to a psychiatrist.

So instead I went for a walk. I wanted to talk to someone. I thought about messaging the girl I had my first [MFM](https://mfm.urbanup.com/7159166) with after meeting at a [munch](https://en.wikipedia.org/wiki/Munch_(BDSM)) in Amsterdam. We liked each other, she liked another guy also, and we all got along. We went for drinks after. She talked working in consulting, and wanting to fuck the burnout out of her.

"Hey, how are you? How's the burnout?" I thought of writing.

"I know this might be weird, if so please ignore. But I just saw an insane movie, 'Festen' by Thomas Vinterberg. And now I just want to talk to someone."

I thought better than to send it, since it was only getting to 10 AM on a Wednesday in Amsterdam. She probably already had enough to deal with.

I'm dealing with some burnout of my own. Ever since I'd gotten home (and stopped drinking), I have been anxious about being productive. (But sometimes, like now, I also just don't want to work. I can feel it in my body and my brain. And this makes me more anxious, and probably a manifestation of burnout syndrome. So instead of working, I'm blogging.)

# Safe for work section

Anyway, I've been trying to start a research blog, which I could hopefully use for my PhD applications this winter, about a nine months from now, to explain what I have been doing for a year after I quit my job. So far, I am making slow progress.

My inital plan was to do a short research project on the US-Canadian trade war. The main methodology would be implementing a very simple computable egeneral equilibrium model (CGEM), which I think would be quite impressive given that I'm just a lowly pre-doc. But CGEMs turned out to be quite hard.

What the hell even is a CGEM? Luckily, I just explained this to my non-economics friend yesterday. General equilibrium models (the GEM in CGEM) are basically a toy model of the economy, represented using equations. You set up equations for household consumers and producers, and optionally, other agents like the government, central bank, and similar agents in foreign countries. But in the simplest models, the most important things are the consumers and producers.

Consumers make choices for example about how much goods they want to consume (which determines the demand of goods), and how much they want to work to be able to afford consuming those goods (which determines the the labour supply). Producers choose how many workers they need to hire (labour demand), and perhaps factor goods, they want to use to the produce final goods for consumers (supply of goods). Then you make markets clear by making supply equal demand, and bada-bing bada-bong, you've solved the equilibrium prices for goods and labour.

A simple GE model
--

Just for "fun," let's look at a simple (but non-trivial) example.

### Firms

Suppose the representative firm uses only labour $ L $ to produce goods $ Y $ with the production function:
$$
\begin{equation}
    Y = f(L) = A L^\gamma,
    \tag{production}
\end{equation}
$$

where $ A $ is a productivity factor and $ \gamma $ is a non-zero parameter. The firm maximizes profits
$$
\begin{equation}
    \pi = p Y - w L,
    \tag{profit}
\end{equation}
$$

which is the revenues from production minus the cost of labour. When the profit function is maximized, its first-order derivative is zero:
$$
\begin{align*}
    \frac{\partial \pi}{\partial L} = \gamma A p L^{\gamma-1} - w = 0.
    \tag{FOC}
\end{align*}
$$

Then the firm's labour demand is
$$
\begin{align}
    L_D^* = \left(
        \frac{w}{pA\gamma}
    \right)^{1 - \gamma},
    \tag{labour demand}
\end{align}
$$

which gives optimal production and profits
$$
\begin{align}
    Y^*
    &=
    A
    \left(
            \frac{w}{pA\gamma}
    \right)^{(1 - \gamma)\gamma},
    \tag{goods supply}
    \\
    \pi^*
    &=
    \left[
        p A
        \left(\frac{w}{pA\gamma} \right)^{\gamma}
        -
        w
    \right]
    \left( \frac{w}{pA\gamma} \right)^{1 - \gamma}.
    \tag{profit curve}
\end{align}
$$


### Households

The representative household chooses how much to work $L$ and how much to consume $C$ to maxmize their utility function
$$
\begin{equation}
    u(C, L) = \frac{C^\alpha}{L^\beta},
    \quad
    \alpha, \beta > 0.
    \tag{utility}
\end{equation}
$$

Assume that all profits made by the firm $ \pi $ are distributed to the household, though the households cannot directly control the firm's decisions (and therefore profit), so they take $ \pi $ as granted.

The household's consumption costs cannot exceed their income from profits and labour, so they are subject to the budget constraint $ p C \le \pi + w L$, where $p$ is the price of goods and $w$ is the wage rate.

Since we are in a one-period model, let's assume that the household consumes all their income, so that
$$
\begin{equation}
    p C = \pi + w L.
    \tag{budget constraint}
\end{equation}
$$

<details>
<summary>We solve for optimal consumption demand and labour supply (toggle ▶ for details).</summary>

For constrained maximization problems, we set up the <a href="https://en.wikipedia.org/wiki/Lagrange_multiplier">Langrangian function</a>
$$
\begin{equation}
    \mathcal{L} = u(C, L) + \lambda (\pi + w L - p C)
    \tag{Lagrangian}
\end{equation}
$$
and the first-order derivatives with respect to the control variables ($ C, L $) and the Lagrange $ \lambda $. The first order conditions are
$$
\begin{align}
    \frac{\partial \mathcal{L}}{\partial C}
    &=
    \alpha \frac{C^{\alpha - 1}}{L^\beta} - \lambda p
    = 0,
    \tag{$\mathcal{L}1$}\label{eq:L1}
    \\  
    \frac{\partial \mathcal{L}}{\partial L}
    &=
    -\beta \frac{C^\alpha}{L^{\beta + 1}} + \lambda w
    = 0,
    \tag{$\mathcal{L}2$}\label{eq:L2}
    \\
    \frac{\partial \mathcal{L}}{\partial \lambda}
    &=
    \pi + w L - p C
    = 0.
    \tag{$\mathcal{L}3$}\label{eq:L3}
\end{align}
$$
Then we have from \eqref{eq:L1} and \eqref{eq:L2} that
$$
\begin{align*}
    \lambda
    =
    \frac{\alpha}{p} \frac{C^{\alpha - 1}}{L^\beta}
    &=
    \frac{\beta}{w} \frac{C^\alpha}{L^{\beta + 1}}
    \\
    \implies
    \frac{L}{C} &= \frac{\beta p}{\alpha w}
    \left(
        =\frac{u_C}{u_L}
    \right)
    \tag{MRS}
    \\
    \implies
    L &= \frac{\beta p}{\alpha w} C.
    \tag{LCT}\label{eq:LTC}
\end{align*}
$$
With the budget constraint \eqref{eq:L3} and labour-consumption tradeoff \eqref{eq:LTC}, we have that
$$
\begin{align*}
    \pi + w L - p C
    =
    \pi
    + w \left(
        \frac{\beta p}{\alpha w}
    \right) C - pC
    = 0.
\end{align*}
$$

</details>

Solving for consumption, we get
$$
\begin{equation}
    C^* = \frac{\pi}{p}\frac{\alpha}{\alpha-\beta}.
    \tag{goods demand}
\end{equation}
$$
Then plugging back into the \eqref{eq:LTC}, we get
$$
\begin{equation}
    L_S^* = \frac{\pi}{w}\frac{\beta}{\alpha-\beta}.
    \tag{labour supply}
\end{equation}
$$


### Market equilibrium

The market clears when demand equals supply for goods and labour:
$$
\begin{equation*}
    Y^* = C^*, \quad L_D^* = L_S^*.
\end{equation*}
$$

<details>
<summary>We solve for the relative prices of labour and goods (toggle ▶ for details).</summary>
We have that
$$
\begin{align}
    Y^* = C^*
    \quad\iff\quad
    A
    \left(
            \frac{w}{pA\gamma}
    \right)^{(1 - \gamma)\gamma}
    &=
    \frac{\pi}{p}\frac{\alpha}{\alpha-\beta},
    \tag{E1}\label{eq:E1}
    \\
    L_D^* = L_S^*
    \quad\iff\quad
    \left(
        \frac{w}{pA\gamma}
    \right)^{1 - \gamma}
    &=
    \frac{\pi}{w}\frac{\beta}{\alpha-\beta}.
    \tag{E2}\label{eq:E2}
\end{align}
$$
Dividing \eqref{eq:E1} by \eqref{eq:E2} gives us
$$
\begin{align*}
    A
    \left(
        \frac{w}{pA\gamma}
    \right)^{\gamma}
    &=
    \frac{w}{p}\frac{\alpha}{\beta}.
\end{align*}
$$

</details>

Solving for the prices relative to each other, we get in equilibrium that
$$
\begin{align}
    \frac{w^*}{p^*}
    = A \left(
        \frac{\alpha}{\beta}
    \right)^{1-\gamma}.
    \tag{relative price}
\end{align}
$$

---

These get pretty hard to solve if you have more than a couple equations representing the agents, so you use a computer. Hence the computable part of CGEM. From what I gather, there are two main proprietary softwares that people use to do these models, where you basically plug in your equations into an interface from the 90s. But doing it this way is not interesting to me. I've been developing a sort of disdain for proprietary software in general (looking at you, Stata). Firstly, because of the time that you have to invest to learn how to work the outdated interface and syntax. And secondly, because it is not free, I usually have to steal it. For this project, it would also be incredibly unsatisfying that I would not understand how the model is actually solved.

More to come.
