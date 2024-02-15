# DetectIntrusion
Implémentation d'un algorithme de détection d'intrusion issu de la méthode Lachina Entropy issu du papier suivant : Lakhina, M. C. A., &amp; Diot, C. (2004). Diagnosing network-wide traffic anomalies. In Proceedings of ACM SIGCOMM.

Nous avons réalisé l'entraînement et l'évaluation sur le [dataset CTU-13](https://www.stratosphereips.org/datasets-ctu13) rassemblant des données de trafic capturée à l'Université CTU en Tchèquie, en 2011. Ce jeu de données contient du trafic réel labellisé en 3 catégories : trafic normal, trafic de fond et trafic de botnet. Il rassemble treize scénarios différents (protocoles, malware, durée, activité différents).

Nous avons utilisé les datasets 1, 2 et 9 pour nos résultats, correspondant à l'action du bot Neris. La méthode peut-être étendue à d'autres scénarios, mais risque d'être moins performante étant donné l'utilisation de bots différents dans ceux-ci.
