# Instalacion

### Necesitaras instalar:

- **[NodeJs](https://nodejs.org/es/)** un entorno de ejecución para JavaScript construido con el motor de JavaScript V8 de Chrome.
- **[Visual Studio Code](https://code.visualstudio.com/)** el editor de código perfecto para aprovechar al máximo TypeScript
- Instalaremos **TypeScript** globalmente para tener acceso a él desde cualquier directorio.

```bash
npm install -g typescript
```

## Compilemos nuestros archivos 🗃

---

Una vez tengamos nuestro proyecto creemos nuestro primer archivo de **TypeScript**, su extensión será `.ts`. De momento la estructura de nuestro proyecto seria algo como:

- 📁 learning-typescript
  - 📄 app.ts

Usaremos el comando de compilación `**tsc**` que viene con `typescript`, para cuando deseemos compilar nuestro código.

```bash
##Ejemplo: tsc my-code.ts
tsc app.ts
```

Esto creará un archivo `app.js` el cual podremos ejecutar con node

```bash
node app.js
```

⚠️**IMPORTANTE**. Si queremos que **TypeScript** automáticamente compile nuestro archivo cuando note algún cambio 👀 podríamos ejecutar:

```bash
tsc --watch app.ts
```

## **Compilar utilizando el archivo `tsconfig.json`**

---

Para crear este archivo en nuestro proyecto ejecutemos el comando:

```bash
tsc --init
```

Este comando generará un archivo `[**tsconfig.json](http://www.typescriptlang.org/docs/handbook/tsconfig-json.html)`\*\*  con opciones de configuración mínimas, similares a las siguientes.

```json
{
  "compilerOptions": {
    "module": "commonjs",
    "target": "es5",
    "pretty": true,
    "strict": true,
    "removeComments": true
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
}
```

Con un archivo **`tsconfig.json`** ubicado en la raíz de tu proyecto de TypeScript, puede usar el comando **`tsc`** para ejecutar la compilación.
