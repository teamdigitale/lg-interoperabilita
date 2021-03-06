# Linee guida del nuovo Modello di interoperabilità (BOZZA)

## Cos'è

Questo progetto è in costruzione.

Lo scopo è scrivere le *Linee guida del nuovo Modello di interoperabilità* previste
dal capitolo 5 del [Piano Triennale](https://pianotriennale-ict.italia.it/).

Questo documento segue la pubblicazione delle [Linee guida per transitare al nuovo 
Modello di interoperabilità](http://lg-transizione-interoperabilita.readthedocs.io/)

## Contribuire

La scrittura delle Linee Guida è partecipativa, i contributi sono benvenuti.

## Decisioni architetturali

Utilizziamo [Architecture Decision
Records](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)
per tracciare le decisioni relative a questa iniziativa

## Generazione della versione web

Per generare la versione navigabile occorre installare [Sphinx](http://www.sphinx-doc.org/) in questo modo:

```
virtualenv env
source env/bin/activate
pip-install sphinx
```

Una volta installato sphinx il testo si genera lanciando lo script `build.sh`
