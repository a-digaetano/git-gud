# Comandi istantanei

## Fallo ora!

```bash
git maintenance start
```

Programma delle operazioni periodiche che ottimizzano il singolo repo
su cui è stato lanciato il comando.

Nel dettaglio, le operazioni sono:
- Garbage Collection
- Commit Graph
- Prefetch
- Loose Objects
- Incremental Repack

Senza particolari controindicazioni, ogni comando git verrà velocizzato.

## Chi non muore si rivede

```bash
git config --global rerere.enabled true
```

Ricorda i merge effettuati e si ricapitano, rifalli da solo.

Salva degli hash di tutti i singoli conflitti per un determinato repo, in modo
che se dovessero ricapitare, verranno automaticamente risolti, generando meno errori.

## Switch e Restore

```bash
git switch new_branch
```

```bash
git restore <edited_file>
```

Il comando `git checkout` è sempre stato un tuttofare, permettendo di rimuovere file dallo stage,
riportarli allo stato dell'ultimo commit, annullare la risoluzione dei conflitti durante un merge,
cambiare branch e altro
Per rendere le cose un pochino più chiare, sono stati introdotti i comandi:

- `git switch` per cambiare branch e fare in modo che, se esiste una controparte remota,
verrà automaticamente tracciata
- `git restore` per annullare le modifiche effettuate dall'ultimo commit su un determinato file

## Smart Pull

```
git config --global pull.rebase true
```

Già menzionato in precedenza, permette di configurare il comportamento di default dell'operazione di pull
in maniera che eventuali commit locali che andrebbero in conflitto con quelli ormai presenti in remoto
vengano "spostati" in fondo alla timeline, in modo da non intrecciare i commit effettuati dagli utenti
e di non avere un ulteriore commit di merge che può risultare confusionario.
