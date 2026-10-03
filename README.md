## Setup

### Dataset

Il dataset va scaricato manualmente, estratto e messo in `./data`.
Non lo aggiungo al repo perché pesa parecchio.

### Ambiente conda

`environment.yml` è l'export dell'env conda. Non è necessario che sia allineato, è più una comodità.

Per ricreare l'ambiente:

```bash
conda env create -p ./.conda -f environment.yml
```

Per esportarlo:

```bash
conda env export --from-history | grep -vE "^(name|prefix):" > environment.yml
```

E per evitare che le semplici esecuzioni del notebook tocchino i metadati e git si agiti, da terminale col conda attivo:
```bash
conda install -c conda-forge nbstripout
nbstripout --install
```