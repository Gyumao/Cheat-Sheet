# Sorting Arrays.

## Sorting Array.

**La méthode `sort()` trie un tableau par ordre alphabétique :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.sort();    // Sorts the elements of fruits```

## Reversing Array.

**La méthode `reverse()` inverse les éléments d'un tableau.**

**Vous pouvez l'utiliser pour trier un tableau par ordre décroissant :**

```let fruits = ["Banana", "Orange", "Apple", "Mango"];```  
```fruits.sort();        // First sort the elements of fruits```  
```fruits.reverse();     // Then reverse the order of the elements```

## Numeric Sort.

**La fonction `sort()` trie les valeurs sous forme de chaînes.**

**Cela fonctionne bien pour les chaînes ("Apple" vient avant "Banana").**

**Toutefois, si les nombres sont triés sous forme de chaînes, "25" est supérieur à "100", car "2" est supérieur à "1".**

**De ce fait, la méthode `sort()` produira un résultat incorrect lors du tri des nombres.**

**Vous pouvez résoudre ce problème en fournissant une fonction de comparaison :**

```let points = [40, 100, 1, 5, 25, 10];```  
```points.sort(function(a, b){return a - b});```

**Utilisez la même astuce pour trier un tableau par ordre décroissant :**

```let points = [40, 100, 1, 5, 25, 10];```  
```points.sort(function(a, b){return b - a});```

## Compare Function.

**Le but de la fonction de comparaison est de définir un autre ordre de tri.**

**La fonction de comparaison doit renvoyer une valeur négative, nulle ou positive en fonction des arguments :**

```function(a, b){return a - b}```

**Lorsque la fonction sort() compare deux valeurs, elle envoie les valeurs à la fonction de comparaison et les trie en fonction de la valeur renvoyée (négative, nulle, positive).**

**Si le résultat est négatif, ac'est trié avant b.**
**Si le résultat est positif, bc'est trié avant a.**
**Si le résultat est 0, aucun changement n'est effectué avec l'ordre de tri des deux valeurs.**

**Exemple :**

**La fonction de comparaison compare toutes les valeurs du tableau, deux valeurs à la fois (a, b).**
**Lors de la comparaison entre 40 et 100, la sort()méthode appelle la fonction de comparaison (40, 100).**
**La fonction calcule de 40 à 100 (a - b), et puisque le résultat est négatif (-60), la fonction de tri va trier 40 comme une valeur inférieure à 100.**
**Vous pouvez utiliser cet extrait de code pour expérimenter le tri numérique et alphabétique:**

```let points = [40, 100, 1, 5, 25, 10];```  
```result = points;```  

```function myFunction1() {```  
  ```points.sort();```
  ```result = points;```  
}

```function myFunction2() {```  
  ```points.sort(function(a, b){return a - b});```  
  ```result = points;```  

## Sorting Array Random Order.

**Tri d'un tableau dans un ordre aléatoire :**

```let points = [40, 100, 1, 5, 25, 10];```  
```points.sort(function(a, b){return 0.5 - Math.random()});```

## Find the Highest (or Lowest) Array Value.

**Il n'y a pas de fonctions intégrées pour trouver la valeur max ou min dans un tableau.**
**Cependant, après avoir trié un tableau, vous pouvez utiliser l'index pour obtenir les valeurs les plus élevées et les plus basses.**

**Tri croissant :**

```let points = [40, 100, 1, 5, 25, 10];```  
```points.sort(function(a, b){return a - b});```  
```// now points[0] contains the lowest value```  
```// and points[points.length-1] contains the highest value```

**Tri décroissant :**

```let points = [40, 100, 1, 5, 25, 10];```  
```points.sort(function(a, b){return b - a});```  
```// now points[0] contains the highest value```  
```// and points[points.length-1] contains the lowest value```

**Le tri de tout un tableau est une méthode très inefficace si vous souhaitez uniquement rechercher la valeur la plus élevée (ou la plus faible).**

## Math.max() Array.

**Vous pouvez utiliser `Math.max.apply` pour trouver le nombre le plus élevé dans un tableau :**

```function myArrayMax(arr) {```  
  ```return Math.max.apply(null, arr);}```

`Math.max.apply(null, [1, 2, 3])` est équivalent à `Math.max(1, 2, 3)`.

## Math.min() Array.

**Vous pouvez utiliser `Math.min.apply` pour trouver le plus petit nombre dans un tableau :**

```function myArrayMin(arr) {```  
 ```return Math.min.apply(null, arr);}```

**`Math.min.apply(null, [1, 2, 3])` est équivalent à `Math.min(1, 2, 3)`.**

## My Min / Max JavaScript Methods.

**La solution la plus rapide consiste à utiliser une méthode "maison".**

**Cette fonction parcourt un tableau en comparant chaque valeur avec la valeur la plus élevée trouvée :**

```function myArrayMax(arr) {```  
  ```var len = arr.length;```  
 ```var max = -Infinity;```  
  ```while (len--) {```  
    ```if (arr[len] > max) {```  
      ```max = arr[len];```  
    ```}```  
 ```}```  
  ```return max;```  
```}```

**Cette fonction parcourt un tableau en comparant chaque valeur avec la valeur la plus basse trouvée :**

```function myArrayMin(arr) {```  
  ```var len = arr.length;```  
  ```var min = Infinity;```  
  ```while (len--) {```  
    ```if (arr[len] < min) {```  
      ```min = arr[len];```  
    ```}```  
  ```}```  
  ```return min;```  
```}```

## Sorting Object Arrays

**Les tableaux JavaScript contiennent souvent des objets :**

```var cars = [```  
  ```{type:"Volvo", year:2016},```  
  ```{type:"Saab", year:2001},```  
  ```{type:"BMW", year:2010}```  
```];```

**Même si les objets ont des propriétés de types de données différents, la méthode `sort()` peut être utilisée pour trier le tableau.**
**La solution consiste à écrire une fonction de comparaison pour comparer les valeurs de propriété :**

```cars.sort(function(a, b){return a.year - b.year});```

**La comparaison des `string properties` est un peu plus complexe :**

```cars.sort(function(a, b){```  
  ```var x = a.type.toLowerCase();```  
  ```var y = b.type.toLowerCase();```  
  ```if (x < y) {return -1;}```  
  ```if (x > y) {return 1;}```  
  ```return 0;```  
```});```
