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
11. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 



> votre commande ?! 

12. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> votre commande ?! 

13. Tapez la commande `ls -l /dev/sda` 

![Placer votre capture d'écran]() 


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



## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

