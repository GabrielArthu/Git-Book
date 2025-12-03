# Um Pequeno Resumo de Aulas: Redes, Segurança e Infraestrutura

Este documento compila os principais conceitos abordados nas aulas dos professores Kenji Taniguchi e Paulo Marcotti durante o primeiro mês de aula no Alpha EdTech.
Obs:Não é nem a ponta do iceberg

---

## 1. Fundamentos de Redes e Internet
*Conceitos básicos que estruturam a comunicação global.*

### Internet vs. Web
- **Internet:** É a infraestrutura física e lógica global que conecta redes de computadores, permitindo a comunicação através do protocolo **IP** (Internet Protocol).
- **Web (World Wide Web):** É um serviço que roda "em cima" da internet, utilizando protocolos específicos (como HTTP/HTTPS) para exibir informações em navegadores.

### Estrutura Física e Lógica
- **Backbone:** A "espinha dorsal" da internet. São as vias principais de tráfego de dados de altíssima velocidade que interligam diferentes redes e países.
- **Topologia de Rede:** Refere-se ao layout físico ou lógico da rede. Define como os dispositivos estão conectados (ex: Estrela, Anel, Barramento, Malha).
- **Intranet vs. Extranet:**
    - *Intranet:* Rede privada interna de uma organização.
    - *Extranet:* Parte da intranet acessível a usuários externos autorizados (parceiros, fornecedores).

### Tipos de Rede (Escala Geográfica)
- **PAN (Personal Area Network):** Redes de curtíssima distância (ex: Bluetooth).
- **LAN (Local Area Network):** Redes locais (casas, escritórios).
- **MAN (Metropolitan Area Network):** Redes metropolitanas (cidades).
- **WAN (Wide Area Network):** Redes de longa distância (países, continentes).

---

## 2. Protocolos e Camada de Transporte
*Como os dados trafegam e são entregues.*

### TCP vs. UDP
- **TCP (Transmission Control Protocol):** Orientado a conexão. Garante a entrega dos dados na ordem correta (confiabilidade). Usado na Web, E-mail, Transferência de arquivos.
- **UDP (User Datagram Protocol):** Não orientado a conexão. Envia dados sem verificar se chegaram (velocidade). Usado em streaming, jogos online, VoIP.

### Endereçamento e NAT
- **NAT (Network Address Translation):** Técnica que permite que múltiplos dispositivos em uma rede privada (LAN) compartilhem um único endereço IP público para acessar a internet.
    - *Problema:* Quebra a conectividade direta ponto-a-ponta, dificultando aplicações como P2P e VoIP.
- **IPv4 vs. IPv6:**
    - *IPv4:* Esgotado, usa endereços de 32 bits.
    - *IPv6:* Solução para a escassez, usa 128 bits, permitindo um número virtualmente infinito de dispositivos.

### Transmissão de Dados
- **Unicast:** Envio de um para um.
- **Multicast:** Envio de um para um grupo específico.
- **Broadcast:** Envio de um para todos na rede.

---

## 3. Serviços de Aplicação e Desenvolvimento
*Ferramentas e arquiteturas para construção de software em rede.*

### Arquitetura de Software
- **Arquitetura de 3 Camadas:** Divisão lógica do software em: Apresentação (Frontend), Regra de Negócio (Backend) e Dados (Banco de Dados).
- **Microsserviços:** Abordagem onde uma aplicação é construída como um conjunto de pequenos serviços independentes que se comunicam via APIs.
- **SPA (Single Page Application):** Aplicações web que carregam uma única página HTML e atualizam o conteúdo dinamicamente (ex: via AJAX).

### APIs e Formatos de Dados
- **API RESTful:** Interface que utiliza os métodos HTTP (GET, POST, PUT, DELETE) para comunicação padronizada.
- **JSON vs. XML:**
    - *JSON:* Mais leve, legível e amplamente usado na web moderna.
    - *XML:* Mais verboso, estruturado e rigoroso.
- **Protobuf:** Formato de serialização de dados (Google), eficiente e rápido, mas binário.

---

## 4. Infraestrutura: DNS e Latência
*O sistema de nomes e a performance da rede.*

### DNS (Domain Name System)
Traduz nomes de domínio (ex: google.com) para endereços IP.
- **NSLookup:** Ferramenta para consultar registros DNS.
- **Registro PTR (Pointer):** O inverso do DNS padrão; resolve um IP para um nome.
- **Envenenamento de Cache (DNS Spoofing):** Ataque onde dados falsos são inseridos no cache do DNS, redirecionando o usuário para sites maliciosos.

### Performance
- **Latência:** Tempo que um pacote de dados leva para ir de um ponto a outro.
- **QoS (Quality of Service):** Mecanismos para priorizar tipos de tráfego (ex: voz > download) para garantir desempenho.

---

## 5. Segurança da Informação
*Proteção de dados, redes e identidades.*

### Criptografia e Certificados
- **HTTPS:** Adiciona camada SSL/TLS ao HTTP para segurança.
- **SSL/TLS Handshake:** Negociação de chaves e autenticação entre cliente e servidor antes da troca de dados.
- **Autoridades Certificadoras (CAs):** Entidades que emitem certificados digitais confiáveis.
- **Criptografia Simétrica vs. Assimétrica:**
    - *Simétrica:* Mesma chave codifica e decodifica.
    - *Assimétrica:* Par de chaves (Pública/Privada).

### Ameaças e Ataques
- **DDoS (Distributed Denial of Service):** Ataque coordenado para tornar um serviço indisponível.
    - *Mitigação:* Blackholing, Rate Limiting.
- **Engenharia Social:** Manipulação psicológica para obter dados confidenciais.
- **Insider Threat:** Ameaça interna (funcionários).

### VPN (Virtual Private Network)
- **Site-to-Site:** Conecta redes inteiras (ex: filial-matriz).
- **Acesso Remoto:** Conecta usuário individual à rede corporativa.

---

## 6. Tendências Modernas
*Novas tecnologias moldando o futuro das redes.*

- **IoT (Internet das Coisas):** Objetos físicos conectados. Desafios: segurança e padronização.
- **SDN (Software Defined Networking):** Separação do plano de controle (software) do plano de dados (hardware).
- **Blockchain:** Livro-razão descentralizado baseado em consenso.
- **CDN (Content Delivery Network):** Servidores distribuídos para entregar conteúdo com menor latência.

---

## 7. Controle de Versão (Git)
*Gestão de código fonte.*

- **Git:** Sistema de controle de versão distribuído.
- **Conceitos Chave:**
    - *Working Tree:* Área de trabalho atual.
    - *Index (Staging):* Área de preparação.
    - *Commit:* Registro permanente (snapshot).
- **Branch:** Linha de desenvolvimento paralela.
- **Merge:** Fusão de branches (pode gerar conflitos).
- **Git Stash:** Salva mudanças temporariamente sem commitar.
