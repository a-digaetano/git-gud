# Branch

Non usare `git checkout` come i tuoi antenati per cambiare branch! La soluzione moderna è:
```bash
git switch
```

Oltre ad essere meno confusionario rispetto alle mille e uno funzionalità di `git checkout`, `git switch` cerca anche tra i branch remoti e, se ne trova uno con lo stesso nome, automaticatimente cambierà il riferimento HEAD con lo stato più aggiornato di quel branch, portando con sé tutte le modifiche non ancora committate (evitando di dover fare stash -> checkout -> pop).

![alt text](./assets/vscode-branch.png)

In vscode, basta cliccare in basso a sinistra sul nome del branch attuale per vedere tutti gli altri branch locali e remoti, separati in due sezioni.

Anche questo commit romperà tutto!