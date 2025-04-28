# Git Workflows

![Git flow diagram](./assets/git-flow.png)
Per gentile concessione di [Vincent Driessen](https://nvie.com/posts/a-successful-git-branching-model/)

Questo è un esempio di workflow di git, uno dei più diffusi, utile soprattuto per distinguere i branch su cui si sviluppa da quelli che segnano lo stato attuale di un ambiente di produzione.

Tuttavia, non si tratta dell'unico: molti di questi sono trattati nella pagina di manuale [`man 7 gitworkflows`](https://www.man7.org/linux//man-pages/man7/gitworkflows.7.html), tuttavia vorrei soffermarmi su uno in particolare.

Il GitHub Workflow, ideato dall'omonima piattaforma, è particolarmente indicato per progetti con rolling release, in cui tutte le installazioni devono necessariamente essere sempre alla versione più aggiornata.

La parte che ritengo particolarmente interessante è quella che riguarda le Pull Request
(chiamate in maniera più sensata da GitLab "Merge Request"): si tratta di richieste di merge,
gestite tramite i permessi forniti da GitHub, che vengono costantemente aggiornate ad ogni push
e che permettono di eseguire check automatici, effettuare code review e aggiungere commenti.
Una volta che _localmente_ si sono effettuate le modifiche concordate, con un semplice push si aggiorna
automaticamente anche la pull request, in modo da effettuare nuovamente controlli e revisioni.

Una volta soddisfatti delle modifiche, un utente autorizzato (eventualmente, richiedendo anche un ulteriore revisione da un altro utente) può chiudere la Pull Request ed effettuare il merge.
