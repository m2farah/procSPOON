Memo
===================

1- To build source code representation of the classes which are in folder "Dev/test/" :

> ``` java -cp spoon-core-5.5.0-jar-with-dependencies.jar spoon.Launcher -i yourAbsolutePath/Dev/test/ --gui --noclasspath ```

2 - To apply processor (compiled processor which was packed to jar file) to source application folder "Dev/bms_app" :  

> ``` java -cp processor.jar:spoon-core-5.5.0-jar-with-dependencies.jar spoon.Launcher -i Dev/bms_app/ -p CatchProcessor --noclasspath
```

## I - Trois manières pour transformer du code (Mechanisme d'intercession):

* API intercession
* Code Snippets
* Template

  ##### a) API intercession
  Très utile pour des transformations très fines. Par exemple l'ajout d'un instruction.
  Mais il est très lourd pour insérer beaucoup.

  ##### b) Code Snippets
  Très utile lorsqu'on veut ajouter des blocks d'instructions. Son usage peut s'avérer compliquer si par exemple lorsqu'il y a beaucoup des tests conditionnels.

  ##### c) Template
  Elle assez pratique et "propre". Sauf que ça mise en place nécessite plus de maitrise car son principe peut être un peu compliqué à l'aborder.
