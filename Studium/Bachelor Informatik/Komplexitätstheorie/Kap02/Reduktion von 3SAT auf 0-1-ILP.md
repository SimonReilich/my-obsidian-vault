---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
$$\text{3SAT} \leq_p 0/1\text{-ILP}$$[[3SAT]] ist [[Karp-Reduktion in Polynomialzeit|in polynomieller Zeit karp-reduzibel]] auf [[0-1-ILP]].

# Beweis
Führe folgende Umwandlungen durch: $$x \mapsto x, \overline{x} \mapsto (1-x), (u_1 \lor u_2 \lor u_3) \mapsto f(u_1) + f(u_2) + f(u_3)) \geq 1$$ 