# Inciampando sui commit

Stai per pushare un commit per una fix, ma appena prima di cliccare ti accorgi che
ti sei dimenticato di modificare una riga o di aggiungere un file? Niente paura, perché esiste

```bash
git commit --amend
```

che permette di modificare l'ultimo commit in locale aggiungendo le ultime modifiche in stage.

![alt text](./assets/vscode-amend.png)

<div class="warning">

Se il commit è stato pushato, **NON FARE AMEND**.
Come regola generale, una volta che un commit è online non va più toccato.

</div>

Qui mettiamo undo commit

Se invece ho già pushato? allora il revert

Se invece ti accorgi di volere davvero un singolo commit presente su un altro branch senza voler effettuare un merge (che si porterebbe dietro anche tutte le altre modifiche) allora puoi usare

```bash
git cherry-pick
```


