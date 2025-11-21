Comandos Básicos do Azure (CLI e Portal)

Este documento reúne comandos e ações frequentes no gerenciamento de máquinas virtuais no Azure.

🧩 Azure CLI — Virtual Machines
🔹 Login
az login

🔹 Criar um Resource Group
az group create --name MeuGrupo --location eastus

🔹 Criar uma VM
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image Ubuntu2204 \
  --admin-username azureuser \
  --generate-ssh-keys

🔹 Listar VMs
az vm list -o table

🔹 Iniciar / Parar VM
az vm start -g MeuGrupo -n MinhaVM
az vm stop -g MeuGrupo -n MinhaVM

🧩 Auto Scale
Adicionar regra de escala (exemplo conceitual)
CPU > 75% → add 1 instance
CPU < 30% → remove 1 instance

🧩 VMSS (Virtual Machine Scale Set)
Criar um VMSS básico
az vmss create \
  --resource-group MeuGrupo \
  --name MeuScaleSet \
  --image Ubuntu2204 \
  --upgrade-policy-mode automatic

🧩 Rede
Criar VNet
az network vnet create \
  --resource-group MeuGrupo \
  --name VNetLab \
  --address-prefix 10.0.0.0/16 \
  --subnet-name Subnet1 \
  --subnet-prefix 10.0.1.0/24

🧩 Disponibilidade
Criar Availability Set
az vm availability-set create \
  --resource-group MeuGrupo \
  --name MeuAvailabilitySet \
  --platform-fault-domain-count 2 \
  --platform-update-domain-count 5

🧩 Backup
Habilitar backup básico
az backup protection enable-for-vm \
  --policy-name DefaultPolicy \
  --vault-name MeuBackupVault \
  --resource-group BackupGroup \
  --vm MinhaVM

🧩 Portal do Azure — Passo a passo
Criar VM no portal:

Azure Portal → “Virtual Machines”

“Create” → “Azure Virtual Machine”

Escolher Resource Group e nome

Escolher Image (Windows/Linux)

Selecionar tamanho (B, D, F Series)

Configurar usuário administrador

Revisar e criar
