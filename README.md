🌐# Trilha: Introdução às Redes e à Internet
👨‍🏫 **Professor:** Kenji Taniguchi

<img src="profKenji.png" alt="prof Kenji" widght= "200" height= "300">

👩‍💻## Aula 01 - Conceitos fundamentais de redes de computadores


### 1. Introdução às Redes de Computadores
- permite que dispositivos se comuniquem de forma *eficiente*, *coordenada* e *confiável*;
- cria ambientes interconectado.
----------
### 2. Benefícios das Redes

- **Eficiência:** Permitem *compartilhamento otimizado de recursos*, reduzindo **custos** e aumentando a **produtividade**.
- **Conveniência:** Garantem *acesso instantâneo* a **informações** e **serviços**, independentemente da localização.
- **Escalabilidade:** A infraestrutura pode **crescer conforme a demanda**.
- **Redundância:** Implementam mecanismos de **backup e continuidade**.

----------

### 3. Definição e Importância das Redes de Computadores

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Uma **rede de computadores** é um sistema organizado de dispositivos interconectados que compartilham informações, serviços e recursos.  


#### Funções essenciais
-   Compartilhamento de Recursos 
-   Comunicação 
-   Acesso à Internet
-   Distribuição de Serviços
    
----------

### 4. Topologias de Rede

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A **topologia de rede** é a forma como os dispositivos estão organizados.

 **Topologia em Estrela:** Todos os dispositivos conectam-se a ==um **ponto central** (hub ou switch)==. <font color="green">  A falha de um dispositivo não afeta os demais, <font color="red">mas se o ponto central falha toda a rede.</font>
 
 **Topologia em Barramento:** Todos os dispositivos ==compartilham um **único cabo**==. <font color="green">  Simples e de baixo custo, <font color="red">mas a falha no cabo paralisa a comunicação, baixa escalabilidade.</font>
   
  **Topologia em Anel:**  Dispositivos conectados em um ==**ciclo fechado**== que circulam até alcançar o destino. <font color="green">  Possui fluxo eficiente, <font color="red">mas a falha em um ponto pode interromper toda a rede.</font>

**Topologia em Malha:** Cada dispositivo é ==interligado a todos== os outros. <font color="green">  Possui alta confiabilidade e redundância, <font color="red">mas possui custo mais elevado e complexidade de implementação.</font>

#### Impacto das Topologias na Comunicação

Redes pequenas **estrela** (simples e eficaz) **X** Grandes organizações  **malha** (alta disponibilidade).
<center>Topologias inadequadas comprometem desempenho, escalabilidade e resiliência.</center>
    

----------

### 5. Comunicação em Rede

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Define **como os dados são enviados, recebidos e interpretados** entre dispositivos.

#### Princípios Fundamentais

- **Emissor e Receptor:** O emissor envia dados; o receptor os recebe. Esses papéis podem alternar.
- **Dados:** A informação transmitida (texto, imagem, vídeo, arquivos, páginas web etc.).
- **Meio de Comunicação:** Caminho físico ou lógico percorrido pelos dados, ex: <font color="red">cabos, conexões sem fio, infraestrutura em nuvem.</font>
- **Protocolos:** Conjuntos de regras que padronizam a comunicação. Exemplo: <font color="red">**TCP/IP**</font>.  
>Os protocolos são como uma **linguagem comum**, garantindo interoperabilidade entre dispositivos de diferentes fabricantes.

----------

### 6. Escalabilidade em Redes

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A **escalabilidade** é a capacidade de uma rede **crescer sem perda de desempenho**. 

### Princípios de Escalabilidade

- **Arquitetura Planejada:** Escolha adequada de topologias, protocolos e equipamentos.
- **Redundância:** Componentes de backup para garantir continuidade.
- **Balanceamento de Carga:** Distribuição uniforme do tráfego para evitar gargalos.
- **Virtualização:** Criação de redes virtuais para uso inteligente dos recursos físicos.
- **Monitoramento e Gerenciamento:** Acompanhamento constante para detectar falhas e otimizar desempenho.

----------

### 7. História e Evolução da Internet

- **ARPANET (Década de 1960):**  Criada pelo Departamento de Defesa dos EUA para permitir comunicação entre cientistas e centros de pesquisa e resiliência em cenários de guerra.
- **Transição para o TCP/IP (Década de 1980):** O protocolo **TCP/IP** tornou-se o padrão da ARPANET e possibilitou a padronização da comunicação, expansão global da rede, comunicação eficiente entre dispositivos diferentes.
- **A Internet Comercial (Década de 1990):** Surgimento dos provedores de Internet (ISP) e comércio eletrônico.
<center>World Wide Web (WWW), criada por Tim Berners-Lee: uso de hipertextos e imagens em páginas web </center> 
    
- **Explosão da Internet e Web 2.0 (Anos 2000)**: Transição de páginas estáticas para plataformas dinâmicas e colaborativas. **Características:**
-   interatividade
-   conteúdos gerados por usuários
-   redes sociais
-   wikis
-   blogs e plataformas de publicação
-   interfaces mais limpas e responsivas  
   
 **UI (User Interface)** interface visual **-X-**  **UX (User Experience):** experiência e usabilidade.
    

### Web 3.0 – A Internet Semântica

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  A Web 3.0 propõe uma Internet mais inteligente, baseada em **Compreensão de significado (Web Semântica)**, **Inteligência Artificial**, **Interconexão Avançada**

👩‍💻## Aula 02 - Protocolos de comunicação em Redes

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
