# Inciampando sui commit

Stai per pushare un commit per una fix, ma appena prima di cliccare ti accorgi che
ti sei dimenticato di modificare una riga o di aggiungere un file? Niente paura, perché esiste

```bash
git commit --amend
```

che permette di modificare l'ultimo commit in locale aggiungendo le ultime modifiche in stage.

<div class="warning">

Se il commit è stato pushato, NON FARE AMEND.
Come regola generale, una volta che un commit è online, non si tocca

</div>
