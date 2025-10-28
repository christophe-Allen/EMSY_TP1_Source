# TP1 - Installation Linux sur une VM - V0.1

## Groupe 

- Noé Alam christophe allenbach 

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Utilisation de VMware et de l'image ISO linux 

1. Lancez VMware Workstation Player (logiciel)  

2. Sélectionnez **Create a New Virtual Machine** 

3. Placez le fichier `.iso` dans une repertoire connu : 

`C:\VosInitiales\VM\ISO`

4. Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

5. Choisir un nom d'OS : `Linux - Debian 11.x` 

![OS name choice](/Images/OS_Choice.jpg) 

6. Nommez la machine virtuelle : `SparkyLinux-NAM-CAH` 

7. Creez un disque virtuel -> capcité : **20GB** 

> remarque$$^1$$ : cocher **store virtual disk a single file**

![Virtual disk](/Images/VirtualDisk.jpg) 

> remarque$$^2$$ : ci-dessous, la configuration de la VM 

![Virtual disk](/Images/VM_Config.jpg) 

8. Lancez la machine virtuelle : **Play virtual machine** 

## Lancement de l'image ISO (Linux - Live CD) 

Lancement du live CD : 
G:
Shell Linux : 

<img width="605" height="234" alt="Capture d’écran 2025-09-18 153203" src="https://github.com/user-attachments/assets/1728c1b7-04c6-4104-9d49-362b47f9f81d" />

> Q1. Quelle est la disposition du clavier américain ?

> QWERTY

> Q2. Quelle est la disposition du clavier suisse romand ?

> QWERTZ

> Q3. Quelle est la disposition du clavier français ?

AZERTY

> 
H. Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 

> Q4. Quelle est la commande complète ?
cd /
> 

i. Affichez le contenu de la racine avec la commande : `ls –l`	
Q5. que signifie l'option -l?
C'est pour afficher le répertoire ou un dossier sous forme longue

Q6. "Décryptez" la ligne où se trouve le répertoire home.
drwxr-xr-x	1 root root	60 Sep 18 13:29
d: Indique le type de fichier ou de répertoire. Dans notre cas, d signifie un répertoire (directory)
rwxr-xr-x: Le premier groupe rwx est pour le propriétaire cela signifie que le propriétaire a des permission pour lire (r), écrire(w) et exécuter (x) sur ce répertoir
le deuxième groupe r-x: Signifie que les membre du groupe peuvent lire(r) et exécuter (x) le répertoire et non le modifier
le troixième groupe r-x: Est pour tout autre utilisateur et ils ont egalement la permision de lire (r) et exécuter (x) le répertoir, mais pas le modifier
1: Indique le nombre de lien qui pointent vers ce répertoire ou fichier 
root: Indique le propriétaire du fichier ou répertoir, dans notre cas l'utilisateur est root.
Deuxième root: Indique le groupe auquel appartient le fichiez ou le répertoire, dans notre cas le groupe est root
60: correspond à la taille du réperetoir
Sep 18 13:29 : correspond à la dernière modification du répertoir

![Placer votre capture d'écran]() 

J. Créez un répertoire de travail nommé « EMSY_XXX-YYY ».
Q7. Dans quel dossier allez-vous le placer (justifiez votre réponse) ?
Dans le répertoire /home, car il contient les répertoires personels des utilisateur.
Q8. Quelle commande allez-vous utiliser ?
sudo mkdir EMSY_NAM-CAH

K. Dans ce répertoire, créez un fichier texte que vous nommerez « TESTSLO_XXX-YYY » et écrivez
un texte, par exemple : « Test Linux by XXX et YYY » 

Q9. Pouvez-vous éditer le fichier texte uniquement avec la commande vi ?
non, il existe d'autre éditeur de texte.

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé 
ci-dessus existe toujours et pourquoi ?
Non, il n'existe plus. Car il étais enregister dans la mémoire RAM.

L. Tapez la commande `ls -l /dev/sda` 
Q11. Que signifie sda ?
sda sgnifie Disk A (premier disque).
Q12. Comme pour la question 6, « décryptez » le résultat affiché.

b: C'est le fichier bloc
rw-: propriètaire peut lire et écrire
rw-: groupe peut lire et écrire
---: les autre utilisateur no'ont aucun droits
1:	Nombre de liens phisyques vers ce fichier
root: propriètaire du fichier
disk: groupe propriètaire 
8:	numéro majeur du périférique
0: numéro mineur du périférique
Oct 2 13:07: date et heure de la dernière modification
/dev/sda: chemin du fichier périférique

<img width="409" height="60" alt="image (1)" src="https://github.com/user-attachments/assets/7192dc54-8adc-45b2-845d-aa3a98aa3fd2" />



## Questions / Réponses 

Q1. Comment se nomme le clavier américain ?

> votre réponse ?!

Q2. Comment se nomme le clavier suisse-romand ?

> votre réponse ?!

Q3. Comment se nomme le clavier français ? 

> votre réponse ?!

Q4. Que signifie l'option `-l` avec la commande `ls` 

> votre réponse ?!

Q5. Décrypter la ligne où se trouve le répertoire **home**    

[Placer votre capture d'écran]()

> votre réponse ?!

Q6. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> votre réponse ?!

Q7. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> votre réponse ?!

Q8. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> votre réponse ?!

Q9. Que signifie **sda** ? 

> votre réponse ?!

Q10. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> votre réponse ?!

Partie 3: Installation sur le disque dur de la VM

M. Pour cela, il faut lancer l’« installer» fourni avec le 
live-cd. Pour vous aider à réaliser cette installation, 
regardez les pages Wiki de la distribution de Sparky 
(aide). 
(https://wiki.sparkylinux.org/doku.php/start)

Q13. Quelle est la taille de disque minimum recommandée pour installer la distribution 
Sparky ?
il faut environ 10-20Go pour l'installation.

Q14. A quoi sert la partition swap ? Est-ce que ce principe existe sur les OS 
Microsoft Windows ? 
1.  la partition swap est une section dédiée du disque dur utilisée comme mémoire virtuelle.
2.  Oui, il existe un équivalent aux partion swap sur les OS Microsoft Windows.

Q15. Quel format pourriez-vous utiliser pour la 3ème partition afin qu’elle soit également
accessible depuis un OS Microsoft ? 
formats compatible: FAT32, exFAT, exFat32

Q16. Durant l’installation, on vous demande deux noms d’utilisateur. A quoi correspondent'ils ? 

N.
<img width="1086" height="708" alt="image" src="https://github.com/user-attachments/assets/94b75162-d8df-4c7b-9952-3a76eaac31b8" />

<img width="352" height="105" alt="image" src="https://github.com/user-attachments/assets/eb223564-11e8-4585-97c3-d1f08974ded4" />

O.Trouvez la ou les lignes de commande permettant de changer le clavier (clavier suisse romand 
trouvable sous « German (Switzerland)) et procédez à la configuration du clavier.
il faut taper cette commande: sudo dpkg-reconfigure keyboard-configuration

P.Testez si l’application « nano » est installée sur votre machine, tapez la commande : 
nano -version
Q17. À quoi sert « nano » ?
Il s'agit d'un autre éditeur de texte en ligne de commande

Q. Testez si l’application « git » est installée sur votre distribution, si ce n’est pas le cas installez
un client git.
Q18. Comment savoir si « git » est déjà installé ? 
il suffit de taper la commande git est il est censé s'ouvrir si il est installé
Q19. Quelle(s) commande(s) utilisez-vous pour l’installer ? 
Pour mettre a jour la liste de paquet: sudo apt update 
pour installer git: sudo apt install git
Q20. Que veut dire « apt » ? 
apt veut dire: Advanced Packaging Tool  
Q21. Est-ce que cette commande peut être utilisée sur toutes les distributions Linux ?
Non, elle est spécifiquement conçu pour fonctionner avec les distribution basées sur debian. 

R. Créez un sous-répertoire « EMSY_TP1_XXX-YYY » dans le répertoire de votre utilisateur.
Attention : Ici on veut que l’utilisateur (vous) ait les droits de lecture, d’écriture et d’exécution.
Q22. Quel est le répertoire utilisateur ?
le réperstoire utilisateur est cah

Q23. Quelles sont les commandes que vous allez utiliser ? 
il faut taper: mkdir EMSY_TP1_NAM-CAH

Dans ce répertoire, tapez la commande : 
git clone https://github.com/christophe-Allen/EMSY_TP1_Source
Il faut au préalable que vous ayez mis en place à cette adresse un fork du dépôt fourni.
Q24. Qu’observez-vous dans votre répertoire ?

## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

