---
lecture: "[[Grundlagen Rechnernetze und Verteilte Systeme]]"
---
#Bachelor #Informatik #GRnVs #Atomic 
# Definition
Die Fourier-Transformierte einer stetigen, integrierbaren Funktion $s(t)$ ist gegeben als
$$ \mathcal{F}(t) = {1 \over \sqrt{2 \pi}} \int_{-\infty}^\infty s(t)e^{-j\pi f t} \space dt = {1 \over \sqrt{2 \pi}} \int_{-\infty}^\infty s(t) * (\cos(2 \pi f t) - j * \sin(2 \pi f t)) \space dt $$
Die Äquivalenz $e^{jx} = \cos(x) + j \sin(x)$ bezeichnet man als Eulersche Formel. Hinweis: $\sqrt{−1} = j$ bzw. $j^2 = −1$