### DocOfMacro
Cette norme de documentation est inspiré d'un live de GodOfMacro !
L'idée de cette technique est de pouvoir commenter du code même quand on a la flemme.

## Version
README.md doit contenir la version la plus moderne dans sa langue la plus universelle.
# 1.0.0 fr-FR

## Crédits
- GodOfMacro
- Monkey Company

## Fonctionnement de base

# La procédure se déroule en quatre étapes :
- Copier
- Coller
- Coder
- Documenter

# Copier

Pour utiliser une librairie ou un framework, il suffit de copier une liste d'instructions présente sur la documentation.
La mise en forme de la liste doit se transformer en commentaire au moment de la copie :

Une liste sous une forme
```
- Étape 1 : Invoquer la classe $class = new class();
- Étape 2 : Utiliser la méthode $class->function();
- Étape 3 : Récupérer le résultat $arr = $class->out('toast'); sous forme d'un tableau
```

Devra être transformé sous cette forme
```
//START Outil > Classe Truc > Action Machin : https://doc.outil.com/classe-truc/#action-machin
//Étape 1 : Invoquer la classe $class = new class();
//Étape 2 : Utiliser la méthode $class->function();
//Étape 3 : Récupérer le résultat $arr = $class->out('toast'); sous forme d'un tableau
//END Outil > Classe Truc > Action Machin
```
La liste doit comporter les étapes avec un marquage pour le début et la fin ainsi qu'un lien de référence pour cette documentation.

# Coller

La partie la plus facile, coller les commentaires dans son code !
```
//START Outil > Classe Truc > Action Machin : https://doc.outil.com/classe-truc/#action-machin
//Étape 1 : Invoquer la classe $class = new class();
//Étape 2 : Utiliser la méthode $class->function();
//Étape 3 : Récupérer le résultat $arr = $class->out('toast'); sous forme d'un tableau
//END Outil > Classe Truc > Action Machin
```

# Coder

Le code doit comporter les marquages de début et de fin avec le lien de référence et uniquement les étapes utiles
```php
function machin() {

  //START Outil > Classe Truc > Action Machin : https://doc.outil.com/classe-truc/#action-machin
  //Action 1 : Invoquer la classe $class = new class();
  $class = new class();
  //Action 3 : Récupérer le résultat $arr = $class->out('toast'); sous forme d'un tableau
  $arr = $class->out('toast');
  //END Outil > Classe Truc > Action Machin

  return $out;
}
```

# Documenter

La documentation doit comporter un sommaire en arborescence qui liste :
- Une page principale
  - Les fonctionnalités
- Les classes
  - Héritage
  - Liste des variables
  - Liste des fonctions

La page principale doit comporter un titre, une description du programme et les fonctionnalités.
Les fonctionnalités doivent comporter un titre et une description.

Chaque élément exploitable comme les classes ou les fonctions doivent comporter :
- Une ancre ou un lien : `https://doc.outil.com/classe-truc/#action-machin`
- Un titre : `Action machin`
- Une description courte : `Insère votre chaîne de caractères dans un tableau`
- Une ou plusieurs lignes de code descriptif :
```php
public class::function ( void ) : void
public class::out ( string $toast ) : array
```
- Un exemple d'utilisation concis :
```php
$class = new class();
$class->function();
$arr = $class->out('toast');
var_dump($arr);
```
- Un résultat :
```php
Array (
    [0] => 'toast'
)
```
- Enfin une liste d'étapes :
```
- Étape 1 : Invoquer la classe $class = new class();
- Étape 2 : Utiliser la méthode $class->function();
- Étape 3 : Récupérer le résultat $arr = $class->out(); sous forme d'un tableau
```

## Évolution

Il suffit de proposer une version et sa langue avec l'arborescence suivante `fr-FR/1.0.0.md`
