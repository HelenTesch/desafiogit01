|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 04 - Serviços e Aplicações na Internet

### 1. Introdução aos Serviços Web

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Os serviços web, permitem integração entre sistemas, disponibilizam funcionalidades via Internet e fornecem aplicações de grande escala. 
 
### 2. APIs e Integração de Sistemas

**O que são APIs:** Atuam como **intermediárias** entre componentes de software, permitindo:
-   compartilhamento de dados,
-   execução de funcionalidades,
-   interoperabilidade entre sistemas.
>Elas especificam *quais solicitações podem ser feitas*, *quais mensagens devem ser enviadas* e *como as respostas são estruturadas*.

#### Como Funcionam

**Solicitações e Respostas:** Opera, por meio de:
-   **Requests (solicitações):** o aplicativo cliente define a ação desejada.
-   **Responses (respostas):** a API retorna dados ou confirmações.

**Padrões e Formatos:** Utilizam formatos padronizados, como:
-   **JSON (JavaScript Object Notation)**
-   **XML (Extensible Markup Language)**
----------

### 3. Web Services e Protocolos (SOAP e REST)

**O que são Web Services:** Serviços baseados na web que fornecem funcionalidades e permitem troca de dados entre sistemas por meio de protocolos padronizados.

#### Protocolo SOAP (Simple Object Access Protocol)
**Características:**
-   Baseado exclusivamente em **XML**.
-   Estrutura rígida e padronizada para mensagens.
-   Inclui solicitações e respostas com forte formalismo.

<font color="GREEN"> **Vantagens:** Segurança robusta (WS-Security); Suporte a transações e alta confiabilidade;  Indicado para ambientes corporativos complexos. </font>

 **Aplicações:** Sistemas de gestão empresarial; Ambientes que exigem comunicação segura e controlada; Integrações críticas e de grande porte.

#### Protocolo REST (Representational State Transfer)
**Características:**
-   Arquitetura mais leve e flexível.
-   Usa diretamente os métodos HTTP: **GET, POST, PUT, DELETE**.
-   Baseia-se na manipulação de _recursos_ identificados por URLs.
    
<font color="GREEN">**Vantagens:** Alta escalabilidade; Simplicidade de implementação; Acessível e amplamente suportado pela web. </font>
 **Aplicações:** APIs públicas; Redes sociais; Aplicativos móveis e IoT.
    
**Comparação entre SOAP e REST**
| SOAP     | Critério| REST    |
| :---        |    :----   |          :--- |
| Estrutura rígida e complexa      | **Complexidade**      | Mais simples e flexível |
| Mais lento (XML pesado)   | **Desempenho**        | Mais rápido (HTTP nativo)      |
| Segurança integrada  | **Segurança**     | Depende de HTTPS, tokens etc.      |
| Mais lento (XML pesado)   | **Desempenho**        | Mais rápido (HTTP nativo)      |

----------

### 4. Arquitetura de Microsserviços

**O que são Microsserviços**
São pequenos serviços autônomos, cada um responsável por **uma única função** da aplicação.  Cada serviço pode ser desenvolvido, implantado e escalado de forma **independente**.
 **Principais Características:**
-   **Desacoplamento** 
-   **Independência tecnológica** 
-   **Escalabilidade isolada** 
-   **Manutenção simplificada**
-   **Implantação contínua** 
-   **Resiliência** 
    
<font color="GREEN"> **Vantagens:** Maior agilidade e flexibilidade; Escalabilidade otimizada; Facilidade de manutenção; Maior tolerância a falhas.</font>

<font color="red">**Desafios:** **Comunicação complexa** entre serviços; Necessidade de **orquestração** (ex.: Kubernetes); Monitoramento e testes mais sofisticados.</font>

>Os microsserviços geralmente se comunicam via **APIs REST**, reforçando a importância dos padrões abordados anteriormente.

----------

### 5. Aplicativos Web Interativos (Web 2.0)

A **Web 2.0** transformou a Internet, tornando aplicações mais dinâmicas, colaborativas e interativas.

#### Tecnologias-chave

**AJAX (Asynchronous JavaScript and XML):** Permite comunicação assíncrona entre cliente e servidor **sem recarregar a página**, proporcionando:
-   interfaces mais rápidas,
-   maior fluidez,
-   melhor experiência do usuário.

**Redes Sociais:** Permitem interação, compartilhamento e colaboração em tempo real.
**Wikis:** Permitem construção colaborativa de conteúdo (ex.: Wikipedia).
**Ferramentas de Produtividade Online:** Permitem edição colaborativa em tempo real.

<font color="GREEN">**Benefícios da Web 2.0:**  Experiência do usuário aprimorada; Colaboração em tempo real; Compartilhamento facilitado de conteúdo; Acesso via dispositivos móveis. </font>

----------

### 6. Autenticação e Segurança em Serviços Web

**Requisitos de Segurança**
-   **Confidencialidade:**  proteção contra acesso não autorizado.
-   **Integridade:**  garantia de que os dados não são alterados indevidamente.
-   **Autenticidade:**  verificação da identidade do usuário.
-   **Autorização:**  acesso apenas a recursos permitidos.

**Técnicas de Autenticação**

- **OAuth:** Protocolo de autorização que permite login via terceiros (Google, Facebook etc.) **sem expor credenciais**.
- **Token de Acesso:** Permitem autenticação contínua sem revalidar credenciais a cada requisição. **JWT (JSON Web Token)**.  

**Boas Práticas de Segurança**
-   **Criptografia SSL/TLS**
-   **Validação de dados de entrada** (prevenção de SQL Injection e XSS)
-   **Proteções contra ameaças comuns** (DDoS, firewall de aplicação)
-   **Gerenciamento de identidade**
-   **Logs e monitoramento de atividades**
