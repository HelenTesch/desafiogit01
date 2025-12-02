# 🌐Trilha: Introdução às Redes e à Internet
👨‍🏫 **Professor:** Kenji Taniguchi

<img src="profKenji.png" alt="prof Kenji" widght= "200" height= "300">

----------

## 👩‍💻Aula 01 - Conceitos fundamentais de redes de computadores


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

----------

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

----------
## 👩‍💻Aula 03: Endereçamento de IP, Sub-redes e Portas

### 1. Endereçamento IPv4

**Estrutura:** Utiliza **32 bits**, divididos em **4 octetos** decimais separados por pontos (ex.: `192.168.1.1`), Cada octeto varia de **0 a 255**, permitindo cerca de **4,3 bilhões** de endereços possíveis.

 **Componentes:**
-   **Endereço de Rede:** Identifica a rede à qual o dispositivo pertence.
-   **Endereço de Host:** Identifica o dispositivo dentro da rede.
-   **Máscara de Sub-rede:** Representada em 32 bits, define quantos bits pertencem à rede e quantos ao host.  
-   **Endereço de Broadcast:** Usado para enviar mensagens a **todos os dispositivos** da mesma rede.  
>Devido ao crescimento da Internet e dos dispositivos conectados, o IPv4 tornou-se insuficiente, gerando uma escassez do IPv4.  

----------

###  2. Endereçamento IPv6

**Estrutura:** O IPv6 utiliza **128 bits**, representados em formato **hexadecimal** e separados por dois-pontos:
 **Princípios Estruturais:**
-   **64 primeiros bits**: identificam a rede.
-   **64 últimos bits**: identificam o dispositivo.
-   **Notação de compressão:** pode omitir zeros para simplificar endereços.  

**Vantagens:**
-   **Espaço praticamente ilimitado** para endereços.
-   **Segurança aprimorada**, com suporte nativo a IPsec.
-   **Configuração automática** de endereços (SLAAC).
-   **Suporte a QoS**, otimizando tráfego prioritário.
-   **Melhor desempenho** e eficiência.

----------

###  3. Máscaras de Sub-rede e Segmentação

**Máscara de Sub-rede:** Define quais bits representam **a rede** e **o host**.  Essencial para:
-   organizar endereços,
-   determinar redes e hosts,
-   identificar se dispositivos estão na mesma sub-rede.
    
 **Segmentação de Redes (Subnetting):** Divisão de uma rede em várias sub-redes menores. Suas vantagens são:
-   **Melhor desempenho:** tráfego local reduzido.
-   **Mais segurança:** isolamento entre segmentos.
-   **Controle de tráfego:** políticas específicas por sub-rede.
-   **Melhor organização** e gestão.
-   **Redução de conflitos de endereço.**

----------

### 5. Ferramentas de Análise de Rede

**Ping (Packet Internet Groper):** Testa **conectividade** e mede a **latência**.  Envia pacotes ICMP para verificar se o destino responde. Útil para:
-   Verificar disponibilidade de um dispositivo.
-   Analisar tempo de ida e volta (RTT).
-   Diagnosticar falhas básicas de rede.

**Traceroute:** Mapeia a rota percorrida pelos pacotes até o destino.  
Exibe cada salto intermediário no caminho. Útil para:
-   Identificar falhas no roteamento.
-   Analisar pontos de latência elevada.
-   Diagnosticar perda de pacotes.

**Identificação de Endereços IP:**
-   **ipconfig** (Windows) / **ifconfig** (Linux):  exibem o IP local e informações da interface de rede.
-   **Ferramentas online:** mostram o **IP público** do usuário.

----------

### 6. Portas, Firewalls e Direcionamento de Tráfego
**Portas de Rede:** Identifica um serviço ativo em um dispositivo. Cada dispositivo pode usar **várias portas simultaneamente**.

**Categorias**
-   **Portas Bem Conhecidas (0–1023):** Associadas a serviços padrão, como:
    -   Porta **80** → HTTP
    -   Porta **443** → HTTPS
    -   Porta **25** → SMTP
    -   Porta **53** → DNS
    -   Porta **22** → SSH
-   **Portas Registradas (1024–49151):** Utilizadas por aplicações registradas.
-   **Portas Dinâmicas/Privadas (49152–65535):** Usadas temporariamente por clientes.
----------

### 7. Firewalls

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Firewalls controlam, filtram e protegem ou redirecionam o tráfego de rede com base em regras, suas funções são:
-   **Filtragem de Pacotes:** Permite ou bloqueia tráfego conforme regras.
-   **NAT (Network Address Translation):**  Permite que vários dispositivos compartilhem um único IP público.
-   **Proxy:** Atuam como intermediários, fornecendo segurança adicional.
-   **Detecção de Intrusão:** Identifica tráfego suspeito ou malicioso.
-   **VPN:** Permitem conexões seguras entre redes remotas.

**Regras de Firewall:** Podem ser baseadas em IPs, portas, protocolos,  direções (entrada/saída).

----------

### 8. Bloqueio de Tráfego por ISPs
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISPs frequentemente bloqueiam portas por motivos como:
-   segurança da rede;
-   prevenção de ataques;
-   controle de tráfego;
-   políticas de uso.

----------

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

----------
