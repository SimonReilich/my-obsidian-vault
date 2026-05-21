---
aliases:
lecture: "[[Grundlagen Datenbanken]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #GDB
# Funktionale Abhängigkeiten
- $\alpha \to \beta$ genau dann wenn $\forall r, s \in R. r.\alpha = s.\alpha \implies r.\beta = s.\beta$
- $\alpha \subseteq R$ ist ein Super-Schlüssel, falls folgendes gilt: $\alpha \to R$
- $\beta$ ist voll funktional abhängig von $\alpha$ genau dann, wenn $\alpha \to \beta$ und $\alpha$ kann nicht mehr "verkleinert" werden, Notation: $\alpha \to^* \beta$
- $\alpha \subseteq R$ ist ein Kandidatenschlüssel, falls folgendes gilt: $\alpha \to^* R$
# Armstrong-Axiome
- Reflexivität: Falls $\beta$ eine Teilmenge von $\alpha$ ist ($\beta \subseteq \alpha$) dann gilt immer $\alpha \to \beta$, insbesondere gilt immer $\alpha \to \alpha$. 
- Verstärkung: Falls $\alpha \to \beta$ gilt, dann gilt auch $\alpha \gamma \to \beta \gamma$. 
- Transitivität: Falls $\alpha \to \beta$ und $\beta \to \gamma$ gilt, dann gilt auch $\alpha \to \gamma$.