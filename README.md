# Minhas configs de Git e Demais ...
Minhas configurações de git e demais coisas.


# Como usar ? 

Para editar o arquivo config do git utilizar o seguinte comando

```
git config --global --edit 
```

# Configurações

estas são as minhas configurações 

```
# This is Git's per-user configuration file.
[user]
# Please adapt and uncomment the following lines:
        name = Filipe Da costa de souza
        email = filipe.cdesouza@gmail.com
[alias]
 s = !git status -s
 c = !git add --all && git commit -m
 l = !git log --pretty=formart:'%C(blue)%h %C(white)%cn %C(cyan)%an %C(red)%cr'
 ```
 
 Basta substituir o arquivo por este e pronto alguns comandos agora fica mais facil de ser utilizados. 

 ## Exemplo

 para utilizar o git status agora, basta utilizar git s , e o git commit git c " sua branch"

 ## Padronizando commits 

 E importante dentro da linha do tempo ter commits padronizados , para isto pode ser utilizar a convençao [Conventional Commit](https://www.conventionalcommits.org/en/v1.0.0/) , existe uma lib git-commit-msg-linter para que você consiga forçar a todos a manter esta
 convenção.

 ```
npm install git-commit-msg-linter --save-dev
 ```

Veja Também
[padrões de prettier](Eslint.md)
[Husky e Lint-Staged](Husky-lint-staged.md)