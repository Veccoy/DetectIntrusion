# DetectIntrusion
Implémentation d'un algorithme de détection d'intrusion issu de la méthode Lachina Entropy issu du papier suivant : Lakhina, M. C. A., &amp; Diot, C. (2004). Diagnosing network-wide traffic anomalies. In Proceedings of ACM SIGCOMM.

Nous avons réalisé l'entraînement et l'évaluation sur le [dataset CTU-13](https://www.stratosphereips.org/datasets-ctu13) rassemblant des données de trafic capturée à l'Université CTU en Tchèquie, en 2011. Ce jeu de données contient du trafic réel labellisé en 3 catégories : trafic normal, trafic de fond et trafic de botnet. Il rassemble treize scénarios différents (protocoles, malware, durée, activité différents).

Nous avons utilisé les datasets 1, 2 et 9 pour nos résultats, correspondant à l'action du bot Neris. La méthode peut-être étendue à d'autres scénarios, mais risque d'être moins performante étant donné l'utilisation de bots différents dans ceux-ci.

### Téléchargements des données

Utilisez les lignes suivantes pour télécharger la totalité des données et placez les dans un répertoire `Datasets/`.

```
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-42/detailed-bidirectional-flow-labels/capture20110810.binetflow -O CTU13_42.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-43/detailed-bidirectional-flow-labels/capture20110811.binetflow -O CTU13_43.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-44/detailed-bidirectional-flow-labels/capture20110812.binetflow -O CTU13_44.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-45/detailed-bidirectional-flow-labels/capture20110815.binetflow -O CTU13_45.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-46/detailed-bidirectional-flow-labels/capture20110815-2.binetflow -O CTU13_46.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-47/detailed-bidirectional-flow-labels/capture20110816.binetflow -O CTU13_47.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-48/detailed-bidirectional-flow-labels/capture20110816-2.binetflow -O CTU13_48.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-49/detailed-bidirectional-flow-labels/capture20110816-3.binetflow -O CTU13_49.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-50/detailed-bidirectional-flow-labels/capture20110817.binetflow -O CTU13_50.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-51/detailed-bidirectional-flow-labels/capture20110818.binetflow -O CTU13_51.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-52/detailed-bidirectional-flow-labels/capture20110818-2.binetflow -O CTU13_52.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-53/detailed-bidirectional-flow-labels/capture20110819.binetflow -O CTU13_53.binetflow
wget https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-54/detailed-bidirectional-flow-labels/capture20110815-3.binetflow -O CTU13_54.binetflow
```
