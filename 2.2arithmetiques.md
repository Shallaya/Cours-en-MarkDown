# Glossaire d'Opérations Arithmétiques Simples

Ce glossaire contient des opérations arithmétiques de base qui peuvent être utilisées pour des exercices simples sur les fonctions en JavaScript.

## Addition
L'addition est l'opération qui consiste à ajouter deux nombres.

```javascript
function addition(a, b) {
    return a + b;
}
```

## Soustraction
La soustraction est l'opération qui consiste à retirer un nombre d'un autre.

```javascript
function soustraction(a, b) {
    return a - b;
}
```

## Multiplication
La multiplication est l'opération qui consiste à multiplier deux nombres.

```javascript
function multiplication(a, b) {
    return a * b;
}
```

## Division
La division est l'opération qui consiste à diviser un nombre par un autre.

```javascript
function division(a, b) {
    if (b !== 0) {
        return a / b;
    } else {
        throw new Error("Division par zéro non permise");
    }
}
```

## Modulo
Le modulo est l'opération qui consiste à trouver le reste de la division de deux nombres.

```javascript
function modulo(a, b) {
    return a % b;
}
```

## Exponentiation
L'exponentiation est l'opération qui consiste à élever un nombre à la puissance d'un autre nombre.

```javascript
function exponentiation(a, b) {
    return a ** b;
}
```

Ces fonctions peuvent être utilisées pour créer des exercices simples et pratiques sur les fonctions en JavaScript.