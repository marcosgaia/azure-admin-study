Arquitetura Azure — Conceitos Fundamentais

Este arquivo resume os blocos estruturais mais importantes do Azure para quem está se preparando para prática ou certificação.

🔷 1. Resource Group

Contêiner lógico para recursos.

Ajuda na organização, controle de custos e remoção de recursos.

🔷 2. Virtual Network (VNet)

Rede isolada no Azure.

Equivalente a uma rede local tradicional.

Componentes:

Subnets

NIC (network interface)

Endereços privados

NSG (Network Security Groups)

🔷 3. Virtual Machine

Unidade computacional principal.

Pode rodar Windows ou Linux.

🔷 4. Disponibilidade
Availability Set

Distribui VMs em Fault Domains e Update Domains.

Availability Zones

Distribui VMs em datacenters físicos diferentes.

🔷 5. Load Balancer

Distribui tráfego entre múltiplas VMs.

Suporta VMSS.

🔷 6. Auto Scaling
Scale Up

Aumenta CPU/RAM de UMA VM.

Scale Out

Aumenta quantidade de VMs.

🔷 7. VMSS (Virtual Machine Scale Set)

Solução completa para autoescalonamento automático com instâncias idênticas.

🔷 8. Application Insights

Telemetria, logs, métricas, erros.

🔷 9. Backup e Recovery Services Vault

Backup de máquinas.

Retenção de longo prazo.

🔷 10. Monitoramento

Azure Monitor

Métricas

Logs Analytics
