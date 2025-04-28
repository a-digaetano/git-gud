# Muovi a tempo il bacino...

Una funzionalità di git spesso sottovalutata è quella contenuta dentro la cartella `.git/hooks`.

Al suo interno, si trovano una serie di script in linguaggio bash che verranno automaticamente richiamati ad un certo momento durante le normali operazioni di git, indicato dal nome del file (per esempio `pre-commit`) senza estensione.

Alcuni esempi di funzionalità utili sono:

- nel pre-commit di lanciare un formatter automatico e una pulizia di dipendenze inutilizzate, in modo da comittare solamente file "puliti".
- nel post-merge, quando ci si accorge che sono cambiate le definizioni per la generazioni di sorgenti, rilanciare la creazione degli autogenerati.

Un comando utilizzabile all'interno degli hook per vedere se un determinato file è stato cambiato è:

```bash
git diff --name-only HEAD@{1} HEAD -- | grep -q 'nome.file';
```

Tuttavia, questi file hanno un problema: non possono essere committati dato che si trovano nella cartella usata da git.
Per ovviare al problema, si può _per ogni repository_ lanciare il comando

```bash
git config core.hooksPath .githooks
```

che cambia la cartella nella quale andare a cercare gli script a `.githooks` (ovviamente, si può scegliere qualsiasi nome)