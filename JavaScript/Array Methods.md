# Array Methods.

## Popping, Pushing and Shifting.

**Lorsque vous travaillez avec des tableaux, il est facile de supprimer des éléments et d’ajouter de nouveaux éléments.**

## Popping.

**La méthode `pop()` supprime le dernier élément d'un tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.pop();   // Removes the last element ("Mango") from fruits```

**La méthode `pop()` retourne la valeur qui a été "extraite" :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```let x = fruits.pop();   // the value of x is "Mango```

## Pushing.

**La méthode `push()` ajoute un nouvel élément à un tableau (à la fin) :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.push("Kiwi");    //  Adds a new element ("Kiwi") to fruits```

**La méthode `push()` retourne la nouvelle longueur du tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```let x = fruits.push("Kiwi");    //  the value of x is 5```

## Shifting.

**La méthode `shift()` supprime le premier élément du tableau et "décale" tous les autres éléments vers un index inférieur :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.shift();     // Removes the first element "Banana" from fruits```

**La méthode `shift()` retourne la chaîne qui a été "décalée" :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```let x = fruits.shift();     // the value of x is "Banana"```

**La méthode `unshift()` ajoute un nouvel élément à un tableau (au début) et "décompose" les éléments plus anciens :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.unshift("Lemon");     // Adds a new element "Lemon" to fruits```

**La méthode `unshift()` retourne la nouvelle longueur du tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.unshift("Lemon");     // Returns 5```

**La propriété `length` fournit un moyen simple d’ajouter un nouvel élément à un tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits[fruits.length] = "Kiwi";     // Appends "Kiwi" to fruits```

## Splicing Array.

**La méthode `splice()` peut être utilisée pour ajouter de nouveaux éléments à un tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.splice(2, 0, "Lemon", "Kiwi");```

**Le premier paramètre (2) définit la position à laquelle les nouveaux éléments doivent être ajoutés (raccordés).**

**Le deuxième paramètre (0) définit le nombre d' éléments à supprimer .**

**Les autres paramètres ("Lemon", "Kiwi") définissent les nouveaux éléments à ajouter .**


**La méthode `splice()` retourne un tableau avec les éléments supprimés :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.splice(2, 2, "Lemon", "Kiwi");```

## Utilisation de splice() pour supprimer des éléments.

**Le paramétrage intelligent, vous pouvez utiliser splice() pour supprimer des éléments sans laisser de "trous" dans le tableau :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.splice(0, 1);     // Removes the first element of fruits```

**Le premier paramètre (0) définit la position à laquelle les nouveaux éléments doivent être ajoutés (fusionnés).**

**Le deuxième paramètre (1) définit le nombre d' éléments à supprimer.**

**Les autres paramètres sont omis. Aucun nouvel élément ne sera ajouté.**

## Merging (Concatenating) Arrays.

**La méthode `concat()` crée un nouveau tableau en fusionnant (concaténant) des tableaux existants :**

```let myGirls = ["Cecilie", "Lone"];```  
```let myBoys = ["Emil", "Tobias", "Linus"];```  
```let myChildren = myGirls.concat(myBoys);    // Concatenates (joins) myGirls and myBoys```

**La méthode `concat()` ne modifie pas les tableaux existants. Il retourne toujours un nouveau tableau.**

**La méthode `concat()` peut prendre n'importe quel nombre d'arguments de tableau :**

```let arr1 = ["Cecilie", "Lone"];```  
```let arr2 = ["Emil", "Tobias", "Linus"];```  
```let arr3 = ["Robin", "Morgan"];```  
```let myChildren = arr1.concat(arr2, arr3);    // Concatenates arr1 with arr2 and arr3```

**La méthode `concat()` peut aussi prendre des valeurs comme arguments :**

```let arr1 = ["Cecilie", "Lone"];```  
```let myChildren = arr1.concat(["Emil", "Tobias", "Linus"]);```  

## Slicing Array.

**La méthode `slice()` divise une partie d'un tableau en un nouveau tableau.**

**Cet exemple découpe une partie d'un tableau à partir de l'élément de tableau 1 ("Orange") :**

```let fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];```  
```let citrus = fruits.slice(1);```  

**La méthode `slice()` crée un nouveau tableau. Il ne supprime aucun élément du tableau source.**

**Cet exemple découpe une partie d'un tableau à partir de l'élément de tableau 3 ("Apple"):**

```let fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];```  
```let citrus = fruits.slice(3);```

**La méthode `slice()` peut prendre deux arguments comme slice(1, 3).**

**La méthode sélectionne ensuite les éléments à partir de l'argument de début et jusqu'à (sans l'inclure) l'argument de fin.**

```let fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];```  
```let citrus = fruits.slice(1, 3);```

**Si l'argument de fin est omis, comme dans les premiers exemples, la `slice()` méthode découpe le reste du tableau.**

```let fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];```  
```let citrus = fruits.slice(2);```

## Converting Arrays to Strings.

**La méthode JavaScript toString() convertit un tableau en une chaîne de valeurs de tableau (séparées par des virgules).**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```result  = fruits.toString();```  

**Résultat :**  

```Banana,Orange,Apple,Mango```

**La méthode `join()` joint également tous les éléments du tableau dans une chaîne.**

**Il se comporte de la même manière toString(), mais vous pouvez également spécifier le séparateur :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```result = fruits.join(" * ");```  

**Résultat :**

```Banana * Orange * Apple * Mango```  

## Automatic toString().

**JavaScript convertit automatiquement un tableau en chaîne séparée par des virgules lorsqu'une valeur primitive est attendue.**

**C'est toujours le cas lorsque vous essayez de générer un tableau.**

**Ces deux exemples produiront le même résultat:**

``` let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
``` result = fruits.toString();```

``` let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```result = fruits;```

**Tous les objets JavaScript ont une méthode toString ().**