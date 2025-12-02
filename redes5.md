|[Início](./README.md)| - |[Trilha: Introdução às Redes e à Internet](./trilha1.md)| - |[Trilha: Controle de Versão](./trilha1.md)|

## 👩‍💻Aula 05 - DNS (Domain Name System)

### 1. Introdução ao DNS

O **DNS (Domain Name System)** é um sistema que funciona como um **diretório de nomes da internet**, associa **nomes de domínio** a **endereços IP** numéricos, permitindo localizar sites, serviços e servidores de e-mail.  
>Traduz nomes como `www.exemplo.com` em endereços como `192.168.1.1`.
----------

### 2. Hierarquia de Domínios e Subdomínios

>**Nomes de Domínio:**
>-   Identificadores textuais usados para acessar recursos na internet.
>-   Organizados hierarquicamente em **rótulos separados por pontos**.

A estrutura DNS é hierárquica.
**TLD (Top-Level Domain):** Indicam categorias gerais de uso.
-   Extensões principais como **.com**, **.org**, **.net**, **.gov**, **.edu**.

**Subdomínios:** Extensões do domínio principal, permitem organizar serviços, regiões, departamentos etc.
 - Exemplo: `www.helenpages.com`
	  -   **www** = subdomínio
	  -   **helenpages** = domínio de segundo nível
	 - **com** = TLD (Top-Level Domain)

**Exemplos de Domínios**
-   Domínios globais: `google.com`, `facebook.com`.
-   Domínios geográficos: `google.co.uk`, `google.fr`.
-   Serviços: `mail.exemplo.com`, `blog.exemplo.com`.
-   IoT: `termostato.casainteligente.com`.
    

----------

### 3. Servidores DNS

**Servidores de Resolução (Recursivos):** 
- Recebem consultas dos clientes.
- Buscam as respostas na hierarquia DNS.
- Guardam resultados em **cache**.
 
 **Servidores Raiz**
-   Direcionam consultas para servidores dos TLDs.
 
 **Servidores Autoritativos:** 
 - Contêm registros DNS de um domínio.
-   Respondem sobre informações específicas do domínio.



    
----------

### 4. Consultas e Respostas DNS

**Funcionamento da Consulta**
-   O navegador envia o nome ao servidor recursivo.
    -   A consulta especifica:  **Nome do domínio**, **Tipo de registro (A, MX etc.)** e   Outros metadados.

**Processo de Resposta**
-   O servidor recursivo consulta servidores autoritativos.
-   As respostas incluem:   **Endereço IP**,  **TTL (Time to Live)**.

<font color="red">**Redirecionamento:** Caso não tenha a informação, o servidor consulta refaz a consulta </font>


**Cache DNS:** Armazena respostas temporariamente, assim consegue acelerar futuras consultas para o mesmo domínio.
    

----------

### 5. Processo de Resolução de Nomes

Etapas do processo completo:
1.  **Consulta ao servidor local**
2.  **Verificação do cache**
3.  **Consulta aos servidores raiz**
4.  **Consulta aos TLDs**
5.  **Consulta ao domínio de segundo nível**
6.  **Resposta final ao cliente**

----------

### 6. Cache DNS

**Conceito:** Armazena temporariamente registros DNS, melhorando o desempenho da rede.
    
>**TTL:** Define o tempo de validade da informação armazenada.

**Tipos:**
-   **Cache local em clientes**
-   **Cache em servidores de resolução**

 <font color="green">**Benefícios:**  Rapidez; Menos tráfego de rede; Redução da carga em servidores. </font> 
<font color="red">**Desafios de Segurança:** Envenenamento de Cache; Ataques MITM; Replays de respostas antigas. </font>
<font color="blue">**Proteções:** Boas práticas de segurança; Monitoramento de tráfego; Uso de **DNSSEC**. </font>

----------

### 7. Segurança e DNSSEC

&nbsp;&nbsp;&nbsp;&nbsp; O **DNSSEC** adiciona autenticação ao DNS.
 **Funções:**
-   Garante **integridade** e **autenticidade** das respostas.
-   Evita adulterações maliciosas.

**Cadeia de Confiança:** Assinaturas digitais desde a raiz até o domínio final.

----------

### 8. DNS over HTTPS (DoH) e DNS over TLS (DoT)

&nbsp;&nbsp;&nbsp;&nbsp; Tecnologias para **criptografar** consultas DNS.

**DoH:** Usa **HTTPS** para enviar consultas (*protege contra inspeção de tráfego*).
**DoT:** Usa **TLS** diretamente para enviar consultas (*protege contra privacidade*).
 <font color="green"> **Benefícios:** Aumentam a privacidade do usuário, tornando as consultas mais difíceis de interceptar. </font>
 <font color="red">**Desafios:** Dificultam filtragem de tráfego malicioso, além de depender da escolha de provedores confiáveis.</font>
    
----------

### 9. Tipos de Registros DNS

- **Registro A (IPv4):** Mapeia domínios endereços IPv4.
- **Registro AAAA (IPv6):** Versão para endereços IPv6.
- **Registro MX:** Define servidores de **e-mail** para o domínio (*inclui prioridades e redundância*).
- **Registro CNAME:** Cria **alias** para outro domínio canônico (*simplifica manutenção*).
-  **Registro TXT:** Armazena textos diversos. Usado em: **SPF**| **DKIM**| **DMARC**.
- **Registro NS:** Indica servidores de nomes autoritativos do domínio.
- **Registro SOA:** Registra informações essenciais da **zona**, como: Número serial | Intervalos de atualização |  Servidor primário.
- **Registro SRV:** Localiza serviços específicos (VoIP, mensagens etc.). Inclui: Porta | Protocolo | Prioridade | Peso.
- **Registros de Alias:** Apelidos usados frequentemente em CDNs (*flexibilizam apontamentos.*).

----------


### 10. Zoneamento e Zonas DNS
**Zonas Diretas:** Fazem a resolução nome → IP.
**Zonas Reversas:** Fazem a resolução IP → nome.
<font color="green"> **Benefícios:** Organização lógica | Delegação de autoridade | Escalabilidade | Facilita manutenção e atualizações. </font>

----------

### 11. Resolução de Problemas em DNS
**Problemas mais Comuns:**
-   Registros configurados incorretamente;
-   Zonas mal definidas;
-   Falhas de resolução;
-   Ataques de cache;
-   Problemas de rede/roteamento.
    
**Etapas de Diagnóstico**
-   Verificação da configuração;
-   Análise de logs
-   Testes com **dig**, **nslookup**, **traceroute**
-   Verificação de conectividade
-   Ajustes de segurança
-   Manutenção de documentação e backups
