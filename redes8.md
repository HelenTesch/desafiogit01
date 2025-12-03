|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

 ## 👩‍💻Aula 08 - Segurança de Redes

### 1. Introdução à Segurança de Redes

&nbsp;&nbsp;&nbsp;&nbsp; O objetivo principal da **segurança de redes** é  proteger a **integridade**, **confidencialidade** e **disponibilidade** das informações, prevenindo ataques, interrupções e acessos indevidos.

----------

### 2. Ameaças à Segurança de Redes

- **Malware:** Software malicioso criado para causar danos ou roubar informações.  Inclui: **vírus**, **worms**, **trojans**, **ransomware**.  
Propaga-se por **downloads**, **anexos** e **sites comprometidos**.
- **Ataques de Phishing:** Fraudes que tentam enganar o usuário para obter **informações sensíveis**, como senhas ou dados financeiros.  
Utilizam e-mails ou mensagens falsas com aparência legítima.
- **Ataques de Negação de Serviço (DoS):** Tornam um sistema indisponível ao sobrecarregar seus recursos com tráfego excessivo ou exploração de falhas.
- **Engenharia Social:** Manipulação psicológica para obter informações confidenciais.  Inclui **pretextos**, **intimidação** ou **manipulação emocional**.
- **Vulnerabilidades de Software:** Falhas em sistemas e aplicativos que podem ser exploradas por invasores. Exemplos: **patches desatualizados**, **configurações incorretas**, falhas de design.
- **Interceptação de Dados:** Captura indevida de dados durante a transmissão.  Exemplo: **sniffing** em redes inseguras.
- **Roubo de Identidade:** Uso indevido de dados pessoais para se passar pela vítima.
- **Backdoors e Exploits:** Métodos para contornar a autenticação ou explorar vulnerabilidades existentes.
- **Injeção de Código:** Inserção de código malicioso para alterar o funcionamento de aplicações.  Principais formas: **SQL Injection**, **XSS**.
- **Ameaças Internas (Insider Threats):** Ações maliciosas realizadas por usuários internos, como funcionários.

----------

### 3. Exploração de Vulnerabilidades e Impactos nas Redes

#### **Identificação e Exploração de Vulnerabilidades**

 - **Procedimentos de Varredura:** Uso de ferramentas automatizadas para localizar falhas.
 - **Análise de Código:** Revisão de código para identificar vulnerabilidades ocultas.
 - **Engenharia Social e Phishing:** Obtêm informações privilegiadas que facilitam explorações posteriores.
 - **Malware Camuflado:** Phishing como meio de entrega de malware que localizará novas vulnerabilidades.
 - **Exploração Zero-Day:** Ataques que utilizam falhas ainda desconhecidas publicamente.
 - **Ataques Baseados em Buffers:** Exploram erros de programação para sobrescrever áreas da memória.
 - **Injeção de Código:** Como **SQL Injection** e **XSS**, manipulando entradas do usuário.

#### **Impactos nas Operações da Rede**

 - **Interrupção de Serviços:** Afeta continuidade e desempenho das operações.
 - **Acesso Não Autorizado:** Compromete sistemas inteiros e dados sensíveis.
 - **Roubo de Dados:** Exfiltração de informações pessoais, financeiras ou estratégicas.
 - **Comprometimento da Integridade:** Alteração de dados, gerando informações falsas.
 - **Disseminação de Malware:** Propagação lateral, ampliando danos.
 - **Prejuízos Financeiros e Reputacionais:** Custos de recuperação, perda de confiança e danos à imagem da organização.

#### Medidas de Prevenção e Mitigação**

-   **Atualizações e Patches Regulares**
-   **Testes de Penetração**
-   **Conscientização de Usuários**
-   **Monitoramento Constante da Rede**

----------

### 4. Medidas de Segurança – Firewalls

>Atuam como barreiras de proteção, controlando o tráfego entre redes e garantindo segurança.
<center>Divisão entre **zona interna** (confiável) e **zona externa** (não confiável).</center>

#### **Tipos de Firewalls**

**Firewall de Pacotes** 
- **Características:** Baseado em **ACLs (Listas de Controle de Acesso)** **Stateless** (não mantém estado). Focado em eficiência e filtragem simples.
- **Tipos de Filtragem:** Analisa apenas cabeçalhos: **IP**, **portas**, **protocolos**.
- **Limitações:** Baixa capacidade de inspeção de conteúdo.  Não lida bem com ataques distribuídos e complexos.
- **Aplicações Práticas:**  Roteadores domésticos. Proteção básica a servidores. Controle de tráfego SSH. Bloqueio de portas e protocolos específicos. Monitoramento e logging.

**Firewall de Estado (Stateful)**
- **Características:** Mantêm tabela sobre o **estado da conexão**. Decisões adaptativas. Inspeção contextual. Eficiência contra ataques de spoofing e DoS.
- **Benefícios:** Menos falsos positivos. Controle eficiente de conexões. Melhoria na segurança geral.
- **Limitações:** Maior uso de recursos. Configuração mais complexa.

**Firewall de Aplicação (Proxy)**
- **Características:** Inspeção profunda (**Deep Packet Inspection**). Controle por aplicação. Filtragem de conteúdo. Autenticação de usuários. Detalhamento em logs.
- **Benefícios:** Segurança avançada. Conformidade com políticas. Acesso granular. Melhor desempenho via cache.
- **Limitações:** Overhead de desempenho. Configuração mais complexa. Necessidade de hardware robusto.

**Firewalls de Próxima Geração (NGFW)**
- **Características:** IPS (Prevenção de Intrusões) integrado. Filtragem avançada. Detecção de malware. Controle granular de aplicações.  Integração com nuvem
- **Benefícios:** Proteção multifacetada. Atualizações dinâmicas. Conformidade melhorada. Análise e relatórios avançados.
- **Limitações:** Requisitos maiores de desempenho. Gerenciamento mais complexo. Integração com a infraestrutura existente
----------

### 5. Firewalls em Sistemas Operacionais

**Linux**
Principais soluções:
-   **Netfilter/Iptables**
-   **UFW**
-   **Firewalld**
-   **PF**
-   **Shorewall**
-   **Nftables**
-   **IPFire**
    

**Windows – Windows Defender Firewall**
Configurações:
-   Regras de entrada e saída
-   Políticas de grupo
-   Uso de PowerShell
-   Monitoramento via Visualizador de Eventos

----------

### 6. Medidas de Segurança – Antivírus

>**Importância:** Prevenção de infecções. Segurança em camadas. Proteção de dados.  Detecção em tempo real
    

**Características de um bom antivírus**
-   Banco de assinaturas atualizado
-   Heurística avançada
-   Varredura manual e programada
-   Baixo impacto no desempenho
    

**Estratégias de Detecção e Remoção**

-   Assinaturas
-   Heurística comportamental
-   Quarentena e remoção
-   Varreduras profundas
-   Atualizações automáticas

----------

### 11. Redes Privadas Virtuais (VPNs)

**Tipos de VPN**
-   **Acesso Remoto**
-   **Site-to-Site**
-   **L2VPN e L3VPN**  

**Elementos Principais**
-   **Túnel criptografado**
-   **Autenticação**
-   **Protocolos de criptografia** (IPsec, SSL/TLS, PPTP)
    
**Formas de Implementação**
-   Software VPN
-   Hardware dedicado
-   Serviços de VPN em nuvem

**Benefícios**
-   Segurança de dados
-   Acesso remoto seguro
-   Proteção em redes públicas
-   Flexibilidade e escalabilidade
-   Redução de custos
    
**Considerações Importantes**
-   Escolha adequada do protocolo
-   Políticas de segurança
-   Conformidade legal
-   Manutenção e atualizações
