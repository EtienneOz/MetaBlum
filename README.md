# MetaBlum

MetaBlum is a generated font using MetaFont language.  
The documentation is quiet messed up, a proper one will come soon.  

## Documentation
[METAFONT for Beginners](http://www.ntg.nl/doc/tobin/mf4begin.pdf)  
[MetaFontBook](http://osp.constantvzw.org/api/osp.tools.metafontbook/a88e0c2fe23d74d5299191b7ae1866362535ccaa/blob-data/MetaFontBook.pdf)   
[http://metafont.tutorial.free.fr/](http://metafont.tutorial.free.fr/)
[http://metafont-neo-doc.readthedocs.org/en/latest/index.html](http://metafont-neo-doc.readthedocs.org/en/latest/index.html) (en français!)

## Quick tutorial
Pour utiliser Metafont il faut installer avant tout Texlive (en moins de 4h ! )  
Sur linux : dans le terminal exécuter:  
```bash
    sudo apt-get install texlive
```
Sur mac : il faut avoir [macport](https://www.macports.org/) d'installé. Puis dans le terminal exécuter:  
```bash
    sudo port install textlive 
```
ou telecharger les sources de texlive puis dans le terminal :
```bash
     cd /chemin/vers/le/dossier
     sudo ./install-tl
```

L'install Linux (debian ubuntu) fonctionne. mais pas sur mac :( snifsnih  

OU  

Installer [LaTex](http://www.latex-project.org/) (généralement déjà installé sur Linux)  


Plein de fonts en .mf : [http://ctan.org/tex-archive/fonts/](http://ctan.org/tex-archive/fonts/)  

Pour generer des fichier:  
Mettre le code metafont dans un fichier .mf  
Liste de commandes pour compiler une lettre.  
```bash
     cd chemin/vers/le/dossier
     mf fichier.mf
     gftodvi fichier.2602gf   // si il y a une erreur il faut taper dans le terminal # mktextfm gray  puis relancer la commande.
     xdvi // optionnel, sur linux on peut ouvrir directement le fichier avec le visionneur de doc 
```

Ma Premiere forme --> un joli smiley
```bash
     cd vers/nouveauDossier/
     mf // lancement de métafont les ** indiquent que métafont demande un fichier.
     \relax // pour initier un nouveau fichier.
     drawdot (35,70); showit; // oeil gauche
     drawdot (65,70); showit; // oeil droit
     draw (20,40)..(50,25)..(80,40); showit; shipit; end // bouche (courbe + ecriture du fichier
```
on obtient un fichier en .2602gf, reste plus qu'à lancer les commandes vues au dessus, à partir de #gftodvi...  

## Specimen

![Demo](https://raw.githubusercontent.com/EtienneOz/MetaBlum/master/documentation/images/specimen.jpg)

## License

This Font Software is licensed under the SIL Open Font License, Version 1.1. 
This license is copied below, and is also available with a FAQ at 
http://scripts.sil.org/OFL

## Repository Layout

This font repository follows the Unified Font Repository v2.0, 
a standard way to organize font project source files. Learn more at 
https://github.com/raphaelbastide/Unified-Font-Repository
