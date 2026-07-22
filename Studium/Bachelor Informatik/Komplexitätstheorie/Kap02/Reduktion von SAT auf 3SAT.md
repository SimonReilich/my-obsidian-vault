---
lecture: "[[Komplexitätstheorie]]"
---
#BScInfo #Informatik #Comp
# Satz
$$\text{SAT} \leq_p \text{3SAT}$$[[SAT]] ist [[Karp-Reduktion in Polynomialzeit|in polynomieller Zeit karp-reduzibel]] auf [[3SAT]].

# Beweis
Eine Klausel mit $k$ Variablen kann in gleicherfüllbare $k-2$ 3-klauseln mit $2k-2$ Variablen umgewandelt werden:$$u_1 \lor u_2 \lor ... \lor u_k \rightsquigarrow (u_1 \lor u_2 \lor x_1) \land (\overline{x_1} \lor u_3 \lor x_2) \land (\overline{x_2} \lor u_4 \lor x_3) ... \land (\overline{x_{k-2}} \lor u_{k-1} \lor u_k)$$ Wenden wir dieses Verfahren auf jede Klausel der ursprünglichen Formel an, erhalten wir eine gleicherfüllbare Formel in 3-[[Konjunktiver Normalform|CNF]].