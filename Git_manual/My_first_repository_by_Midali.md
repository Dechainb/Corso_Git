Corso Midali
[video su YouTube](https://youtu.be/wPAE9-DdMtI?si=u9XnsQFVogywQ2ZN)

# my first repositiry
ciao mondo

- git  clone indirizzo url della repositoiry che trovo su code
- costruire body pagina html: maiusc + punto esclalamtivo + tab<br>
- aprire terminale ctrl + ò<br>
- git init   inizializza nuova cartella come repository<br>
- git status info su repository
- git add + nome file lo traccia nella repository<br>
- git add . traccia tutto quello che aggiungo


- git commit -m "creato pagine essenziali" fa un commit e tra virgolette scrivo cosa ho fatto in quel commit. E' come mettere una tacca sullla porta quando segno l'altezza di un bimbo.
git log mostra tutti i commit fatti

## branch di sviluppo e branch di produzione
i pallin sono i commit<br>
git checkout -b fabiodev  crea branch dove sviluppare  i miei file<br>
git checkout master  ritorno su mio branch main<br>
git merge  porta le modifiche fatte su fabiodev a main le fonde

1 modifico articolo<br>
2 git add .  convalido modifica pronto per il commit<br>
3 git reset se voglio eliminare la modifica<br>
4 git commit -m "descrizione" faccio commit<br>
5 git log mi mostra i commit fatti<br>
6 git reset HEAD~1   torna indietro di 1 commit    tilde faccio alt e 126 da tastiera numerica<br>o faccio git reset e incollo hash del commit dove voglio tornare
