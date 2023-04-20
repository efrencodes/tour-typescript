# Tipo y subtipos de TypeScript

[https://learn.microsoft.com/es-mx/training/paths/build-javascript-applications-typescript/](https://learn.microsoft.com/es-mx/training/paths/build-javascript-applications-typescript/)

Todos los tipos en TypeScript son subtipos de un único tipo principal denominado **any**. **any** es un tipo que puede representar cualquier valor de JavaScript sin restricciones. No generarán un error en tiempo de compilación pero en tiempo de ejecución pueden producirse errores.

> TypeScript nos provee dentro del archivo de configuración tsconfig.json una opción donde podemos definir la regla noImplicitAny a true para que TypeScript nos alerte cada vez que se usa un tipo any.

Todos los demás tipos se clasifican:

## Tipos primitivos

-   boolean
-   number
-   string
-   enum **enumeración definida por el usuario o tipos**
    Los valores **enum** comienzan con el valor de 0. Si quiere empezar con otro valor diferent, se especifica en la declaración **enum**

```typescript
// Empieza en el número 100
enum ContractStatus {
    Permanent = 100,
    Temp,
    Apprentice,
}
enum Status {
    ACTIVE = true,
    INACTIVE = false,
}
```

-   void **indica la ausencia de valor, como en una función sin ningún valor devuelto**
-   null undefined **son subtipos de todos los demás tipos**

## Tipos de objeto o parámetros de tipo

Los tipos de objeto son todos los tipos de clase, interfaz, matriz o lineal.

## Aserción de tipos

Tratar una variable como un tipo de dato diferente. La sintaxis de **as**:

```typescript
let randomValue: unknown = 10;
randomValue = true;
randomValue = 'Mateo';
if (typeof randomValue === 'string') {
    console.log((randomValue as string).toUpperCase()); //* Returns MATEO to the console.
} else {
    console.log('Error - A string was expected here.'); //* Returns an error message.
}
```
