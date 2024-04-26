[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

ANSWER:
The goal is to shpw that $O(\log_{2} n)$ is the same as $O(\log_{2} n)$, and to do that we can start with substituting in either $\log_{2}$ or $\log_{5}$ into $T(n) \in O(f(n))$. I will complete both, but for now I arbitrarily choose $\log_{2}$. With it substituted in we have $T(n) \in O(\log_{2}(n))$, then based off of the rest of the definition of $O$ we assume $T(n) \leq c * \log_{2}(n)$. In order to move forward, I need to use the change of base formula which looks like $\log_{a}(b)= \frac{(\log_{c}(b))}{(log_{c}(a))}$ to change $\log_{2}(n)$ into $\frac{\log_{5}(n)}{\log_{5}(2)}$. Now $T(n) \leq c * \log_{2}(n)$ will look like $T(n) \leq c * \frac{\log_{5}(n)}{\log_{5}(2)}$ and we see that the denominator is now a constant which makes it eligable to be combined with the constant $c$, leaving us with $T(n) \leq c * \log_{5}(n)$. Intuitively we can see that $T(n) \leq c * \log_{2}(n)$ transformed into $T(n) \leq c * \log_{5}(n)$
