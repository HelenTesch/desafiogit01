|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 03 - Repositório Remoto
### 1. Introdução ao Repositório Remoto

>O Git possibilita o **controle de versão** local, mas a colaboração entre múltiplas pessoas exige uma forma de compartilhamento. Para isso, existe o **repositório remoto**, uma cópia do projeto hospedada na internet que permite:
-   Compartilhar código;
-   Integrar contribuições de colaboradores;
-   Sincronizar versões entre vários computadores.

Ele funciona como **ponto central de sincronização** e também como **backup** do projeto.

----------

###  2. Conceito de Repositório Remoto
**O que é um Repositório Remoto**
>Um repositório remoto é uma **versão online do repositório Git**. O fluxo básico envolve:
1.  **Adicionar o link remoto** ao repositório local (`git remote add`);
2.  **Enviar (push)** a cópia local para o servidor;
3.  **Baixar (pull)** o projeto do remoto para máquinas diferentes.

**Remoto como Backup**
>Mesmo trabalhando sozinho, hospedar o projeto em um remoto mantém:
-   Todo o **histórico de commits**;
-   Branches e tags.

<center>A *Working Tree* e o *Index* não são enviados, mas podem ser reconstruídos. </center>

**Atualizações não são “ao vivo”**
*As modificações só aparecem:*
-   No remoto após um **git push**;
-   No local após um **git pull**.

>Os comandos normais do Git **não** se comunicam com a internet.

**Comandos importantes**
-   **git clone**
-   **git fetch**
-   **git push**
-   **git pull**

----------

###  3. Serviços de Hospedagem: GitHub, GitLab e Bitbucket
>Esses serviços **não são o Git**, mas plataformas que hospedam repositórios remotos.

**GitHub**
>Plataforma mais popular, oferecendo:
-   **Repositórios de código**;
-   **Colaboração** via _forks_ e _pull requests_;
-   **Revisão de código**;
-   **CI/CD**;
-   **GitHub Pages** para sites e documentação;
-   Forte **comunidade open source**.

----------

###  4. Configurando o GitHub e Enviando o Projeto Local
 **Criando uma conta**
-   Criar conta em *github.com*;
-   Utilizar autenticação segura;
-   Recomenda-se ativar **2FA (Autenticação de Dois Fatores)**.
    
**Criando um par de chaves SSH**
>O GitHub **não permite senha via terminal**, devendo-se usar SSH:
-   Criar chave com `ssh-keygen -t ed25519 -C "email"`;
-   A **chave privada** fica no computador;
-   A **chave pública** é adicionada ao GitHub;
-   Teste via `ssh -T git@github.com`.
    
**Criando um repositório remoto**
*Ao criar o repositório:*
-   Dar nome;
-   Escolher visibilidade (público ou privado);
-   Não adicionar README, .gitignore ou licença (para evitar commit extra).
    
**Público ou privado?**
*Depende de fatores como:*
-   Propriedade intelectual;
-   Conteúdo sensível;
-   Estágio de maturidade do projeto;
-   Necessidade de colaboração aberta.
    
**Adicionando o link remoto**
*Copiar a URL SSH e usar:*
`git remote add origin <url>
git remote -v` 

**Enviando o projeto: git push**
*Trocar branch principal para **main**:*
`git branch -m master main git push --set-upstream origin main` 

 **HTTPS x SSH**
-   HTTPS usa _Personal Access Token_;
-   SSH usa o par de chaves – **mais simples e recomendado**.

----------

###  5. Remote-Tracking Branch
*Após o primeiro push, surge uma **remote-tracking branch**, como:*
-   `origin/main`

>Ela representa **o estado atual do repositório remoto** e aparece com ícone diferente no GitLens.

*Existem dois tipos de branch:*
-   **Locais**
-   **Remote-tracking** (representações do remoto)

----------
###  6. Colaboração Independente
 **Clonando repositório**
*Colaboradores usam:*
`git clone <url>` 
>*git init + git remote add* não substitui o **clone**, pois não baixa o histórico.
>
**Fazendo mudanças locais**
*Cada colaborador cria suas próprias branches, faz commits e **só envia** ao remoto quando tiver permissão.*
 **Adicionando colaboradores**
*O dono do projeto concede permissão:*
-   *Settings*→ *Collaborators* → *Add people*.

 **Enviando mudanças**
*Primeiro push:*
`git push --set-upstream origin <branch>` 
*Depois:*
`git push` 
*Somente os novos commits são enviados.*

----------

###  7. Integração de Mudanças

**Baixando modificações: git fetch**
`git fetch` baixa:
-   Branches remotas;
-   Commits novos.
>Mas **não altera branches locais**.

**Merge local**
*Para integrar contribuições:*
`git checkout main git merge origin/<branch>` 
Depois, enviar ao remoto:
`git push` 

**Atualizando branch local**
*Colaborador executa:*
-   `git fetch` + `git merge origin/main`, ou
-   apenas `git pull`.

**Deletando branches**
*Local:*
`git branch -d <branch>` 
*Remoto:*
`git push -d origin <branch>` 

----------

###  8. Problemas Comuns

**Push falhou: non-fast-forward**
>Ocorre quando as branches **bifurcam**.  

<font color="red"> Push só funciona com linha reta. </font>
*Para sobrescrever:*
`git push --force` 
*Mas isso pode apagar commits remotos.*
*Causas comuns:*
-   Uso de `git commit --amend`;
-   Duas pessoas modificando a mesma branch sem sincronizar.
    
**Branch local divergiu da remota**
Não usar `--force`, e sim:
`git fetch
git checkout <branch>
git merge origin/<branch>` 
*Resolve preservando ambos os lados.*
**Conflito após git pull**
*O pull faz:*
1.  `git fetch`;
2.  `git merge`.
    
*Se houver conflitos, são resolvidos manualmente ou com:*
`git merge  --abort`
