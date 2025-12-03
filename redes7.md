|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

 ## 👩‍💻Aula 07 - Redes de Computadores

### 1. Introdução às Redes de Computadores

&nbsp;&nbsp;&nbsp;&nbsp; O estudo das redes envolve sua **classificação por abrangência geográfica**, **protocolos**, **arquiteturas**, **dispositivos** e **tecnologias de comunicação**.

----------

### 2. Classificação das Redes por Abrangência Geográfica
**Redes de Área Pessoal (PAN):**
 - **Características:** Comunicação entre dispositivos de uso individual, possui alcance de poucos metros.
 - **Aplicações:** **Bluetooth**: conexão entre fones, teclados, smartphones e **NFC**: pagamentos móveis e emparelhamentos rápidos.

**Redes de Área Local (LAN):**
 - **Características:** **Alta velocidade** e **baixa latência**, cobrem distâncias de alguns metros a alguns quilômetros, utiliza de **switches**, **roteadores**, **APs** e outros dispositivos locais.
 - **Aplicações:** Redes domésticas com PCs, smartphones e dispositivos IoT, Escritórios compartilhando impressoras, arquivos e serviços internos, casas, escritórios e campi.
  
  **Redes  de Área Metropolitana(MAN):**
 - **Características:** Alcance típico de **dezenas de quilômetros** , interconectam várias LANs dentro de uma mesma cidade, são menos abrangentes que WANs, mais extensas que LANs.
 - **Aplicações:** Operadoras oferecendo Internet urbana e empresas com múltiplas unidades em uma mesma região.   

**Redes  de Longa Distância (WAN):**
 - **Características:** Latência maior que LAN, devido à distância elevada, possui infraestrutura mais complexa (linhas alugadas, fibra, satélite), suportam conexões globais (rede de longa distância cidades, estados, países e continentes)– base da **Internet**.
 - **Aplicações:** Corporações multinacionais conectando filiais e provedores de Internet oferecendo acesso a diferentes localidades.

#### Comparação entre LAN, MAN, WAN e PAN
|Tipo | Alcance| Velocidade | Exemplo de uso   |
| :---:        | :---        |    :----   |          :--- |
|**PAN**| Centímetros a metros      | Média      | Bluetooth, NFC   |
|**LAN**| Metros a quilômetros   | Alta       | Casas, escritórios, campi      |
|**MAN**|Vários km|Alta|Cidades|
|**WAN**|Centenas a milhares de km|Variável|Internet, multinacionais|
----------

### 4. Protocolos Utilizados em Redes (WAN, MAN, PAN)
**Protocolos de WAN**

-   **IP (IPv4/IPv6):** roteamento de pacotes na Internet.
-   **BGP:** troca de rotas entre sistemas autônomos.
-   **MPLS:** encaminhamento por rótulos, alta eficiência.
-   **Frame Relay / ATM:** tecnologias legadas ainda existentes.
-   **PPP / PPPoE:** conexões ponto a ponto e autenticação.
-   **VPN (IPsec, SSL/TLS, L2TP, PPTP):** túneis seguros.
-   **TCP e UDP:** protocolos de transporte fundamentais.


**Protocolos de MAN**

-   **Metro Ethernet:** Ethernet em escala metropolitana.
-   **ATM:** transmissão de dados, voz e vídeo.
-   **SONET/SDH:** padrões ópticos de alta capacidade.
-   **RPR:** eficiente em topologias de anel óptico.
-   **MPLS e EoMPLS:** gerenciamento avançado e serviços de QoS.

**Protocolos de PAN**

-   **Bluetooth:** comunicação pessoal de curto alcance.
-   **NFC:** aproximação física para troca de dados.
-   **Zigbee:** automação de baixa potência.
-   **Wireless USB:** USB sem fio de alta velocidade.
-   **IrDA:** transmissão por infravermelho (legado).

----------

### 5. Dispositivos de Redes

 - **Switches:** Operam na **camada de enlace**, responsáveis por encaminhar dados com base no **endereço MAC**. Reduzem colisões e
   aumentam a eficiência.
 - **Roteadores:** Operam na **camada de rede**, responsáveis por encaminhar pacotes entre redes distintas usando **endereços IP**. Podem implementar **NAT**, firewall e outras funções.
 - **Hubs:** Dispositivos simples da **camada física**, responsáveis por enviar dados para **todos os dispositivos** (ineficientes). Largamente substituídos por switches.
 - **Access Points (APs):** Permitem conexões Wi-Fi em uma LAN, responsáveis por ampliar a cobertura e conectar dispositivos móveis.
 - **Firewalls:** Podem ser físicos ou integrados a roteadores, responsáveis por filtrar o tráfego com base em regras de segurança.
 - **Servidores:** Armazenamento, impressão, aplicativos, autenticação.**DHCP:** distribui IPs automaticamente.
 - **Modems:** Utilizam tecnologias como cabo, fibra ou DSL, responsáveis por converter sinais digitais/analógicos para acesso à
   Internet.

----------

### 6. Arquiteturas de LAN

 - **Ethernet:** Arquitetura mais utilizada no mundo, opera em topologia de **barramento** ou **estrela**. Seus métodos de acesso são:
   **CSMA/CD** (antigo) e **CSMA/CA** (moderno).  Suporta velocidades de **10 Mbps a 100 Gbps**.
 - **Token Ring:** Topologia em **anel**, sua transmissão é por **token**, garantindo ausência de colisões.     
 - **FDDI:** Anel duplo em **fibra óptica**, com redundância. Velocidade de 100 Mbps.
- **ARCnet:** Topologia de barramento, simples e barata. Popular no passado, menor desempenho.
- **WLAN (Wi-Fi):** Ethernet sem fio baseada em **IEEE 802.11**. Amplamente usada em residências e empresas.Frequências: **2,4 GHz** e **5 GHz**.
- **Powerline LAN:** Usa a rede elétrica para transmitir dados. Útil onde cabos Ethernet não podem ser instalados.
----------

### 7. Tecnologias de Interconexão em WANs

- **Linhas Alugadas:** Conexões ponto a ponto dedicadas (T1, T3, fibra). Largura de banda garantida.
- **VPN:** Usa a Internet para criar túneis criptografados.  Solução econômica e segura para acesso remoto.
- **MPLS:** Encaminhamento eficiente baseado em rótulos. Oferece **QoS**, segurança e segmentação de tráfego.
- **SD-WAN:** Gerenciamento inteligente via software. Combina vários tipos de conexão (VPN, banda larga, MPLS). Reduz custos e aumenta flexibilidade.
- **Redes Privadas Dedicadas:** Conexões exclusivas entre filiais. Alta segurança e controle total.
- **Redes de Pacotes:** Incluem **Frame Relay**, **ATM** e **X.25** (legados). Parcialmente substituídas por tecnologias modernas. 

----------

### 8. Protocolos Wi-Fi (IEEE 802.11)

**Principais Padrões**
-   **802.11b** – até 11 Mbps
-   **802.11a/g** – até 54 Mbps
-   **802.11n (Wi-Fi 4)** – >100 Mbps, MIMO
-   **802.11ac (Wi-Fi 5)** – vários Gbps
-   **802.11ax (Wi-Fi 6)** – maior capacidade e eficiência

 **Segurança Wi-Fi**
-   **WPA/WPA2:** baseados em TKIP e AES.
-   **WPA3:** padrão atual, mais seguro.
-   **802.11i:** estrutura de segurança.
-   **Wi-Fi Direct:** comunicação direta entre dispositivos.

----------

### 9. Boas Práticas de Segurança em Redes Wi-Fi

-   Uso de **criptografia WPA3** (ou WPA2).
-   Senhas fortes e complexas.
-   Ocultação de SSID.
-   Filtragem de **endereços MAC**.
-   Atualização frequente de firmware.
-   Desativação de serviços não utilizados (como WPS).
-   Monitoramento constante de tráfego.
-   Uso de **VLANs** para segmentação.
-   Utilização de **VPN** em redes públicas.
-   Autenticação forte (ex.: EAP).

----------

### 10. Redes Celulares: 3G, 4G e 5G

- **3G:** Primeira geração com suporte real a dados móveis. Viabilizou videochamadas e Internet móvel básica.
- **4G (LTE):** Arquitetura totalmente baseada em pacotes. Suporte a streaming HD, jogos online e conexões rápidas.
- **5G:** Revolução na conectividade móvel. **Velocidades ultra rápidas**. **Latência extremamente baixa** (crítico para IoT e VR). **Maior capacidade** para milhões de dispositivos. Suporte a **network slicing**, adaptando a rede a diferentes aplicações. Impacto em áreas como automação industrial, carros autônomos e saúde.
