
### Dependências
   * npm install --save express
   * npm install --save @types/express -D
   * npm install --save typescript
   * npm install ts-node-dev -D
   * npm install tsc-init

   * OPTIONAL --> sudo npm install tsc-init -g

### Config package.json
  "scripts": {
    "dev": "ts-node-dev --transpile-only src/server.ts"
  },

### tsconfig.json
{
  "compilerOptions": {
      "module": "commonjs",
      "esModuleInterop": true,
      "allowSyntheticDefaultImports": true,
      "target": "es6",
      "noImplicitAny": true,
      "moduleResolution": "node",
      "sourceMap": true,
      "outDir": "dist",
      "baseUrl": ".",
      "paths": {
          "*": [
              "node_modules/*",
              "src/types/*"
          ]
      }
  },
  "include": [
      "src/**/*"
  ]
}

npm run dev