---
lecture: "[[Numerisches Programmieren]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #NumProg 

# Numerische Eigenwertberechnung

- für symmetrische Matrizen ist die [[Kondition]] des Problems sehr gut
- für asymmetrische Matrizen ist die [[Kondition]] des Problems sehr schlecht
- Naive Methode: Finde Nullstellen des [[charakteristisches Polynom einer Matrix|charakteristischen Polynom]] der Matrix, z.B. mit [[Newtonmethode]] 
- Achtung: Reduktion des gutkonditionierten Problems auf Problem mit sehr schlechter [[Kondition]] => geht besser

# Verfahren

- Iterationsbasierte Verfahren: [[Poweriteration]], [[Inverse Iteration]], [[Raylight-Quotionteniteration]] 
- Andere Methode: [[QR-Iteration]]
- Viele $0$-Einträge drücken die Laufzeit => [[Householder Transformation]] um ähnliche Matrizen mit vielen $0$-Einträgen zu erhalten