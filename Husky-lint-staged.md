# Husky

O Husky serve como hooks para validar Eslint - Testes e qualquer comando que desejar
automaticamente junto com pre-commit. 

## Instalação usando Yarn
Vou abordar somente o uso com yarn aqui, mas para saber mais pode [consultar aqui](https://typicode.github.io/husky/#/)

```
yarn install husky --save-dev
yarn add pinst --dev # if your package is not private
```
## Habilitando os hooks

```
yarn husky install
```

## Para habilitar os hooks automaticamente quando e clonado o projeto

Adicione no package.json 

```
{
  "private": true,
  "scripts": {
    "postinstall": "husky install"
  }
}
```

## Adicionando um hook
Neste exemplo e adicionado um hook para o git do pré-commit , na maioria dos
meus projetos isso ja e suficiente. 

```
npx husky add .husky/pre-commit "npm test"
```

## Lint-staged

Usar um hook para disparar um comando de lint para projetos pequenos tudo certo
,porem se houver muitos arquivos isso pode levar muito tempo. 

Para isso use o lint-staged , com isso ele so vai verificar os arquivos em 
staged ou seja quando adicionado no cabeçalho "git add˜

```
npm i lint-staged
```

Depois disso crie um arquivo chamado ".lintstagedrc"

```
{
    "./src/*.ts": [
        "eslint --fix",
        "yarn test:dev"
    ]
}
```
Nesse caso os comandos executaram somente dentro do .src/*.ts e 
dentro do array [] você pode adicionar os comandos na sequência que deseja.



