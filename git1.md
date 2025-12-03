|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 01 - Git, VSCode e GitLens
### 1. Introdução ao Controle de Versão

**O que é um sistema de controle de versão?**

>Um *sistema de controle de versão* permite **rastrear mudanças**, **restaurar versões anteriores** e manter o histórico de arquivos ao longo do tempo. Ele evita problemas como perda de conteúdo, versões duplicadas e desorganização.

 **O que é o Git?**

>O **Git** é um sistema de controle de versão distribuído, eficiente e rápido, capaz de gerenciar projetos pequenos e grandes.  
Ele registra todas as modificações ao longo do desenvolvimento, permitindo compreender *o quê* mudou, *quando* e *por quê*.

 **Conceitos fundamentais**
-   **Repositório:** Pasta que contém todos os arquivos do projeto e seu histórico.
-   **Commit:** Um *checkpoint*, uma versão salva e permanente do projeto.
-   **Servidores remotos:** GitHub, GitLab e Bitbucket (não cobertos em detalhes nesta aula).

----------

### 2. Instalação do Git

A instalação varia conforme o sistema operacional.

**Windows (instalação nativa)**
-   Baixar instalador oficial.
-   Utilizar opções padrão.
-   Verificar instalação com `git --version`.

 **Windows via WSL**
~~Foi o que eu usei ...~~ 😬  
*Permite rodar Linux dentro do Windows, oferecendo:*
-   Melhor compatibilidade com ferramentas do mercado
-   Ambiente de desenvolvimento equivalente ao usado profissionalmente  
    Procedimento:

**Passos:**
1.  Executar `wsl --install` como administrador.
2.  Criar usuário Linux.
3.  Atualizar pacotes:  
    `sudo apt update && sudo apt upgrade`
4.  Instalar Git:  
    `sudo apt install git`.

**Linux:** Instalação via gerenciador de pacotes da distribuição (Ubuntu, Debian, Fedora etc.).
**macOS:** Instalação disponível no site oficial do Git.

----------
### 3. Configuração Inicial do Git
**Nome e Email**
Configurações obrigatórias:
`git config --global user.name "Seu Nome" git config --global user.email "seu@email.com"` 

**Editor de texto:** Define o editor aberto pelo Git:
-   Windows sem WSL: **notepad**
-   Linux/macOS/WSL: **nano**
`git config  --global core.editor nano` 

**Outras configurações importantes**
-   **Alias:** atalhos para comandos longos
-   **Color UI:** ativa cores no terminal
-   **Merge tool:** ferramenta para resolver conflitos
-   **Push default, pull rebase, autocrlf** etc.

**Configurações globais x locais**
-   `--global`: vale para todos os projetos
-   Local (sem flag): válida apenas para o repositório atual
----------

### 4. Fluxo de Trabalho Básico com Git
 **Criando um projeto**
1.  Criar pasta: `mkdir projeto`
2.  Entrar na pasta: `cd projeto`
3.  Inicializar repositório:  
    `git init`
>Uma pasta oculta **.git** é criada, ela contém *todo o histórico do projeto*.

**Working Tree:** São os arquivos reais da pasta do projeto.

 `git status`: Mostra o estado atual:
-   Arquivos novos (**untracked**)
<font color="red"> Arquivos modificados </font>
<font color="green">Arquivos prontos para commit </font>
 
 `git add`: Envia arquivos modificados para o **Index (Staging Area)**.

**Index / Staging Area:** Local temporário onde ficam as alterações que serão incluídas no commit.

Estados possíveis:
-   **Untracked files**
-   **Changes not staged for commit**
-   **Changes to be committed**

`git commit`: Cria um snapshot permanente do estado do Index:
`git commit  -m "Mensagem"` 
>Importante: **cada commit armazena todos os arquivos do projeto**, não apenas os modificados.

`git log`: Mostra o histórico de commits, incluindo:
-   Hash (ID único)
-   Autor
-   Data
-   Mensagem

----------

### 5. Fluxos de Trabalho Adicionais
 **Git não rastreia pastas:** Somente arquivos. Pastas só aparecem se contiverem algum arquivo.
 **Deletar arquivos:**
-   Remover arquivo da Working Tree.
-   Atualizar Index: `git add arquivo`
-   Registrar commit.

 **Renomear arquivos:** O Git detecta renomeações por heurística ao executar `git add`.
**Mover arquivos:** Funciona como renomear, o Git detecta pelo conteúdo.
 **Ignorar arquivos (.gitignore):** Permite indicar arquivos que não devem ser rastreados.
Exemplos:
`*.txt
docs/
anotacoes/*.md` 

**Remover mudanças do Index:** O “desfazer do git add”:
`git reset HEAD arquivo` 

**Comparar versões (git diff):**
-   Working Tree vs Index
-   Index vs último commit
-   Dois commits
-   Working Tree vs commit

 **Remendar o último commit:** Adicionar mudanças que ficaram de fora:
`git commit  --amend` 

**Tags:** Rótulos para marcar versões:
`git tag v1.0
git tag v1.0 <hash>
git tag -d v1.0` 

 **Alias:** Criar atalhos para comandos frequentes:

`git config --global  alias.l "log --oneline"` 

----------

### 6. Visual Studio Code (VSCode)
**Instalação:** Disponível para Windows, Linux e macOS.

**WSL:** Instalar a extensão **WSL** no VSCode para acessar pastas Linux.

**Uso básico**
-   **Abrir pastas**
-   **Explorador de arquivos**
-   Criar, mover, editar e deletar arquivos
-   Terminal integrado (`Ctrl + ``)


----------

### 7. Funcionalidades Git no VSCode

#### A aba Source Control mostra:
-   Arquivos modificados (**Changes**)
-   Arquivos prontos para commit (**Staged Changes**)

**Diferenças exibidas visualmente:**
-   Igual ao `git diff`
-   Mostra linhas adicionadas e removidas

**Ações disponíveis:**
-   **Adicionar ao Index** (ícone de +)
-   **Remover do Index** (ícone de -)
-   **Commit** com mensagem
-   **Commit (Amend)** para remendar último commit
-   Visualizar **versões antigas** (Timeline)

----------

### 8. Extensão GitLens

>O **GitLens** expande enormemente as funcionalidades Git no VSCode.

**Funcionalidades principais**
-   **Blame annotations:** mostra autor, data e commit de cada linha
-   **Commit Graph:** histórico visual dos commits
-   **Comparação avançada de versões**
-   **Exibição detalhada do commit**
-   **Exploração de repositório** sem usar terminal

*Permite visualizar:*
-   Arquivos modificados
-   Diff entre versões
-   Conteúdo completo do arquivo em commits anteriores
