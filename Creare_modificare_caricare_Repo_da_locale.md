
## Strumenti necessari
* VsCode
* una directory in locale dove creo o sposto i file della mia repo.

## Creare una Repository

1) mi sposto all'interno della directory che diventarà la mia Repository in questo caso Repo
 ~/Documenti/Dechainb/Repo $

 2) Inizializzo la directory<br>
 **git init**<br>
 Compare la scritta main<br>
 ~/Documenti/Dechainb/Repo (main)

 main indica che la directory Repo è stata inizializzata e siamo sul ramo main.
Inizializzando, abbiamo creato una cartella    *.git* 

La Directory .git ha cinque sottocartelle:<br>
hooks/<br>
info/<br>
objects/<br>
refs/<br>
branches/<br>
HEAD<br>
config<br>
description<br>

[Le  cartelle di .git](https://www.manuelricci.com/guida/come-inizializzare-git-da-riga-di-comando)

** il comando ***git status*** mi peermette di vedere lo stato della Repo e dei file al suo interno

3) lavorare sulla Repo inserendo i file con  
* vscode
* editor vi da bash line
* touch o echo comandi da bash

4) inserire i file sulla staging area
**git add**<br>Variabili:
* . tutti i file
* .read.md read1.md file specifici
* *.md file con estensione md

5) Committare, dalla staging area alla Repo

***git commit"""<br> apre editor di testo su bash. Utile se voglio scrivere un commento nascosto oltre al titolomessaggio che voglio dare alla mia commit<br>
Variabili:<br>
***git commit -m "first commit"***<br>
***git commit -m "firstcommit" -m "creato file read.md"*** la prima -m è il messaggio che vedrò su git status, il secondo - m è un commento nascosto

** Scorciatoia comandi: da working directory a Repo<br>
***git commit -ma "firstcommit" -m "creato file read.md"***

6) ** il comando ***git log*** ma io preferisco<br> ***git log --online***<br>o 
***git log --online --reverse***

git log mi darà come informazioni:<br>
commit 7af9d9b89d196ca4be265dba20deeb648544c357<br>
(HEAD -> main)<br>
Author: SDechain <dechain.trade@gmail.com><br>
Date:   Sat Aug 24 08:32:00 2024 +0200

Attenzione: git log visualizza un elenco in modalità visualizzazione e non mostra la barra per inserire nuovi comandi.<br> Premere ***q*** per uscire.

### approfondimento SHA1
7af9d9b89d196ca4be265dba20deeb648544c357 

Qualsiasi cosa in Git è controllata.<br> Il meccanismo che Git usa per fare il commit è una hash SHA-1. Si tratta di una stringa di 40-caratteri, composta da caratteri esadecimali (0–9 ed a–f) e calcolata in base al contenuto dei file o della struttura della directory in Git.

L'hash contiene un checksum. Questo significa che è impossibile cambiare il contenuto di qualsiasi file o directory senza che Git lo sappia.

Ogni commit ha il suo hash che lo identifica o, con il comando oneline comodo quando abbiamo molte commit il codice id<br>
$ git log --oneline --reverse<br>
f73e7a0 first commit<br>
7af9d9b (HEAD -> main) second Commit

### approfondimento posizione commit

(HEAD -> main)<br>
HEAD è il puntatore che indica la posizione del commit. Posso entrare nella crtella heads per vederlo<br>
***cat .git/HEAD***

## Modificare un Commit solo da locale

***git commit --amende***<br> apre editmsg dove posso modoficare il testodel commit, commento, eliminare file committati.

***git reset --soft id commit "35a00b1"*** torna alla staging area pre commit

***git reset --mixed id commit "35a00b1" torna alla working directory

***git reset --hard id commit "35a00b1" torna alla commit precedente ATTENZIONE PERCE CANCELLA I FILE

Comandi utili per puntare al commit che mi interessa: o scrivo id o digito
git reset --soft HEAD^  ogni accento circonflesso mi indica di quante commit torno indietro.<br>
Consiglio utile: prima digito git log --oneline cosi vedo i commit e a quale mi interessa puntare.

## caricare Repository su github

1) Creo la mia repo su Github e ne copio Url

2) ***git remote add origin https://github.com/..................<br> "origin è il nome che do al mio server"

3) git push -u origin main

Approfondimento: git remote

***git remote -v***<br> ottengo il nome dei server registrati e url
***cat .git/config*** apro file di configurazione server

***git remote show [nome server]***<br> mi da il dettagloio servergit remote rename origin<br>
***git remote rename [ nome server]  [nuovo nome]***<br>
***git remote remove [nome server]










 




