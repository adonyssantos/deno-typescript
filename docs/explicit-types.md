# Tipos de datos explícitos

# **Tipo de Datos String**

---

El tipo de datos string se utiliza para almacenar información textual. Tanto JavaScript como TypeScript usan comillas dobles ("), así como comillas simples (') para rodear su información textual como una cadena.

```json
let a: string = undefined; // Error ❌
let b: string = null; // Error ❌
let c: string = ""; ✅
let d: string = "p"; ✅
let e: string = "potazio? kon arroh blanco"; ✅
let f: string = 3; // Error ❌
let g: string = "3"; ✅
```

# **Tipo de Datos Numérico**

---

El tipo de datos `number` se usa para representar tanto enteros como valores de punto flotante en JavaScript y en TypeScript. Sin embargo, debe recordar que todos los números están representados internamente como valores de coma flotante.

```json
let a: number = undefined; // Error ❌
let b: number = null; // Error ❌
let c: number = 3; ✅
let d: number = 0b111001; // Binary ✅
let e: number = 0o436; // Octal ✅
let f: number = 0xadf0d; // Hexadecimal ✅
let g: number = "cat"; // Error ❌
```

# **Tipo de Datos Boolean**

---

A diferencia de los tipos de datos `number` y `string`, `boolean` solo tiene dos valores válidos. Solo puedes establecer su valor en `true` o `false`.

```json
let a: boolean = true; ✅
let b: boolean = false; ✅
let c: boolean = 23; // Error ❌
let d: boolean = "blue"; // Error ❌
```

# **Tipo de Datos Array**

---

Puede definir tipos de array de dos maneras diferentes en JavaScript. En el primer método, usted especifica el tipo de elementos de array seguidos por `[]` lo cual que denota un array de ese tipo. Otro método es utilizar el tipo de array genérico `Array<elemType>` . El siguiente ejemplo muestra cómo crear arrays con ambos métodos. Especificar `null` o `undefined` como uno de los elementos producirá errores cuando el indicador `strictNullChecks` sea `true`.

```tsx
let miArray: tipoDato[]; //Ejemplo
let miArray: Array<tipoDato>; //Ejemplo otra forma

let a: number[] = [4, 8, 15, 16]; ✅
let b: Array<string> = ["etece", "el", "pepe"]; ✅
let c: number[] = [1, "apple", "potato"]; //Error ❌
```

**IMPORTANTE**
Puedes crear arrays mixtos, o variables mixtas, es decir que permitan introducir distintos tipos de valores en el o que almacene varios tipos de valores, sería de esta forma:

```json
//Con los arrays se debe envolver con un **()**
let mixed: **(string|number)**[] = [1, "Toh chevere", 3] ✅
let mixed: **(string|number)**[] = [1, "Hi", false] //Error ❌

//Pero si son variables sencillas no hace falta
let uid: string|number;
uid = 123; ✅
uid = "Hello"; ✅
uid = false'//Error ❌
```

# **Tipo de Datos Object**

---

```tsx
//Esto puede causar errores por que un array
//tambien es interpretado como objeto
let myObject: object = {
  name: 'Yoshi',
  age: 30,
};

//Una forma mas específica de hacerlo sería
let myObject: {
  name: string;
  age: number;
};

myObject = {
  name: 'Luigi',
  age: 32,
};
```

# **Los tipos Any y Never**

---

Digamos que usted está escribiendo un programa donde el valor de una variable lo determinan los usuarios o el código escrito en una biblioteca de terceros. En este caso, no podrá establecer el tipo de esa variable correctamente. La variable podría ser de cualquier tipo, como una cadena de texto, número o booleano. Este problema se puede resolver usando el tipo `any`. Esto también es útil cuando está creando arrays con elementos de tipos mixtos.

```tsx
let a: any = "apple"; ✅
let b: any = 14; ✅
let c: any = false; ✅
let d: any[] = ["door", "kitchen", 13, false, null]; ✅

b = "people"; ✅
```
