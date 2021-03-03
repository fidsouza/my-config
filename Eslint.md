# Padrões de projeto
## JavaScript com Standard javascript style

### Para projetos somente javascript

```
npm install standard --save-dev
```

[mais detalhes ler a documentação](https://standardjs.com/)

### Para projetos com TypeScript 
[Es-Lint with standard-javascript-style](https://www.npmjs.com/package/eslint-config-standard-with-typescript)

Instalar utilizando o comando abaixo , importante que algumas versões superiores tem ocorrio alguns bugs que ainda não encotrei a
solução.

```
yarn add eslint@6 eslint-plugin-standard@4 eslint-plugin-promise@4 eslint-plugin-import@2 eslint-plugin-node@9 @typescript-eslint/eslint-plugin@2 eslint-config-standard-with-typescript@11.0.1 -D
```

### Arquivo de configuração tsconfig

```
{
"compilerOptions": {
	"outDir":"./dist",
	"module":"commonjs",
	"target":"es2019",
	"esModuleInterop":true,
	"allowJs":true
	}
}

```

pode também ser utilizado o comando tsconfig

```
tsc --init
```
### Configurando o ESLINT

criar o arquivo .eslintrc.json

```
{
    "extends":"standard-with-typescript",
    "parserOptions":{
        "project": "./tsconfig.json"
    }
}
```

criar o arquivo .eslintignore

```
node_modoules
dist
```

### Para projetos em typescript

[Utilizar o plugin para vscode](https://github.com/Microsoft/vscode-eslint)

### Para projetos em javascript
[Utilizar o plugin](https://github.com/standard/vscode-standard)


