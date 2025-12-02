|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

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
