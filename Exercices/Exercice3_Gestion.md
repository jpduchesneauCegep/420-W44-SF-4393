# Exercice 3 – Gestion des disques LVM

### Informations
- Évaluation : formative
- Type de travail : individuel
- Durée : 1 heures
- Système d'exploitation : Linux Ubuntu client 22.04 et Ubuntu serveur 22.04
- Environnement : virtuel, vsphere.

### Objectifs :

Cet exercice a pour objectifs :
- Pouvoir ajouter des disques dur dans LVM

Vous devez réaliser cette exercice sur le client et sur le serveur.


## Partie 1 : Vérification de vos disques

Vérifier l'état de votre système avant de débuté et garder une traçe des informations 

```bash
echo --- Avant modification --- > FichierDesTraces.txt
date >> FichierDesTraces.txt
df -H >> FichierDesTraces.txt
lsblk >> FichierDesTraces.txt
cat /etc/fstab >> FichierDesTraces.txt
```

## Partie 2 : État du stokage LVM

Taper les commandes suivante et garder une trace des informations :

```bash
echo --- Avant modification --- > FichierLVM.txt
date >> FichierLVM.txt
sudo pvs >> FichierLVM.txt
sudo vgs >> FichierLVM.txt
sudo lvs >> FichierLVM.txt
```

## Partie 3 : Modification de votre stokage LVM

D'abord il faut ajouter le disque sdb dans le "physiqual volume" : 
```bash
sudo pvcreate /dev/sdb # Si sdb est bien le nouveau disque vérifier avec les commandes de la partie 2
sudo pvs
```

Par la suite, nous pouvont ajouter le disque dans le "volume group" :

```bash
sudo vgextend ubuntu-vg /dev/sdb
sudo vgs 
```
Maintenant, nous allons étendre le "logical volume" :

```bash
sudo lvextend -l +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
```
Vérifier le résulat et placer l'information dans votre fichier : 
```bash
echo --- Après modification --- >> FichierLVM.txt
date >> FichierLVM.txt
sudo pvs >> FichierLVM.txt
sudo vgs >> FichierLVM.txt
sudo lvs >> FichierLVM.txt
```

## Pour vérification
Remettre une capture d’écran des trois commandes suivantes et ce pour les deux VMS (dans un seul fichier):
```bash
sudo pvs 
sudo vgs 
sudo lvs 
```
## Compétences développées


00Q1 - Effectuer l’installation et la gestion d’ordinateur :

    2 installer le système d’exploitation.
    4 Effectuer des tâches de gestion du système d’exploitation.

00SF - Évaluer des composants logiciels et matériels

    1 Rechercher des composants logiciels et matériels.
    2 Formuler des avis sur les composants logiciels et matériels.

Note : les compétences sont développées en partie.

## Références
- Ubuntu : https://ubuntu.com/download/desktop

- LVM : https://access.redhat.com/documentation/fr-fr/red_hat_enterprise_linux/6/html/logical_volume_manager_administration/index

- zsh : https://kifarunix.com/install-and-setup-zsh-and-oh-my-zsh-on-ubuntu-20-04/ 
