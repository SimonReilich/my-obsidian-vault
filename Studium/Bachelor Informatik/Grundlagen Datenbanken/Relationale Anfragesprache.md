---
aliases:
lecture: "[[Grundlagen Datenbanken]]"
degree: "[[Bachelor Informatik]]"
---
#BScInfo #Informatik #GDB
# Datentypen
- character(n), char(n), character varying / varchar(n) für text
- numeric(p, s), integer, decimal
- blob und raw für große Binärdateien
- clob für sehr große Stringattribute
- date für Datumsangaben
- xml für XML-Dokumente
# SQL-Befehle
- Anlegen von Tabellen/Relationen:
```SQL
create table Professoren 
	(PersNr integer not null, 
	Name varchar (30) not null 
	Rang character (2) );
	```
- Einfügen von Tupeln 
```SQL
insert into hoeren
	select MatrNr, VorlNr
	from Studenten, Vorlesungen
	where Titel = 'Logik';
```
- Löschen von Tupeln
```SQL
delete Studenten
	where Semester > 13;
```
- Verändern von Tupeln
```SQL
update Studenten
	set Semester = Semester + 1;
```
- Sortierung
```SQL
select PersNr, Name, Rang
from Professoren
order by Rang desc, Name asc;
```
- Duplikateliminierung
```SQL
select distinct Rang
from Professoren
```
- Mengenoperationen (Schemagleichheit!): `union, intersect, minus`
- Existenzquantor: `exists`
- Aggregatsfunktionen: `avg, min, max, count, sum`
- Modularisierung (CTE):
```SQL
with h as 
	(select VorlNr, count(*) as AnzProVorl 
	from hoeren 
	group by VorlNr), 
g as 
	(select count (*) as GesamtAnz 
	from Studenten) 
select h.VorlNr, h.AnzProVorl, g.GesamtAnz, cast(h.AnzProVorl as decimal(6,2)) / g.GesamtAnz as Marktanteil 
from g,h
```