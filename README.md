# TAREA 2 - Configuración del proveedor Proxmox con Terraform

Este repositorio contiene la configuración inicial de Terraform para conectarse a un entorno Proxmox utilizando el proveedor Telmate/proxmox, segun lo solicitado.

---

### 📄 Captura de Pantalla Terraform Init

📷 ![actividad2](https://github.com/churataselem/actividad2-proxmox/blob/main/Captura%20desde%202025-05-14%2014-08-33.png)


### 📄 Captura de Pantalla Terraform Plan

📷 ![actividad2](https://github.com/churataselem/actividad2-proxmox/blob/main/Captura%20desde%202025-05-14%2015-12-43.png)

### `providers.tf`

```hcl
terraform {
  required_providers {
    proxmox = {
      source = "Telmate/proxmox"
      version = "3.0.1-rc3"
    }
  }
}

provider "proxmox" {
  pm_tls_insecure      = true
  pm_api_url           = "https://200.9.165.138:8006/api2/json"
  pm_api_token_id      = "terra@pve!te"
  pm_api_token_secret  = "69622"
}
