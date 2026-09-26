<p align="center">
  <img src="assets/ezval-cookie-checker.png" alt="EZVAL — VALORANT Cookie Checker pour Windows" width="100%">
</p>

<p align="center">
  <strong>VALORANT Cookie Checker</strong><br>
  Analyse de cookies Netscape, lecture des données VALORANT et organisation des résultats dans une application Windows.
</p>

<p align="center">
  <a href="../../releases/latest"><strong>↓ Télécharger l'exécutable</strong></a>
  &nbsp;·&nbsp; Windows &nbsp;·&nbsp; Build 4 &nbsp;·&nbsp; Licence requise
</p>

---

### Interface

<p align="center">
  <img src="assets/ezval-mascot-vandal.png" alt="Mascotte EZVAL au masque de chat présentant quatre skins de Vandal" width="680">
</p>

<p align="center"><sub>La mascotte originale d'EZVAL, dans une nouvelle pose avec une collection de skins de Vandal.</sub></p>

<table>
  <tr>
    <td width="50%" align="center"><a href="assets/ezval-new-check.png"><img src="assets/ezval-new-check.png" alt="EZVAL — import de cookies et paramètres de vérification" width="100%"></a><br><sub>01 · New check — import et paramètres</sub></td>
    <td width="50%" align="center"><a href="assets/ezval-results-start.png"><img src="assets/ezval-results-start.png" alt="EZVAL — vue Results avant les premiers résultats" width="100%"></a><br><sub>02 · Results — démarrage du traitement</sub></td>
  </tr>
  <tr>
    <td width="50%" align="center"><a href="assets/ezval-results-active.png"><img src="assets/ezval-results-active.png" alt="EZVAL — résultats et progression pendant la vérification" width="100%"></a><br><sub>03 · Results — progression et statuts</sub></td>
    <td width="50%" align="center"><a href="assets/ezval-sorter.png"><img src="assets/ezval-sorter.png" alt="EZVAL — Sorter, inventaire et inspection d'un skin Vandal" width="100%"></a><br><sub>04 · Sorter — filtres, skins et inspecteur</sub></td>
  </tr>
</table>

<sub>Captures originales fournies pour cette présentation, sans retouche.</sub>

### Fonctionnement

| Étape | Traitement |
| :--- | :--- |
| **01 / Import** | Lecture d'un fichier `.txt` ou d'un dossier de cookies au format Netscape. Les fichiers identiques peuvent être ignorés par la déduplication. |
| **02 / Vérification** | Préparation des cookies, traitement des sessions et suivi de l'état de chaque entrée dans l'interface. |
| **03 / Enrichissement** | Récupération des informations VALORANT disponibles : région, rang, skins et solde VP. Les données dépendent de la session et des services distants. |
| **04 / Résultats** | Inspection, export d'un résumé JSON et classement par région, rang, quantité de skins et VP. |

### Capacités techniques

- **Traitement par lots** avec nombre de tâches simultanées réglable, progression en direct, pause, reprise et arrêt.
- **Gestion des doublons** pour éviter de traiter plusieurs fois un export identique.
- **Proxies optionnels** avec validation préalable et suivi de leur état depuis l'interface.
- **Exports structurés** : rapports JSON et arborescence `sort/<REGION>/` avec catégories `skin`, `rank`, `rank & skin` et `VP`.
- **Activation en ligne** par clé ; l'état local est protégé par DPAPI sous Windows. Les mises à jour de l'exécutable sont contrôlées par taille et empreinte SHA-256 avant remplacement.

### Utilisation

1. Téléchargez le **`.exe`** dans les **Assets** de la [dernière release](../../releases/latest).
2. Lancez EZVAL sur Windows, puis saisissez votre clé de licence. La validation nécessite une connexion Internet.
3. Dans **New check**, sélectionnez un fichier ou un dossier de cookies Netscape dont vous avez l'autorisation d'usage.
4. Consultez **Results** pour les statuts et les détails ; ouvrez **Sorter** pour le classement.

> **Sécurité des sessions** — Les cookies sont des données d'authentification sensibles. Les catégories de tri peuvent contenir des **copies des fichiers de cookies** : protégez également le dossier `sort/`. Ne publiez jamais ces fichiers dans une issue GitHub.

<p align="center"><sub>Distribution en exécutable uniquement · Projet indépendant, sans affiliation avec Riot Games ou VALORANT.</sub></p>
