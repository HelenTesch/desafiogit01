|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

 ## 👩‍💻Aula 09 - Segurança na Web

### 1. Introdução à Segurança na Web

>&nbsp;&nbsp;&nbsp;&nbsp; A segurança na web evoluiu conforme a internet passou a transmitir informações cada vez mais sensíveis. 

**Evolução do HTTP para HTTPS**

-   **HTTP:** transmite dados em texto simples, permitindo interceptações.
-   **HTTPS:** adiciona uma camada de segurança por meio da **criptografia SSL/TLS**.
-   O uso de **certificados digitais** garante a autenticidade do servidor.
-   O protocolo promove: **Confidencialidade**, **Integridade**, **Autenticação**.
 
**Vulnerabilidades do HTTP**

-   **Sniffing de pacotes:** interceptação e leitura de dados sensíveis.
-   **Man-in-the-Middle (MitM):** invasor altera ou monitora a comunicação.
-   **Falsificação de conteúdo:** injeção de scripts e manipulação de dados.
-   **Roubo de credenciais:** envio inseguro de senhas e dados pessoais.

----------

### 2. Mecanismos de Comunicação Segura (HTTPS)

**Criptografia de Dados:** O HTTPS utiliza criptografia para impedir que invasores compreendam informações interceptadas.  
Principais protocolos usados:
-   **SSL (Secure Sockets Layer)**
-   **TLS (Transport Layer Security)**

**Certificados Digitais:** Autenticam o servidor, sendo emitidos por uma **Autoridade Certificadora (CA)**.  Funcionam como credenciais confiáveis que asseguram a legitimidade do site.

**Garantias do HTTPS**
-   **Integridade:** uso de _MACs_ para verificar se o dado foi alterado.
-   **Confidencialidade:** algoritmos criptográficos protegem informações sensíveis.
-   **Proteção contra MitM:** dados cifrados dificultam interceptação e manipulação.
    
----------

###  3. SSL/TLS – Fundamentos da Criptografia no HTTPS

**Criptografia Simétrica e Assimétrica:** Esses protocolos combinam os dois tipos de criptografia.
- **Criptografia Simétrica:** Usa **uma chave única**, com alta performance para grandes volumes de dados.
- **Criptografia Assimétrica:** Utiliza um **par de chaves (pública e privada)**, assim permite **autenticação** e **troca segura de chaves**. Algoritmos comuns: **RSA**, **AES**.
 
#### **Handshake SSL/TLS**
Processo de estabelecimento da conexão segura (*garante autenticidade, confidencialidade e possibilidade de autenticar também o cliente*):
1.  **Início da comunicação** pelo cliente.
2.  **Envio do certificado** pelo servidor.
3.  **Autenticação do certificado** pelo cliente.
4.  **Acordo da chave de sessão** (criptografia assimétrica).
5.  **Criptografia da sessão** com chave simétrica.
----------

### 4. Autoridades Certificadoras (CAs) e Certificados

**Processo de Emissão**
-   **Escolha da CA** (ex.: _Let’s Encrypt, DigiCert_).
-   **Geração do par de chaves** no servidor.
-   **Validação de identidade** pelo CA.
-   **Emissão** do certificado digital.

 **Instalação e Renovação**
-   Configuração em servidores como _Apache_, _Nginx_ ou _IIS_.
-   Certificados possuem **validade limitada** (1 a 3 anos).
-   Renovação evita:
	-   Interrupção de serviços.
    -   Avisos de insegurança.
    -   Perda de confiança do usuário.
-   Automatização com ferramentas como **Certbot**.

**Consequências de Certificado Expirado**
-   Site pode se tornar inacessível.
-   Navegadores exibem alertas de segurança.
-   Riscos de ataques MitM.
-   Perda de credibilidade.
----------

### 5. Verificação de Certificados

**Cadeia de Confiança**
O navegador verifica (*se algo falhar, há alertas e bloqueios da conexão*):
-   O nome do domínio.
-   A CA emissora.
-   A validade do certificado.

 **Proteção contra MitM**
Certificados garantem:
-   Criptografia dos dados.
-   Integridade contra modificações.
-   Autenticidade do servidor acessado.


----------

### 6. Criptografia de Dados na Web

#### **Conceitos Fundamentais**
-   **Cifra:** algoritmo matemático de cifrar/decifrar.
-   **Chave:** valor utilizado no processo criptográfico.
-   **Algoritmo:** conjunto estruturado de operações de cifragem.

**Objetivos da Criptografia:**
-   **Confidencialidade:** dados ilegíveis para terceiros.
-   **Integridade:** garantia de que não foram alterados.
-   **Autenticidade:** comprovação da origem do dado.
-   **Proteção contra MitM:** comunicação protegida.
-   **Privacidade do usuário:** segurança em transações e dados pessoais.

----------

### 7. Comparação: Criptografia Simétrica vs. Assimétrica

**Simétrica:** <font color="green"> **Vantagens:** rápida e eficiente. </font> <font color="red">**Desafio:** distribuição segura da chave. </font>
 **Assimétrica:** <font color="green">**Vantagens:** resolve o problema de distribuição de chaves. </font> <font color="red">**Desvantagem:** maior custo computacional. </font>
    
**Uso Combinado:** Protocolos como **TLS** utilizam, a chave assimétrica para estabelecer chave de sessão e a chave simétrica para transmissão dos dados (rápida e segura).
    

----------

### 8. Criptografia de Ponta a Ponta (E2E)

> **Características:** Apenas remetente e destinatário podem decifrar, nem mesmo o fornecedor do serviço consegue ler os dados.
    

**Limitações:**
-   Gestão e backup de chaves.
-   Maior uso de recursos.
-   Pode afetar a experiência do usuário.

**Casos de Uso**
-   **Aplicativos de mensagens** (ex.: WhatsApp).
-   **Transações financeiras**.
-   **Armazenamento em nuvem seguro**.


----------

### 9. Segurança na Web em Navegadores

**Indicadores Visuais**
-   **Cadeado** na barra de endereço.
-   **HTTPS** indicando conexão cifrada.
-   **Mensagens** como “Conexão Segura”.
-   Alertas de **site não seguro**.

**Certificados EV, DV e OV**

-  **DV (Domain Validation):** Verifica apenas propriedade do domínio. Processo rápido e automatizado.
- **OV (Organization Validation):** Verifica domínio e dados da empresa. Nível intermediário de segurança.
 - **EV (Extended Validation):**  Verificação rigorosa.  Exibe nome da empresa na barra de endereço.  Maior confiança ao usuário.
