# Exécuter l’agent Dynatrace sous Windows
<img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/datadog.png" width=200 height=200 >    <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/windows.png" width=200 height=200 > <br> <br>
Ce guide vous guidera à travers les étapes pour exécuter l'agent Datadog sur une machine Windows, puis affichera les métriques collectées sur un tableau de bord Datadog.
## Conditions préalables
1. Un compte Datadog actif. Si vous n'en avez pas, inscrivez-vous <a href="[https://openclassrooms.com/fr/](https://www.datadoghq.com/)">ici</a> .
2. Une machine Windows (Serveur ou Poste de travail).

## Guide étape par étape

### 1. Installez l'agent Datadog sur Windows
#### a.Téléchargez le programme d'installation :

<ul>
  <li>Connectez-vous à votre compte Datadog.</li>
  <li>Accédez à Agent > Windows .</li>
  <li>Téléchargez le programme d’installation de Datadog Agent approprié en fonction de votre version de Windows.</li>
</ul>
 
#### b.Installez l'Agent Datadog :
<ul>
  <li>Exécutez le programme d'installation en tant qu'administrateur.</li>
  <li>Suivez les invites d'installation.</li>
  <li>Lors de l'installation, il vous sera demandé votre clé API Datadog. Vous pouvez trouver cette clé dans votre tableau de bord Datadog sous Intégrations > API .</li>
</ul>
<table>
  <tr>
    <td> <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/1.png" width=350 height=350 ></td>
    <td></td>
    <td> <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/2.png" width=350 height=350 ></td>
  </tr>
  <tr>
    <td> <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/3.png" width=350 height=350 ></td>
    <td></td>
    <td>  <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/4.png" width=350 height=350 ></td>
  </tr>
</table>

#### c.Démarrez l'Agent Datadog :
Après l'installation, l'Agent Datadog commencera à s'exécuter en tant que service sur votre machine Windows. Vous pouvez gérer le service Datadog Agent via l' Servicesapplication sous Windows. <br>
<img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/5.png" width=700 height=300 >

### 2.(Facultatif) Configurer l'agent pour collecter les métriques système
Par défaut, l’agent Datadog collectera les métriques de base du système telles que l’utilisation du processeur, la mémoire et les E/S disque. Cependant, si vous souhaitez collecter des métriques supplémentaires :

1. Accédez au répertoire de configuration de l'Agent Datadog, généralement C:\ProgramData\Datadog.
2. Modifiez le datadog.yamlfichier à l'aide d'un éditeur de texte.
3. Décommentez ou ajoutez des configurations spécifiques en fonction des métriques que vous souhaitez collecter.
4. Enregistrez le fichier et redémarrez le service Datadog Agent pour que les modifications prennent effet.
### 3. Afficher le tableau de bord Datadog
  #### a. Accédez au tableau de bord Datadog :
- Connectez-vous à votre compte Datadog.
- Dans le volet de navigation de gauche, cliquez sur Tableaux de bord .
  #### b. Choisissez un tableau de bord préconfiguré :
- Datadog propose plusieurs tableaux de bord prêts à l'emploi. Pour les métriques Windows, vous trouverez le nom de la machine dans la liste du tableau de bord.
  #### c. (Facultatif) Personnaliser un tableau de bord :
- Si vous souhaitez personnaliser votre tableau de bord :
    . Cliquez sur le bouton Nouveau tableau de bord .
    . Ajoutez des widgets et sélectionnez les métriques ou les événements qui vous intéressent.
    . Personnalisez la visualisation, la période et la mise en page comme vous le souhaitez.
    . Enregistrez le tableau de bord pour référence future.
<img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/6.png" width=600 height=515 >


### 4.(Facultatif) Explorer et définir des alertes
1. Lors de l'affichage de votre tableau de bord, vous pouvez définir des alertes pour des mesures ou des événements spécifiques en cliquant sur l'icône en forme de cloche.
2. Définissez vos critères d'alerte, votre message et l'endroit où vous souhaitez être averti (par exemple, e-mail, Slack, etc.).
3. Enregistrez l'alerte et Datadog vous avertira lorsque les critères spécifiés seront remplis.
   
   <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/7.png" width=800 height=250 >
## Constatation
Vous avez installé avec succès l'agent Datadog sur votre machine Windows et vous pouvez désormais surveiller et visualiser les performances de votre système via le tableau de bord Datadog.
### 5. (Facultatif) Test de charge
Exécutez quelques commandes sur la machine Windows et affichez les modifications dans le tableau de bord.
### Ouvrez PowerShell en tant qu'administrateur et exécutez ce qui suit :
### a. Cela ajoutera une certaine charge au processeur.

```bash
    $loop = [scriptblock]::Create("while ($true) {}")
    Start-Job -ScriptBlock $loop
```
 <img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/8.png" width=800 height=257 >
 
### b. Cela ajoutera une certaine charge à la mémoire.

```bash
   $memArray = @()
   while ($true) {
    $memArray += new-object byte[] 10MB
    Start-Sleep -Seconds 2
   }
```
<img src="https://github.com/naimiatef/Datadog_Windows/blob/main/datadog/9.png" width=800 height=250 >
