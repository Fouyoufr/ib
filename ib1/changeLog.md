﻿**Version 1.5.2:**
 - Correction installation lecteur Skillpipe
 - Correction commande 'new-ib1Nat' pour switch existant non interne.

**Version 1.5:**
 - Nouvelle commande 'new-ib1Nat' pour créer/configurer le réseau NAT

**Version 1.4.4:**
 - Correction du paramètre '-First' de la commande 'start-ib1SavedVMs' pour filtrer le cas de plusieurs VM aux noms correspondant.
 - Ajout de changement de registre pour la commande 'switch-ib1VMfr'.
 - Suppression de la déclaration des 'TrustedHosts' pour la commande 'complete-ib1Setup'
 - Désactivation des services BITS et DoSVC dans la commande 'complete-ib1Setup'

**Version 1.4.3:**
- Correction du chemin du module ib1 pour "mount-ib1VHDBoot"
- Ajout d'une clef de registre "Run" dans "mount-ib1VHDBoot"

**Version 1.4.2:**
- Nouvelle commande "stop-ib1ClassRoom" pour arrêter toutes les machines du réseau local.
- Correction de l'insertion du module ib1 dans le disque virtuelle lors de la commande "mount-ib1VHDBoot" pour compatibilité versions < w10/2016.
- Ajout de la version du module dans le log de lancement

**Version 1.4.1:**
- Remplacement des ">>$null" par des "|out-null"
- Suppression des valeurs "$false" par défaut pour les paramètres de type "switch"
- Remplacement du redémarrage de WinRm par "enable-psRemoting" en le changeant de place
- Changement de la commande "get-ib1NetComputers" pour simplifier avec tableau associatif
- Sauvegarde des "TrustedHosts" pour les remettre en place après action
- Passage des réseau de la machine en "Privé" à chaque redémarrage après la commande "complete-ib1Install"

**Version 1.4:**
- Moteur de log du module (commande interne "write-ib1Log").
- Nouvelle commande pour afficher le log "get-ib1Log"
- Changement général du paramètre "-vmName" pour accepter des fragements de noms de VMs.
- Changement de syntaxe de "switch-ib1vmFR" : remplacement du paramètre "-noCheckpoint" par le paramètre "-Checkpoint"
- Ajout des paramètres "-subnet", "-Gateway" et "-getCred" à la commande "invoke-ib1NetCommand"
- Optimisation radicale de la commande "invoke-ib1NetCommand" en passant par des jobs Powershell
- Nouvelle commande "get-ib1Version"
- Installation du module ib1 dans le VHD lors du "mount-ib1VHDBoot"
- Désactivation de la session étendue sur Hyper-V avec "complete-ib1Setup" (pb groupe RDP)
- Test de disponibilité de Powershell Direct dans la commande "repair-ib1VMNetwork"
- Commande "connect-ib1VMNet" marquée comme obsolète.
- Utilisation des Notes des VMs pour tracer les actions du module.