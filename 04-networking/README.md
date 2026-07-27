# 🌐 Azure Networking

![Azure](../assets/banner.png)

## Objetivo

Neste módulo foram estudados os principais serviços de rede do Microsoft Azure, entendendo como conectar recursos, datacenters e usuários com segurança.

---

# Serviços estudados

## Virtual Network (VNet)

A Azure Virtual Network (VNet) é uma rede privada na nuvem que permite a comunicação entre recursos do Azure e ambientes locais.

### Benefícios

- Isolamento de rede
- Comunicação segura
- Segmentação
- Controle de tráfego

![Virtual Network](../assets/networking-overview.png)

---

## Subnets

As Subnets permitem dividir uma VNet em várias redes menores.

### Benefícios

- Organização
- Segurança
- Separação entre ambientes
- Controle por NSG

![Subnet](../assets/subnet.png)

---

## VPN Gateway

Permite conectar uma empresa ao Azure através da Internet utilizando criptografia.

Tipos:

- Site-to-Site
- Point-to-Site
- VNet-to-VNet

O modelo recomendado é o **Route-based VPN Gateway**.

![VPN Gateway](../assets/vpn-gateway.png)

---

## Azure ExpressRoute

Serviço utilizado para criar uma conexão privada entre o datacenter da empresa e o Azure.

Vantagens:

- Maior velocidade
- Menor latência
- Maior segurança

![ExpressRoute](../assets/expressroute.png)

---

## Azure DNS

Serviço para hospedagem e gerenciamento de zonas DNS.

Permite criar registros:

- A
- AAAA
- MX
- TXT
- CNAME

![Azure DNS](../assets/azure-dns.png)

---

# Resumo

Neste módulo aprendi como o Azure realiza toda a comunicação entre recursos utilizando VNets, Subnets, VPN Gateway, ExpressRoute e Azure DNS.

---

## Conceitos aprendidos

- Virtual Network
- Subnets
- VPN Gateway
- Route-based Gateway
- ExpressRoute
- Azure DNS
- Comunicação híbrida
