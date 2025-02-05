# Les Variables en JavaScript

## Introduction
Les variables sont des conteneurs pour stocker des valeurs. En JavaScript, on utilise des variables pour stocker des données que l'on peut manipuler et utiliser tout au long de notre programme.

## Déclaration de Variables
En JavaScript, on peut déclarer des variables en utilisant les mots-clés `var`, `let` ou `const`.

### `var`
Le mot-clé `var` est utilisé pour déclarer une variable. Les variables déclarées avec `var` ont une portée de fonction ou globale.

```javascript
var x = 10;
console.log(x); // Affiche 10
```

### `let`
Le mot-clé `let` est utilisé pour déclarer une variable avec une portée de bloc. Cela signifie que la variable n'est accessible que dans le bloc où elle est déclarée.

```javascript
let y = 20;
if (true) {
    let y = 30;
    console.log(y); // Affiche 30
}
console.log(y); // Affiche 20
```

### `const`
Le mot-clé `const` est utilisé pour déclarer une constante, c'est-à-dire une variable dont la valeur ne peut pas être modifiée après sa déclaration. Les constantes ont également une portée de bloc.

```javascript
const z = 40;
console.log(z); // Affiche 40
// z = 50; // Erreur : Assignment to constant variable.
```

## Types de Variables
En JavaScript, les variables peuvent contenir différents types de données. Voici les principaux types de données :

### Nombres
Les nombres peuvent être des entiers ou des nombres à virgule flottante.

```javascript
let age = 25;
let pi = 3.14;
```

### Chaînes de caractères
Les chaînes de caractères sont des séquences de caractères entourées de guillemets simples ou doubles.

```javascript
let name = "Alice";
let greeting = 'Bonjour';
```

### Booléens
Les booléens représentent une valeur vraie ou fausse.

```javascript
let isStudent = true;
let isTeacher = false;
```

### Tableaux
Les tableaux sont des listes ordonnées de valeurs.

```javascript
let fruits = ["Pomme", "Banane", "Orange"];
```

### Objets
Les objets sont des collections de paires clé-valeur.

```javascript
let person = {
    name: "John",
    age: 30,
    isStudent: false
};
```

### Null et Undefined
`null` représente une valeur intentionnellement vide, tandis que `undefined` signifie qu'une variable n'a pas été assignée.

```javascript
let emptyValue = null;
let notAssigned;
console.log(notAssigned); // Affiche undefined
```

## Conclusion
Les variables sont essentielles en JavaScript pour stocker et manipuler des données. Il est important de choisir le bon type de variable (`var`, `let`, `const`) et de comprendre les différents types de données pour écrire un code efficace et maintenable.


## Hoisting
Le hoisting est un comportement par défaut de JavaScript où les déclarations de variables et de fonctions sont déplacées en haut de leur contexte d'exécution avant que le code ne soit exécuté. Cela signifie que vous pouvez utiliser des variables et des fonctions avant même de les avoir déclarées dans votre code.

### Hoisting avec `var`
Les variables déclarées avec `var` sont hoistées en haut de leur contexte d'exécution, mais leur initialisation reste à l'endroit où elles sont définies.

```javascript
console.log(a); // Affiche undefined
var a = 5;
console.log(a); // Affiche 5
```

### Hoisting avec `let` et `const`
Les variables déclarées avec `let` et `const` sont également hoistées, mais elles ne sont pas initialisées. Elles restent dans une "zone morte temporelle" jusqu'à ce que l'exécution atteigne leur déclaration.

```javascript
console.log(b); // Erreur : Cannot access 'b' before initialization
let b = 10;

console.log(c); // Erreur : Cannot access 'c' before initialization
const c = 15;
```

## Scope (Portée)
La portée d'une variable détermine où elle peut être accédée dans le code. En JavaScript, il existe trois types principaux de portée : globale, de fonction et de bloc.

### Portée Globale
Les variables déclarées en dehors de toute fonction ou bloc ont une portée globale et sont accessibles partout dans le code.

```javascript
var globalVar = "Je suis global";

function test() {
    console.log(globalVar); // Affiche "Je suis global"
}
test();
console.log(globalVar); // Affiche "Je suis global"
```

### Portée de Fonction
Les variables déclarées à l'intérieur d'une fonction ont une portée de fonction et ne sont accessibles qu'à l'intérieur de cette fonction.

```javascript
function test() {
    var functionVar = "Je suis dans une fonction";
    console.log(functionVar); // Affiche "Je suis dans une fonction"
}
test();
console.log(functionVar); // Erreur : functionVar is not defined
```

### Portée de Bloc
Les variables déclarées avec `let` ou `const` à l'intérieur d'un bloc (délimité par des accolades `{}`) ont une portée de bloc et ne sont accessibles qu'à l'intérieur de ce bloc.

```javascript
if (true) {
    let blockVar = "Je suis dans un bloc";
    console.log(blockVar); // Affiche "Je suis dans un bloc"
}
console.log(blockVar); // Erreur : blockVar is not defined
```

## Conclusion
Comprendre le hoisting et la portée des variables est crucial pour éviter les erreurs et écrire un code JavaScript clair et maintenable. Utilisez `let` et `const` pour bénéficier d'une portée de bloc et éviter les pièges du hoisting avec `var`.

## Les Tableaux en JavaScript

Les tableaux sont des structures de données utilisées pour stocker des collections d'éléments. En JavaScript, un tableau peut contenir des éléments de différents types, y compris des nombres, des chaînes de caractères, des objets et même d'autres tableaux.

### Création de Tableaux
Vous pouvez créer un tableau en utilisant des crochets `[]` et en séparant les éléments par des virgules.

```javascript
let fruits = ["Pomme", "Banane", "Orange"];
let mixedArray = [1, "Bonjour", true, { name: "Alice" }];
```

### Accéder aux Éléments d'un Tableau
Les éléments d'un tableau sont accessibles via leur index, qui commence à 0.

```javascript
let firstFruit = fruits[0]; // "Pomme"
let secondFruit = fruits[1]; // "Banane"
```

### Modifier les Éléments d'un Tableau
Vous pouvez modifier les éléments d'un tableau en utilisant leur index.

```javascript
fruits[1] = "Kiwi";
console.log(fruits); // ["Pomme", "Kiwi", "Orange"]
```

### Méthodes Courantes des Tableaux

#### `push()`
Ajoute un ou plusieurs éléments à la fin du tableau et retourne la nouvelle longueur du tableau.

```javascript
fruits.push("Mangue");
console.log(fruits); // ["Pomme", "Kiwi", "Orange", "Mangue"]
```

#### `pop()`
Supprime le dernier élément du tableau et le retourne.

```javascript
let lastFruit = fruits.pop();
console.log(lastFruit); // "Mangue"
console.log(fruits); // ["Pomme", "Kiwi", "Orange"]
```

#### `shift()`
Supprime le premier élément du tableau et le retourne.

```javascript
let firstFruit = fruits.shift();
console.log(firstFruit); // "Pomme"
console.log(fruits); // ["Kiwi", "Orange"]
```

#### `unshift()`
Ajoute un ou plusieurs éléments au début du tableau et retourne la nouvelle longueur du tableau.

```javascript
fruits.unshift("Fraise");
console.log(fruits); // ["Fraise", "Kiwi", "Orange"]
```

#### `indexOf()`
Retourne le premier index où un élément donné peut être trouvé dans le tableau, ou -1 s'il n'est pas présent.

```javascript
let index = fruits.indexOf("Kiwi");
console.log(index); // 1
```

#### `splice()`
Ajoute ou supprime des éléments d'un tableau.

```javascript
fruits.splice(1, 1, "Pêche", "Abricot");
console.log(fruits); // ["Fraise", "Pêche", "Abricot", "Orange"]
```

#### `slice()`
Retourne une copie superficielle d'une portion du tableau dans un nouveau tableau.

```javascript
let someFruits = fruits.slice(1, 3);
console.log(someFruits); // ["Pêche", "Abricot"]
```

#### `forEach()`
Exécute une fonction donnée sur chaque élément du tableau.

```javascript
fruits.forEach(function(fruit) {
    console.log(fruit);
});
// Affiche "Fraise", "Pêche", "Abricot", "Orange"
```

#### `map()`
Crée un nouveau tableau avec les résultats de l'appel d'une fonction fournie sur chaque élément du tableau.

```javascript
let upperFruits = fruits.map(function(fruit) {
    return fruit.toUpperCase();
});
console.log(upperFruits); // ["FRAISE", "PÊCHE", "ABRICOT", "ORANGE"]
```

#### `filter()`
Crée un nouveau tableau avec tous les éléments qui passent le test implémenté par la fonction fournie.

```javascript
let longFruits = fruits.filter(function(fruit) {
    return fruit.length > 5;
});
console.log(longFruits); // ["Fraise", "Abricot"]
```

#### `reduce()`
Applique une fonction sur un accumulateur et chaque valeur du tableau (de gauche à droite) pour réduire à une seule valeur.

```javascript
let totalLength = fruits.reduce(function(accumulator, fruit) {
    return accumulator + fruit.length;
}, 0);
console.log(totalLength); // 22
```

## Conclusion
Les tableaux sont des structures de données puissantes et flexibles en JavaScript. En utilisant les méthodes courantes des tableaux, vous pouvez facilement manipuler et transformer les données pour répondre à vos besoins spécifiques.