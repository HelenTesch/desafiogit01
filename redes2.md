|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 02 - Protocolos de comunicação em Redes

### 1. Introdução aos Protocolos de Comunicação
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Os **protocolos de comunicação**  definem regras, formatos e procedimentos que permitem que dispositivos troquem dados de forma **organizada, eficiente e segura**.

----------
### 2. O que são Protocolos de Comunicação
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Um **protocolo de comunicação** é um conjunto de regras padronizadas que determinam como:
-   Mensagens devem ser formatadas;
-   Dispositivos iniciam, mantêm e finalizam a comunicação;
-   Erros são detectados e corrigidos;
-   Dados devem ser interpretados no destino.

----------

### 3. Tipos de Protocolos de Comunicação
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Os protocolos são classificados conforme sua função e camada de atuação. Os principais grupos são:
-   **Protocolos de Rede:** Atuam na **camada de rede**, gerenciando o encaminhamento de pacotes entre dispositivos, o mais utilizado é o **TCP/IP**, funções principais:
	- **Roteamento de dados:** melhor rota para o tráfego.
	-  **Endereçamento:** atribuição de endereços IP a cada dispositivo.
	- **Encapsulamento:** inclusão de cabeçalhos com informações de controle e identificação.
    
-   **Protocolos de Transporte:** Atuam na **camada de transporte**, garantindo a comunicação direta entre dispositivos finais, os principais são: 
	- **TCP (Transmission Control Protocol):** **Confiável**, garante **entrega ordenada**, verificação de erros e retransmissão.  
	- **UDP (User Datagram Protocol):** **Rápido**, porém **não confiável**, sem controle de conexão ou garantia de entrega.
    
-   **Protocolos de Aplicação:** Interação entre **aplicações e serviços na rede**. Principais exemplos: 
	-   **HTTP (Hypertext Transfer Protocol):** Páginas web.
	-  **SMTP (Simple Mail Transfer Protocol):** Envio de e-mails. 
	- **FTP (File Transfer Protocol):** Transferência de arquivos.  
----------

### 4. RFC – Request for Comments

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Documentos técnicos oficiais criados pela **IETF** (Internet Engineering Task Force), definem padrões, protocolos e procedimentos utilizados na Internet.
**Funções dos RFCs**

-   **Padronização:** Compatibilidade entre dispositivos e sistemas..
-   **Inovação:** Documentam novas tecnologias e avanços da Internet.
-   **Resolução de Problemas:** Abordam desafios técnicos e propõem soluções.
-   **Referência Autoritativa:** Fonte definitiva de consulta técnica.
----------
### 5. Estrutura de um Protocolo de Comunicação
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Os principais componentes são:

**Cabeçalhos (Headers):** Contêm informações de controle utilizadas para:
-   **endereçamento** (origem e destino);
-   **controle de fluxo**;
-   **identificação do protocolo**;
-   parâmetros de verificação e segurança.

**Mensagens:** Conteúdo principal transmitido entre dispositivos. Pode ser dividida em segmentos dependendo do protocolo.
**Campos de Dados:** Partes específicas das mensagens, contêm valores relevantes para o sistema receptor.  Seguem padrões definidos para assegurar consistência e entendimento.

----------

### 6. Técnicas que Garantem a Transmissão Correta
**Integridade de Dados:** Uso de verificação, detecção de erros e códigos de validação.   
**Sequenciamento:** Trabalha para que os dados cheguem na **ordem correta**.
**Confirmação e Retransmissão:** Pacotes perdidos podem ser reenviados (se for recusado pelo receptor).
 **Gerenciamento de Erros:** Permite correção ou retransmissão de pacotes danificados.
 
----------

### 7. Protocolos de Segurança na Comunicação Online

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **SSL/TLS – Criptografia e Segurança:** O conjunto de protocolos **SSL/TLS** (Secure Sockets Layer / Transport Layer Security) cria um canal seguro entre cliente e servidor, funções:
-   **Criptografia de Dados:** impede leitura por terceiros.
-   **Proteção da Privacidade:** dados pessoais ficam ocultos durante a transmissão.
-   **Autenticidade:** garante que o usuário está acessando o servidor legítimo.
-   **Integridade:** evita alterações nas informações enviadas.
-   **Defesa Contra Ataques:** especialmente contra interceptação e ataques de *man-in-the-middle*.
>Sites seguros exibem **HTTPS** e um cadeado na barra de endereço.

----------

### 8. Importância da Proteção de Informações Sensíveis
-   **Roubo de Identidade** 
-   **Segurança Financeira**
-   **Confidencialidade Empresarial** 
-   **Cumprimento Regulatório** 

----------

### 9. LGPD – Lei Geral de Proteção de Dados

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A **LGPD (Lei nº 13.709/2018)** regulamenta o tratamento de dados pessoais no Brasil.  Busca proteger a privacidade e garantir direitos aos cidadãos.

#### Objetivos e Princípios da LGPD
-   **Proteção da Privacidade e Integridade de Dados**
-   **Direitos dos Titulares** 
-   **Transparência** 
-   **Responsabilidade Empresarial** 
-   **Consentimento Informado**
-   **Sanções por Não Conformidade** 
-   **Alinhamento Internacional**
