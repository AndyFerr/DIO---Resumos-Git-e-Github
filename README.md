
# DIO - Resumos Git e Github

Repositório para armazenar resumos sobre Git e Github o curso Versionamento de Código Git e Github da [Digital Innovation One](https://www.dio.me/).


## 📚Documentação
- [Documentação Git](https://www.git-scm.com/doc)
- [Documentação Github](https://www.docs.github.com/)
- [Editando um README](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)

## 📝 Conceitos e lembretes
- O git não reconhece diretórios vazios, fazendo-se necessário que haja algum arquivo dentro dele; para isso, é comumente usado um arquivo vazio chamado ".gitkeep".

- __Árvore de trabalho__ ➡️ __Área de preparação__ ➡️ __Commit__

- Ao modificar um arquivo, ele cai na árvore de trabalho; caso o modifique pro que era antes, o git entende que não ouve alterações e o remove dessa área.

-

## 💻 Códigos gerais no Git

```
git config
```
 _Lista as configurações do git; com o “--global” mostra as configurações locais;_
```
git config -global user.name
```
_Configura um nome_
```
git config -global user.email
```
_configura um email_
```
git config –global init.defaultBranch <main>
```
_Configura o bglh padrão do git, que às vezes está como “Master”_
```
git clone <URL> <novo nome caso queira renomear>
```
_clona um repositório do github para a sua máquina_
```
git init
```
_Transforma a pasta atual em um repositório local_
```
cd .git
```
_Acessa uma pasta com arquivos ocultos_
```
git remote -v
```
_Lista os repositórios remotos vinculados_
```
git remote add <Nome do repositório><URL>
```

_Vinculação de um repositório remoto a um repositório local_
```
git status
```
_Mostra a branch do repositório e se tem algum commit; além de mostrar o estado dos arquivos_
```
git add <nome do arquivo>
```
_Adiciona o arquivo à área de preparação_
```
git commit -m ”<descrição do commit>”
```
_Cria um commit_
```
git log
```
_Lista o hitórico de alterações/commits_
```
git reflog
```
_Todo o histórico de alterações dos commits_
```
touch <nome do arquivo>
```
_Cria um arquivo vazio_
```
echo <nome do arquivo> .gitignore
```
_Cria um arquivo ".gitignore" ao mesmo tempo que manda um arquivo para dentro dentro dele, assim o git não o reconhecerá_

---
### Desfazendo comandos no Git
```
rm rf .git
```
_Caso você tenha inicializado um repositório local por engano e queira desfazer, é só remover o .git_
```
git restore <nome do arquivo>
```
_Se tiver alterado algum arquivo e quiser voltar ao que era antes_
```
git commit -amend -m "<mensagem>"
```
_Altera a mensagem do último commit_
```
git reset -soft <hash do commit anterior ao que você quer retornar>
```
_Para retornar os arquivo de um commit à área de preparação_
```
git reset <hash do commit anterior ao que se quer retornar> // git reset mixed <hash do commit anterior ao que se quer retornar>
```
_Para retornar os arquivo de um commit à área de preparação_
```
git reset -hard <hash do commit anterior ao que se quer retornar>
```
_Apagar o commit e seus arquivos_
```
git reset <nome do arquivo>
```
_Removendo um arquivo da área de preparação_