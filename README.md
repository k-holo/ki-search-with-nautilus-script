# ki-search-with-nautilus-script
nautilus script for search files or directories

anglais en premier suivi de l'explication en français
english first and french next

-------------------------

My first real share in gitub
it's a nautilus script wrote in python 3
to find files and directories with a part of name

I'm not fan of the find of Nautilus with ctrl + F
so I wrote a nautilus script to help me to find files ans directories
without command lines


the engine use subprocess.Popen to lunch a find in the directory you choose
glob and walk didn't gave me satisfaction

-------------------------
# to install my script 
just copy it into folder of nautilus scripts
/home/USER/.local/share/nautilus/scripts
aka :
~/.local/share/nautilus/scripts

-------------------------
my script find files or directories using a element you selected in nautilus
this element can be a file or a directory
if you selected a directory the script use it as root
if you selected a file the path of the file will be the root of search

-------------------------
only the next level of the path is use to search
so
search machin will find
/path/to/machin
or 
/path/to/machin.ext

but not 
/path/to/machin/truc
nor
/path/to/machin/truc.ext

-------------------------
# search are case insensitive

-------------------------

default search is pattern in search as *pattern*
others possibilities are
"exacty as" like pattern 
begin with like pattern*
ends with like *pattern

-------------------------
in the window of finded elements, only name are wrote
but you can see path when you clic on an element

-------------------------
# shortcuts :
ctrl + q or touche escape to exit
double clic on element to open nautilus in path of file or directory

-------------------------
# to use the script, 
right clic on file or directory
go to "Scripts" find the script
focus by default is on the entry widget
tapes your pattern search
tab to change the widget and space to select option
entrer to lunch the search

clic on element to select and initiate button to open the element in nautilus
or double clic on element to do the same  thing

--------------------------------------------------------------------------------------
# # FRANCAIS :

je ne suis pas fan de la recherche avec Ctrl + F de nautilus...
je me suis donc fait un script pour me simplifier les recherches
sans avoir à passer en ligne de commande

pour le moteur, j'ai finalement utilisé find dans un subprocess.Popen
glob ou walk étant trop pénible à utiliser dans mon cas

-------------------------
chercher_ici est un script prévu pour fonctionner en tant que nautilus script
il est à placer dans le dossier :
/home/USER/.local/share/nautilus/scripts
soit :
~/.local/share/nautilus/scripts

-------------------------
il recherche des fichiers et des dossiers depuis un répertoire
en choisissant un dossier ou un fichier

la recherche se focalise sur le dernier niveau de l'arborescence
que ce soit un fichier ou un dossier qui le soit

rechercher machin trouvera
/chemin/vers/machin
ou 
/chemin/vers/machin.ext

mais pas 
/chemin/vers/machin/truc
ni
/chemin/vers/machin/truc.ext

-------------------------
les recherches se font sans distinction de casse

-------------------------
si vous choisissez un dossier, la recherche se fera dans ce dossier
si vous choisissez un fichier, la recherche se fera à partir du dossier contenant ce fichier

-------------------------
le choix par défaut est contenant le motif de recherche, c'est à dire *recherche*
les autres possibilités sont 
    exact , c'est à dire recherche
    commence par, c'est à dire recherche*
    fini par, c'est à dire *recherche

-------------------------
dans la fenêtre des éléments trouvés, seuls les noms sont marqués
mais le chemin complet est indiqué si on clic sur un élément

-------------------------
# raccourcis clavier :
ctrl + q ou touche échappe pour quitter
double clic sur un élément pour ouvrir nautilus à l'emplacement du fichier ou du dossier

-------------------------
# pour l'utiliser, 
faites un clic droit sur un fichier ou un dossier
allez dans le choix "Scripts"
puis chercher_ici (ou un autre nom si vous avez changer le nom)
le focus est sur le entry, tapez votre recherche
tabulation permet de passer d'une option à une autre
le choix entre recherche exacte, commence par, fini par et contient, 
se fait avec la barre d'espace quand le focus est sur le choix avec la touche Tab
quelque soit l'emplacement la touche Entrée valide la recherche

après un clic sur un des éléments, un double clic sur celui ci 
ou un clic sur le bouton voir ouvre le fichier ou le dossier en sélectionné dans nautilus
