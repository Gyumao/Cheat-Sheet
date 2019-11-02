# Objects JavaScript.

**Vous avez déjà appris que les variables JavaScript sont des conteneurs pour les valeurs de données.**
**Ce code attribue une valeur simple (Fiat) à une variable nommée voiture:**

```let car = "Fiat";```

**Les objets sont aussi des variables. Mais les objets peuvent contenir plusieurs valeurs.**
**Ce code affecte de nombreuses valeurs (Fiat, 500, blanc) à une variable nommée voiture :**

```let car = {type:"Fiat", model:"500", color:"white"};```

**Les valeurs sont écrites sous la forme nom: paires de valeurs (nom et valeur séparés par deux points).**

**Les objets JavaScript sont des conteneurs pour les valeurs nommées appelées propriétés ou méthodes.**

## Object Definition.

**Vous définissez (et créez) un objet JavaScript avec un littéral d'objet :**

```let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};```

**Les espaces et les sauts de ligne ne sont pas importants. Une définition d'objet peut s'étendre sur plusieurs lignes :**

``` let person = {```
  ```firstName: "John",```
  ```lastName: "Doe",```
  ```age: 50,```
  ```eyeColor: "blue"```
```};```

## Object Properties.

**Le name:values dans les objets JavaScript sont appelées propriétés :**

```Propriété	Valeur de la propriété```
```Prénom      	        John```
```nom de famille	    Biche```
```âge	                50```
```couleur des yeux	    bleu```

## Accessing Object Properties.*

**Vous pouvez accéder aux propriétés des objets de deux manières :**

```objectName.propertyName```

**ou**

```objectName["propertyName"]```

**Exemple 1**
```person.lastName;```

**exemple 2**
person["lastName"];

## Object Methods.

**Les objets peuvent aussi avoir des méthodes .**
**Les méthodes sont des actions pouvant être effectuées sur des objets.**
**Les méthodes sont stockées dans des propriétés en tant que définitions de fonction .**

```Propriété	Valeur de la propriété```
```Prénom	            John```
```nom de famille	    Biche```
```âge	                50```
```couleur des yeux	    bleu```
```nom complet	function () {return this.firstName + "" + this.lastName;}```

**Une méthode est une fonction stockée en tant que propriété.**

```let person = {```
  ```firstName: "John",```
  ```lastName : "Doe",```
  ```id       : 5566,```
  ```fullName : function() {```
    ```return this.firstName + " " + this.lastName; }```
```};```

**Le mot clé ```this```**
**Dans une définition de fonction, ```this``` fait référence au "propriétaire" de la fonction.**
**Dans l'exemple ci-dessus, ```this``` c'est l' objet personne qui "possède" la fullNamefonction.**
**En d'autres termes, ```this.firstNamesignifie``` la ```firstNamepropriété``` de cet objet.**

## Accessing Object Methods.

**Vous accédez à une méthode d'objet avec la syntaxe suivante :**

```objectName.methodName()```

**Exemple**
```name = person.fullName();```

**Si vous accédez à une méthode sans les parenthèses (), la fonction sera retournée :**

```name = person.fullName;```

## Do Not Declare Strings, Numbers, and Booleans as Objects!

**Lorsqu'une variable JavaScript est déclarée avec le mot clé ```new```, la variable est créée en tant qu'objet :**

```let x = new String();        // Declares x as a String object```
```let y = new Number();        // Declares y as a Number object```
```let z = new Boolean();       // Declares z as a Boolean object```

**Éviter String, Numberet Booleanobjets. Ils compliquent votre code et ralentissent la vitesse d'exécution.**
