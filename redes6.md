|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

 ## 👩‍💻Aula 06 - Arquitetura da Internet

### 1. Introdução à Arquitetura da Internet

O funcionamento da **Internet**  baseia-se em uma **arquitetura descentralizada**, isto é, não há uma única entidade controlando toda a rede. Em vez disso, diversos atores como **ISPs**, **backbones** e **Pontos de Troca de Tráfego (IXPs)** colaboram para garantir conectividade mundial.

> A Internet funciona como uma verdadeira **rede de redes**, integrada por estruturas robustas que permitem a circulação eficiente de dados entre diferentes regiões do planeta.

----------

### 2. Backbones da Internet

#### **Conceito e Função**
Os **backbones** constituem a *espinha dorsal* da Internet. São redes de **alta capacidade**, formadas principalmente por **cabos de fibra óptica**, **roteadores avançados** e infraestruturas de grande porte. Operam como rotas principais que transportam grandes volumes de dados entre países, continentes e ISPs.

**Características principais:**
-   Altíssima capacidade de transmissão.
-   Utilização de equipamentos de última geração.
-   Estabelecimento de rotas intercontinentais para garantir comunicação global.
    

**Principais Backbones Mundiais**
Entre os backbones globais mais relevantes estão:
-   **Level 3 Communications (CenturyLink)**: presença global abrangente.
-   **AT&T**: grande operadora com backbone em múltiplas regiões.
-   **NTT Communications**: forte atuação na Ásia, Europa e América.
-   **TATA Communications**: extensa malha intercontinental.
-   **Globenet**: destaque na América Latina.
-   **Embratel (Brasil)**: importante backbone brasileiro, subsidiária da Claro.
   
----------

### 3. Latência de Rede

>A **latência** é o _atraso_ entre o envio e o recebimento de dados em uma rede. 

**Fatores que influenciam:**
-   Distância física.
-   Congestionamento.
-   Qualidade das rotas e equipamentos.
-   Número de “saltos” entre roteadores.

----------

### 4. Problemas e Soluções nos Backbones

**Problemas Comuns**
-   **Congestionamento**: excesso de tráfego que excede a capacidade da infraestrutura.
-   **Falhas de hardware**: defeitos em roteadores, fibras ou equipamentos intermediários.
-   **Ataques cibernéticos**: especialmente **DDoS**, invasões e manipulação de dados.
-   **Roteamento subótimo**: rotas inadequadas podem aumentar latência.
-   **Monitoramento insuficiente**: dificulta a detecção de anomalias em tempo real.

**4.2 Soluções Adotadas**
-   Expansão de infraestrutura e otimização de rotas.
-   Implementação de **redundância** (rotas alternativas).
-   Firewalls, IDS e análise de tráfego para segurança.
-   Colaboração com **IXPs** para reduzir latência e otimizar tráfego.
-   Sistemas avançados de monitoramento e automação.
    
----------

### 5. Pontos de Troca de Tráfego (IXPs)

**Função dos IXPs**

>Os **IXPs** são instalações físicas onde diversas redes (ISPs, empresas, provedores de conteúdo) se conectam para trocar tráfego **localmente**. Isso reduz rotas longas e diminui significativamente a latência.

**Funcionamento:** Realizam a conexão direta entre redes por meio de roteadores e switches, fazendo acordos de **peering**, o que permite a troca recíproca de tráfego. Apresenta o princípio de **neutralidade**, garantindo equidade a todos os participantes.
    
<font color="green">**Impactos Positivos** </font>

-   **Redução de latência**.
-   **Alívio dos backbones**.
-   **Mais resiliência** via múltiplos IXPs regionais.
-   **Estímulo à inovação** e competitividade no mercado.

----------

### 6. Desafios de Segurança na Internet

**Principais Ameaças**
-   **Malware** (vírus, worms, trojans, spyware, adware).
-   **Ransomware**: criptografa dados e exige resgate.
-   **Phishing**: tentativa de enganar usuários para roubar informações.
-   **Ataques DDoS**: sobrecarga de serviços por tráfego malicioso.
-   **BGP Hijacking**: sequestro de rota via manipulação de informações de roteamento.
-   **Vulnerabilidades em dispositivos IoT**.
    
**Engenharia Social:** Técnicas que exploram o fator humano, como:
-   **Phishing**
-   **Pretexting**
-   **Tailgating**
-   **Quid pro quo**
    
**Estratégias de Mitigação**
-   Firewalls, filtros e IDS.
-   Criptografia (ex.: **TLS/SSL**).
-   Controle de acesso rigoroso.
-   Filtragem de tráfego em IXPs.
-   Segurança física em centros de dados.

----------

### 7. Gerenciamento de Tráfego e Qualidade de Serviço (QoS)
**Gerenciamento de Tráfego:** Inclui práticas para garantir eficiência e estabilidade da rede.
-   **Balanceamento de carga**.
-   **Priorização de tráfego** (ex.: voz e vídeo).
-   **Roteamento inteligente** para reduzir latência.
    
**QoS (Quality of Service):** Conjunto de técnicas para assegurar desempenho e qualidade.
-   Reserva de largura de banda.
-   Minimização de latência e _jitter_.
-   Garantia de disponibilidade mesmo em alta demanda.

<font color="red">Desafios incluem custo, complexidade crescente e adaptação a novas tecnologias. </font>

----------

### 8. IPv4, IPv6 e Escassez de Endereços


| **IPv4**     | **IPv6** | 
| :---        |    :----   | 
| Endereços de **32 bits**.     | Endereços de **128 bits**.
| Aproximadamente **4,3 bilhões** de endereços.   | Quantidade virtualmente ilimitada.     | 
|**Escassez** devido à massificação da Internet e dispositivos conectados.| Melhorias de segurança e eficiência.
    
 **Transição:** É gradual e envolve coexistência entre IPv4 e IPv6 durante a adoção.

----------

### 9. Roteadores e Encaminhamento de Dados

**Papel dos Roteadores:**
-   Interconectar redes diferentes.
-   Escolher o *melhor caminho* para cada pacote.
-   Garantir eficiência, confiabilidade e segurança na transmissão.

**Componentes e Funcionalidades**
-   **Interfaces de rede** (Ethernet, fibra, Wi-Fi).
-   **Tabelas de roteamento** atualizadas dinamicamente.
-   **Protocolos de roteamento** (OSPF, BGP, RIP, EIGRP).
-   **Firewall**, **NAT** e **QoS** integrados.
-   Firmware e software de gerenciamento.

**Tomada de Decisão de Roteamento** (*Baseada nos dados dos cabeçalhos dos pacotes*)
-   Endereço IP de origem.
-   Endereço IP de destino.
-   TTL, portas e protocolo.

>Com isso, define-se o **próximo salto (next hop)** até o destino final.

**Algoritmos e Construção das Tabelas**
Processo envolve:
-   Coleta de informações de roteamento.
-   Cálculo das melhores rotas.
-   Atualização contínua da tabela.
-   Uso de métricas como custo, latência e largura de banda.
