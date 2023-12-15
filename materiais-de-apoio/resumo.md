<details>

<summary>Configurando o GIT localmente</summary>

```
git config --global user.name ""
git config --global user.email ""
```

</details>

<details>

<summary>Adicionando token gerado no GitHub</summary>

```
git config --global credential.helper store
```
</details>

<details>

<summary>Gerando senha SSH</summary>

```
ssh-keygen -t ed25519 -C "email"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

</details>

<details>

<summary>Conectando pasta local para remoto</summary>

```
git init (dentro da pasta que deseja subir)
git remote add origin URL (url do repositório)
```
</details>

<details>

<summary>Criando GitIgnore</summary>
Ignorar pasta que não deseja subir:

```
echo nomedapasta / > .gitignore
```
</details>

<details>

<summary>Git Keep</summary>
Adicionar um arquivo .gitkeep para que seja reconhecido o diretório vazio

```
touch nomedapasta / .gitkeep
```

</details>

<details>

<summary>Restaurar arquivo editado</summary>
Excluir alterações feitas

```
git restore nomedoarquivo
```

</details>

<details>

<summary>Alterar mensagem de commit</summary>
Será alterado a mensagem do ultimo commit realizado
(alterar pelo vim)

```
git commit --amend 
```
ou
(alterar direto)
```
git commit --amend -m "novocommit"
```

</details>

<details>

<summary>Git reset</summary>

**GIT RESET --SOFT** > Retorna os arquivos posteriores ao commit para a area de preparação (git add. + git commit)
```
git reset --soft iddocommitanterior
```
**GIT RESET --MIXED** > Retorna os arquivos posteriores ao commit para a area de trabalho (git commit)
```
git reset --mixed iddocommitanterior
```
**GIT RESET --HARD** > Exclui todos os arquivos posteriores ao commit (sem recuperação)
```
git reset --hard iddocommitanterior
```

</details>

<details>

<summary>Branches</summary>
Ramificações do projeto, pode ser utilizados como area de teste antes de incluir na branch principal (main).

_criar branch test:_
```
git checkout -b nomedabranch
```

_selecionar a branch:_
```
git checkout nomedabranch
```

_unificar a branch na main:_
(selecionado a main)
```
git merge nomedabranchtest
```

_deletar a banchtest:_
```
git branch -d nomedabranch
```
_histórico de commits das branchs:_
```
git branch -v
```
</details>

<details>

<summary>Comandos gerais importantes</summary>

_Clonar repositório remoto no local:_
```
git clone URLSSH nomepasta
```

_Commitar:_
```
git commit -m "nomedocommit"
```

_Puxar alterações feitas ao repositório:_
```
git pull
```

_Enviar alterações feitas no local para o remoto:_
```
git push
```

_Adicionar os arquivos na area de trabalho para commitar posteriormente:_
```
git add .
```

_Visualizar o histórico de commits:_
```
git log
```

_Verificar se há arquivos na area de trabalho ainda para submeter:_
```
git status
```

_excluir pasta que subiu errada:_
```
rm -rf .git
```

</details>


<div align="center">Feito com 💙 por <a href="https://github.com/evypersonal">Evy</a>.</div>
