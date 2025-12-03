|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 02 - Branches e Merge
### 1. Introdução ao Uso de Branches

>O Git permite manter versões diferentes de um projeto ao mesmo tempo. Isso é útil, por exemplo, quando se deseja testar múltiplas ideias sem comprometer a versão principal.   A funcionalidade central para isso é a **branch**, que representa uma linha de desenvolvimento independente.

----------

### 2. O que é uma Branch
-   Uma **branch** é um _marcador que aponta para um commit_.
-   A branch padrão criada pelo Git é chamada **master** (ou _main_, em projetos mais recentes).
-   Enquanto uma **tag** é fixa, uma branch **avança conforme novos commits são feitos**.
-   É possível criar quantas branches forem necessárias, com nomes arbitrários.

----------
### 3. Como as Branches São Utilizadas

**Branch master (main)**
-   Representa a **versão de produção**.
-   Alterações nessa branch devem estar testadas e estáveis.
-   Em cenários de publicação automática, o commit apontado por *master* é o distribuído ao público.

**Outras Branches**
-   São usadas para desenvolver **rascunhos**, **novos recursos**, **correções** ou **experimentos**.
-   Não devem afetar diretamente a versão de produção.

----------
### 4. Criando e Gerenciando Branches

**Comando git branch**

 - Cria um novo marcador sobre o commit atual:
`git branch nome-da-branch` 

 **Criando uma Branch em Outro Commit**
`git branch nova-branch <hash>` 

**Atalho para criar e trocar imediatamente**
`git checkout -b nova-branch` 

----------

### 5. O Papel da HEAD
-   **HEAD** indica **qual branch está atualmente selecionada**.
-   Ao fazer um commit, **a branch selecionada pela HEAD avança**.
-   Trocar de branch = mudar a HEAD para outro marcador.

----------

### 6. Git Checkout
**Trocar de branch**
`git checkout nome-da-branch` 
-   Move a HEAD para outra branch.
-   Atualiza a *Working Tree* para refletir o conteúdo do commit de destino.
-   Se houver modificações locais incompatíveis, o checkout pode falhar.
    
**Regras importantes**
-   Modificações locais **não são apagadas** caso sejam mantidas sem conflito.
-   Quando há conflito potencial, o checkout é cancelado para evitar perdas.
    
----------

### 7. Criando Versões Independentes
O processo apresentado no PDF usa o exemplo de escrever um guia com duas versões:
-   **long-exposure**
-   **high-iso**
O fluxo é:
1.  Criar branch.
2.  Trocar para ela com `checkout`.
3.  Modificar arquivos.
4.  Realizar commits na nova linha de desenvolvimento.

----------

### 8. Git Commit e Evolução das Branches
-   Commits feitos na branch selecionada avançam somente esse marcador.
-   Outras branches permanecem fixas nos seus commits originais.

----------

### 9. Visualização de Histórico
-   `git log --all` exibe todo o histórico, mesmo de branches distintas.
-   `git log --graph` mostra a ramificação visual.

----------

### 10. Git Merge
>Merge é a operação que **une o trabalho de uma branch na outra**.

**Merge Fast-Forward**
*Ocorre quando:*
-   A branch de destino está _atrás_ da branch de origem numa linha reta de commits.
*Resultado:*
-   Apenas **move a branch de destino para frente**, sem criar um commit de merge.
    
**Merge Three-Way**
*É necessário quando:*
-   As branches divergiram, ou seja, têm commits diferentes após o ponto comum.

*Resultado:*
-   O Git cria um **novo commit de merge**, combinando conteúdos das duas branches.
-   Usa três pontos de referência:
    -   Commit da branch A
    -   Commit da branch B
    -   Último commit ancestral comum

----------
### 11. Conflitos de Merge
**Quando ocorrem**
*Um conflito aparece quando:*
-   Dois commits alteram **as mesmas linhas** de um arquivo de formas diferentes.

**Identificação do conflito**
*No arquivo afetado surgem marcadores:*
*<<<<<<< HEAD*
*(conteúdo da branch atual)*
*=======*
*(conteúdo da outra branch)*
*>>>>>nome-da-branch*
**Resolução**
O desenvolvedor deve:
1.  Editar manualmente o arquivo.
2.  Remover marcadores.
3.  Ajustar o conteúdo final.
4.  Executar `git add`.
5.  Criar o commit de merge.
    
----------

### 12. Deletando Branches
-   Após o merge, uma branch pode ser removida:
`git branch -d nome-da-branch` 
-   **Não deletar** se ela for o _único marcador_ apontando para um commit de ponta.

----------

### 13. Solução de Problemas Comuns
**Git checkout falhou por causa de modificações locais**
Usar **git stash**:
`git stash
git checkout outra-branch` 
Para recuperar depois:
`git stash apply` 

 **Iniciei um merge, deu conflito e não quero resolver agora**
`git merge  --abort` 

 **Fiz um merge e quero desfazer o commit de merge**
*Usar:*
`git reset  --hard <commit-destino>` 
<font color="red">Cuidado: apaga a Working Tree. </font>
**Commit feito na branch errada**
Solução:
1.  Fast-forward na branch correta.
2.  Reset da branch errada para o commit anterior.
**Quero desfazer o commit, mas manter as modificações**
*Usar:*
`git reset  --mixed <hash>` 
Mantém alterações na Working Tree sem perder trabalho.
----------
### 14. Diferentes Modos do Git Reset
-   **--hard**: Move branch e reseta a Working Tree (perigoso).
-   **--mixed**: Move branch e _não_ altera a Working Tree.
-   **--keep**: Tenta preservar modificações locais; aborta se não for seguro.
-   **--soft**: Move a branch e mantém tudo no _staging_.
-   Variante `git reset HEAD <arquivo>` serve para desfazer um `git add`.
