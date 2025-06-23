# Projeto-MultiCloud-AWS-Azure
Projeto de Entrega: Integração Multi-Cloud Azure + AWS via VPN Site-to-Site
Este repositório contém toda a documentação e artefatos referentes ao projeto de integração entre nuvens Microsoft Azure e Amazon Web Services (AWS), realizado como parte da disciplina de Redes de Computadores no curso técnico do SENAI de Informática.

🧠 Objetivo do Projeto
Estabelecer um ambiente multi-cloud entre as plataformas Azure e AWS, configurando uma VPN Site-to-Site que possibilite a comunicação direta e segura entre máquinas virtuais privadas, utilizando apenas endereços IP internos (sem exposição pública).

🧰 Recursos Utilizados
🔵 Microsoft Azure
Serviço	Descrição
Virtual Network (VNet)	Rede virtual principal da Azure
Subnet Gateway	Subnet reservada exclusivamente para o VPN Gateway
Subnet Privada	Subnet onde a máquina virtual Debian foi provisionada
VPN Gateway	Componente de borda responsável pela conexão VPN
Local Network Gateway	Representa a VPC da AWS na configuração VPN
Virtual Machine	Instância privada (Debian 12 - tipo t2.micro)

🟠 Amazon Web Services (AWS)
Serviço	Descrição
VPC (Virtual Private Cloud)	Rede virtual principal da AWS
Subnet Privada	Subnet onde a instância EC2 foi provisionada
EC2 Instance	Instância privada (Ubuntu - tipo t2.micro)
Customer Gateway (CGW)	Representa o IP público da Azure na VPN
Virtual Private Gateway (VGW)	Gateway da AWS para a conexão VPN
VPN Connection	Conexão entre o VGW da AWS e o CGW da Azure

🖥️ Instâncias Virtuais
Plataforma	Sistema Operacional	Tipo da Instância	IP Privado
Azure	Debian 12	t2.micro	192.168.0.4
AWS	Ubuntu	t2.micro	172.16.0.213
