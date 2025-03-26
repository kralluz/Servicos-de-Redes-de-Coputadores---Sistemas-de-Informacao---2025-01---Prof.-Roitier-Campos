# Projeto: Gestão de Redes de Computadores com Docker

## Visão Geral

Este projeto implementa uma infraestrutura de rede corporativa utilizando Docker, integrando serviços como DNS, DHCP, Firewall, LDAP, SAMBA, FTP e um servidor Web (NGINX).

## Estrutura do Projeto

- **docker-compose.yml:** Define a orquestração dos containers e a topologia de rede (sub-redes para servidores e clientes).
- **/dns/:** Arquivos de configuração do Bind9 (DNS).
- **/dhcp/:** Configuração do servidor DHCP.
- **/firewall/:** Script de regras do iptables.
- **/ldap/:** Arquivos para configuração do OpenLDAP.
- **/samba/:** Configuração do serviço SAMBA.
- **/ftp/:** Configuração do vsftpd.
- **/web/:** Configuração do NGINX e arquivos estáticos.
- **/router/:** Script de roteamento e NAT para o container roteador.
- **/ansible/:** Playbook para automação da implantação.

## Pré-requisitos

- Docker e Docker Compose instalados.
- (Opcional) Ansible para automação.

## Instruções de Implantação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu_usuario/seu_projeto.git
   cd seu_projeto
   ```

2. **Ajuste os arquivos de configuração:**
   Verifique e modifique os endereços IP, senhas e outros parâmetros conforme sua infraestrutura.

3. **Suba os containers:**
   ```bash
   docker-compose up -d
   ```

4. **(Opcional) Automatize com Ansible:**
   ```bash
   ansible-playbook ansible/deploy.yml
   ```

## Testes e Validação

- **DNS:**
  Verifique a resolução:
  ```bash
  dig @192.168.1.10 www.example.local
  ```

- **DHCP:**
  Conecte um cliente à sub-rede `192.168.1.0/24` e verifique a obtenção de IP.

- **LDAP & SAMBA:**
  Teste a autenticação e o acesso aos compartilhamentos.

- **FTP:**
  Conecte utilizando as credenciais definidas:
  - Usuário: `ftpuser`
  - Senha: `ftppass`

- **Web Server:**
  Acesse [http://192.168.1.60](http://192.168.1.60) para visualizar a página de boas-vindas.
