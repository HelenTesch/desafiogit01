|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 04 - Pull Request
### 1. Introdução ao Pull Request

>O *Pull Request* (PR) é um recurso oferecido por plataformas como o **GitHub**, que melhora o fluxo de trabalho colaborativo ao permitir que alterações desenvolvidas em uma branch sejam revisadas e integradas a outra branch de forma organizada, comunicativa e segura.

**Problema do fluxo manual de merge**
*No fluxo tradicional:*
-   O responsável pelo merge precisa **baixar a branch**, realizar o merge localmente e fazer o push.
-   A comunicação exige ferramentas externas.
-   Há menos controle e segurança no versionamento.
    
**Solução com Pull Request**
*O PR centraliza o processo:*
-   O próprio colaborador solicita o merge no GitHub.
-   O revisor analisa as alterações diretamente na plataforma.
-   O merge ocorre **remotamente**, com mais controle e transparência.

----------

### 2. Benefícios do Pull Request
**Comunicação:**
-   Permite discussões e comentários diretamente no GitHub.
-   Facilita colaboração entre membros.
-   Elimina dependência de meios externos de comunicação.

**Organização:**
-   Possibilidade de exigir aprovações, revisões e testes antes do merge.
-   Ajuda na governança do projeto e na padronização do código.

**Automação:**
-   Integração com ferramentas como **GitHub Actions**.
-   Execução automática de testes, validações e outros processos.

----------

### 3. Fluxo de Trabalho com Pull Request

** Etapas:**
1.  Criar uma branch a partir da branch base.
2.  Implementar a tarefa na nova branch.
3.  Resolver eventuais conflitos.
4.  Publicar a branch no repositório remoto.
5.  Solicitar o Pull Request para a branch base.
    
 **Controle do Mantenedor**
-   O revisor (ex.: líder técnico) pode ser o único autorizado a aprovar ou rejeitar PRs.
-   Todos podem revisar e fornecer feedback.
    

----------

### 4. Criando um Pull Request no GitHub

**Passo a passo**
1.  Acessar *Pull Requests* no repositório.
2.  Clicar em **New Pull Request**.
3.  Selecionar a **branch base** e a **branch de origem**.
4.  Clicar em **Create Pull Request**.
5.  Inserir título e descrição.
6.  Escolher entre PR normal ou PR em rascunho *Draft Pull Request*).
    
**Identificação de Conflitos**
-   Se houver mensagem indicando **"no conflicts"**, o merge é direto.
-   Se houver **conflitos**, será necessária sua resolução antes da mesclagem.

----------

### 5. Diferenças (Diff): Comparação de Branches
**Visualização pelo GitHub**
-   A aba **Files Changed** exibe alterações:
    -   **Adições** em verde (+)
    -   **Remoções** em vermelho (-)
-   Possui filtros, conversas e configurações de visualização.

**Comparação via Git**

##### Comparação de dois pontos (A..B)
-   Compara diretamente os estados finais de duas referências.
-   Foca no estado da **branch base**.
-   Alterações podem parecer ambíguas se o branch base mudar.

##### Comparação de três pontos (A…B)
-   Mostra diferenças desde o **ancestral comum**.
-   Foca no que a branch do tópico está introduzindo.
-   É o método padrão utilizado pelo GitHub nos PRs.

----------
### 6. Review (Revisão)
**Objetivo da Revisão**
-   Permitir avaliação, comentários e aprovação de alterações antes do merge.
-   Garantir qualidade e conformidade com diretrizes do projeto.

**Tipos de Revisão**
-   **Comentário**: Observações gerais ou dúvidas.
-   **Aprovação**: Aceita as alterações e autoriza o merge.
-   **Solicitação de alterações**: Exige modificações antes do merge.

 **Solicitação de Revisão**
-   Pode ser destinada a uma pessoa específica ou equipe.
-   Revisores podem ser definidos automaticamente via **CODEOWNERS**.
-   Revisores podem ser re-solicitados após ajustes.

**Processo de Revisão**
1.  Abrir a PR.
2.  Acessar o modo de revisão.
3.  Comentar diretamente nas linhas ou trechos de código.
4.  Sugerir alterações específicas.
5.  Marcar arquivos como “visualizados”.
6.  Finalizar com **Submit Review**.

**Conversas (Conversations)**
-   Possibilidade de acompanhar discussões na linha do tempo do PR.
-   Conversas podem ser marcadas como **resolvidas**.
-   Ajuda a organizar feedbacks pendentes ou concluídos.

----------

### 7. Conflitos
**O que são Conflitos**
>Ocorrem quando duas branches alteram o mesmo arquivo no mesmo trecho, assim o Git não consegue determinar automaticamente qual versão é a correta.
    
**Processo de Resolução**
1.  Acessar a branch da PR:
    `git checkout nomedabranchcomatualizações` 
2.  Integrar a branch base:
    `git merge main` 
3.  Resolver conflitos manualmente.
4.  Realizar push das correções:
    `git push` 
    
**Como Evitar Conflitos**
-   Cada colaborador trabalhar em arquivos distintos.
-   Cada feature ter sua própria branch.
-   Em projetos com mais de um colaborador por feature:
    -   Ter uma branch principal da feature.
    -   Cada dev criar sua sub-branch e abrir PR para a branch principal da feature.

----------

### 8. Finalizando um Pull Request
 **Processo de Merge**
1.  Abrir a PR.
2.  Ir até a área de merge.
3.  Clicar em **Merge Pull Request**.
4.  Confirmar o merge.

 **Após o Merge**
*Duas opções:*
   -   **Apagar a branch**: mantém o repositório limpo.
    -   **Manter a branch**: útil como backup até o lançamento da release.

 **Atualização local:**
*Após o merge:*
`git checkout main
git pull`
