# Functions JavaScript

**Une fonction JavaScript est un bloc de code conçu pour effectuer une tâche particulière.**
**Une fonction JavaScript est exécutée lorsque "quelque chose" (l'appelle).**

```function myFunction(p1, p2) {```  
  ```return p1 * p2;   // The function returns the product of p1 and p2```
```}```

## Function Syntax.

**Une fonction JavaScript est définie avec le functionmot - clé, suivi d'un nom , suivi de parenthèses () .**
**Les noms de fonction peuvent contenir des lettres, des chiffres, des traits de soulignement et des signes **dollar (mêmes règles que les variables).**
**Les parenthèses peuvent inclure des noms de paramètres séparés par des virgules:**
**( paramètre1, paramètre2, ... )**
**Le code à exécuter, par la fonction, est placé entre accolades: {}**

```function name(parameter1, parameter2, parameter3) {```  
  ```// code to be executed```
```}```  

**Les paramètres de fonction sont listés entre parenthèses () dans la définition de fonction.**
**Les arguments de fonction sont les valeurs reçues par la fonction lorsqu'elle est appelée.**
**Dans la fonction, les arguments (les paramètres) se comportent comme des variables locales.**
**Une fonction est sensiblement la même chose qu'une procédure ou un sous-programme, dans d'autres langages de programmation.**

## Function Invocation.

**Le code à l'intérieur de la fonction sera exécuté lorsque "quelque chose" (appellera) la fonction:**
 **-Lorsqu'un événement se produit (lorsqu'un utilisateur clique sur un bouton).**
 **-Quand il est appelé (appelé) depuis du code JavaScript.**
 **-Automatiquement (auto-invoqué).**

## Function Return.

**Lorsque JavaScript atteint une returninstruction, la fonction cesse de s'exécuter.**
**Si la fonction a été appelée à partir d'une instruction, JavaScript "retournera" pour exécuter le code après l'instruction appelante.**
**Les fonctions calculent souvent une valeur de retour . La valeur de retour est "renvoyée" à "l'appelant":**

### Pourquoi des fonctions?
**Vous pouvez réutiliser le code: définissez le code une fois et utilisez-le plusieurs fois.**
**Vous pouvez utiliser le même code plusieurs fois avec des arguments différents pour produire des résultats différents.**

**Convertissez Fahrenheit en Celsius:**

```function toCelsius(fahrenheit) {```
  ```return (5/9) * (fahrenheit-32);```
```}```

### L'opérateur () appelle la fonction.

**En utilisant l'exemple ci-dessus, toCelsiusfait référence à l'objet fonction et toCelsius()au résultat de la fonction.**
**Accéder à une fonction sans () retournera la définition de la fonction au lieu du résultat.**

## Functions Used as Variable Values.

**Les fonctions peuvent être utilisées de la même manière que vous utilisez des variables, dans tous les types de formules, d'affectations et de calculs.**

**Au lieu d'utiliser une variable pour stocker la valeur de retour d'une fonction :**

```let x = toCelsius(77);```
```let text = "The temperature is " + x + " Celsius";```

**Vous pouvez utiliser la fonction directement, en tant que valeur de variable :**

```let text = "The temperature is " + toCelsius(77) + " Celsius";```

**Vous en apprendrez beaucoup plus sur les fonctions plus loin dans ce tutoriel.**

## Local Variables.

**Les variables déclarées dans une fonction JavaScript deviennent LOCAL pour la fonction.**
**Les variables locales ne sont accessibles que depuis la fonction.**

```// code here can NOT use carName```
```function myFunction() {```
  ```let carName = "Volvo";```
  ```// code here CAN use carName```
```}```
```// code here can NOT use carName```

**Comme les variables locales ne sont reconnues que dans leurs fonctions, les variables portant le même nom peuvent être utilisées dans différentes fonctions.**
**Les variables locales sont créées au démarrage d'une fonction et supprimées à la fin.**