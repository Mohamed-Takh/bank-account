# Bank Account

Le but de cet exercice est de réaliser une application permettant de manipuler un compte bancaire en effectuant des opérations courantes et en pouvant relever le solde de celui-ci.

Avant de commencer, quelques définitions d’usage :
 * Opération : manipulation du compte bancaire modifiant son état.
 * Retrait : opération visant à retirer de l’argent d’un compte.
 * Virement : opération visant à transférer de l’argent d’un compte vers un autre.
 * Dépôt : opération visant à déposer de l’argent sur un compte.
 * Solde : montant disponible sur un compte.
 * Relevé bancaire : liste des opérations effectuées sur un compte depuis une date donnée.
 * Découvert : situation dans laquelle se trouve un compte possédant un solde négatif.

### Contraintes : 
 * Chaque classe doit étendre au moins une interface.
 * Toutes les méthodes publiques de chacune des classes doit être présente et documentée dans une interface.
 * Le nom des interfaces doit décrire l’intention des méthodes qu’elles contiennent.
 * Chaque classe ne doit avoir qu’une seule responsabilité.
 * Les références sont toujours statiquement typées par une interface.
 * Les classes ne doivent pas avoir les mêmes noms que les interfaces qu’elles implémentent (par exemple, pas d’interface « IBankAccount » pour une classe « BankAccount »),

#### Étape 0 :
Créez une classe `Test` dans un fichier `Test.java`. Ajoutez y la méthode `main`. La méthode `main` se contentera d’appeler des méthodes `etape_n()`, comme ceci :

```java
??? main(???) {
    etape_1();
    etape_2();
    …
}
```

(Les « ??? » indiquent que vous devez aller chercher quoi indiquer ...)

Pour chaque étape, ajoutez la méthode `etape_n()` correspondante. Celle-ci aura toujours pour signature :

```java
private static void etape_n() {
    ...
}
```

Cette méthode devra toujours implémenter un ou plusieurs petits tests pour vous permettre de manipuler le code des classes que vous viendrez de développer (en plus bien sur de l’interface de BlueJ).

#### Étape 1 :

Afin de poser les premières bases de notre application, pour cette première étape, il vous est demandé de réaliser un compte bancaire simple. Celui-ci sera matérialisé à l’aide d’une classe. Il possède un solde et on doit pouvoir y retirer de l’argent et en déposer.

#### Étape 2 :

Maintenant que nous pouvons réaliser dépôts et retraits, ajoutez à l’application la notion d’opération bancaire et chaque compte bancaire devra maintenant porter l’ensemble des opérations qui y ont été effectuées.

#### Étape 3 :

Pour permettre la lisibilité des opérations, ajoutez à votre application la possibilité d’afficher la liste des opérations effectuées à l’aide d’un petit tableau en ASCII, par exemple :

```md
|Date     | Opération | Montant |  Solde|
|---------|-----------|---------|-------|
|05/12/20 | Retrait   |   50,00 | 100,00|
|20/12/20 | Dépôt     |   25,00 | 125,00|
|02/01/21 | Dépôt     |  350,00 | 475,00|
```

#### Étape 4 :

La précédente fonctionnalité nous a permis de voir que de nombreux clients exagèrent et possèdent un compte avec un solde négatif trop important. Ajoutez la notion de découvert et limitez-le à un montant qui vous semble raisonnable.

#### Étape 5 :

À présent, nous allons nous focaliser sur les virements. Lorsqu’on réalise un virement, nous demandons à la banque de réaliser un transfert de notre compte sur un autre. Implémentez cette fonctionnalité en vous basant sur cette vision des choses.

#### Étape 6 :

Pour finir, et toujours afin de satisfaire notre clientèle, ajoutez à l’application la possibilité de créer un compte épargne. Sur ce compte, on ne peut que déposer de l’argent et faire des virements, mais on ne peut pas faire de retrait.