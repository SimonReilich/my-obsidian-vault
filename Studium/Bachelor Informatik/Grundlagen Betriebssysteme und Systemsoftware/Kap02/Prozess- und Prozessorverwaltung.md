---
lecture: "[[Grundlagen Betriebssysteme und Systemsoftware]]"
---
#BScInfo #Informatik #GBS 
# Betriebssystem, Assembler, Maschienenebene
- Definition [[Betriebssystem]], [[Instruction Set Architecture]], [[Assembler]] 
- Jeder [[Prozess]] besitzt einen [[Prozessadressraum]] und [[Prozesskontext]] 

# Ziele & Kriterien
- Optimierungsziele sind Systemabhängig
- universell: Fairness und Balance
- Unterscheidung [[IO-bund Prozesse|IO-]] und [[CPU-bound Prozesse]] 

# Scheduling
- Prinzipielle Unterscheidung: [[Non-Preemptive-Scheduling|Non-Preemptive-]] und [[Preemptive-Scheduling]] 
- Strategien: 
	- Batch-Systeme: [[FCFS-Scheduling|FCFS]], [[SJF-Scheduling|SJF]] oder [[SRTN-Scheduling|SRTN]] 
	- Interaktive Systeme: [[RR-Scheduling|RR]] oder [[Priority-Scheduling|Priority]]
	- Echtzeit-Systeme: [[EDF-Scheduling|EDF]] oder [[RMS-Scheduling|RMS]] 