# Express TypeScript Server

This is basically a learning-based project. In it, I will try to build a server using Express.js with TypeScript, and the step-by-step documentation is provided below.

{ "schemaVersion": 1, "label": "node", "message": "sweet world", "color": "orange" }

## Installation

Steps to install and set up the project.

1. Initialize a node project

    ```bash
    npm init -y

    ```

2. Remove {"type": "commonjs"} from "package.json" file
3. Install Express.js

    ```bash
    npm install express --save
    ```

4. Install TypeScript
    ```bash
    npm i -D typescript
    ```
5. Initialize TypeScript

```bash
npx tsc --init
```

6. Configure "tsconfig.json" file

```bash
{
  // Visit https://aka.ms/tsconfig to read more about this file
  "compilerOptions": {
    // File Layout
    "rootDir": "./src",
    "outDir": "./dist",

    // Environment Settings
    // See also https://aka.ms/tsconfig/module
    "module": "nodenext",
    "target": "esnext",
    "types": [],
    // For nodejs:
    // "lib": ["esnext"],
    // "types": ["node"],
    // and npm install -D @types/node

    // Other Outputs
    // "sourceMap": true,
    // "declaration": true,
    // "declarationMap": true,

    // Stricter Typechecking Options
    "noUncheckedIndexedAccess": true,
    "exactOptionalPropertyTypes": true,

    // Style Options
    // "noImplicitReturns": true,
    // "noImplicitOverride": true,
    // "noUnusedLocals": true,
    // "noUnusedParameters": true,
    // "noFallthroughCasesInSwitch": true,
    // "noPropertyAccessFromIndexSignature": true,

    // Recommended Options
    "strict": true,
    // "jsx": "react-jsx",
    // "verbatimModuleSyntax": true,
    "isolatedModules": true,
    "noUncheckedSideEffectImports": true,
    "moduleDetection": "force",
    "skipLibCheck": true,
  }
}
```

7. Create a folder "src" then add a file "server.ts" and pest below codes

```bash
import express, { Request, Response } from "express";

const app = express();
const port = 5000;

app.get("/", (req, res) => {
	res.send("Hello World!");
});

app.listen(port, () => {
	console.log(`Example app listening on port ${port}`);
});
```

8. Insert Express related types for TypeScripts

```bash
npm i --save-dev @types/express
```

9. Install tsx for running server repeatedly:

```bash
npm i -D tsx
```

10. Configure package.json file for dev command

```bash
"scripts": {
    "dev": "npx tsx watch ./src/server.ts"
},
```

11. Finally, run server using below command and check

```bash
npm run dev
```

Installation complete
