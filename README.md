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
