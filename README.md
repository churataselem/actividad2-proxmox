# TAREA 2 - Configuración del proveedor Proxmox con Terraform

Este repositorio contiene la configuración inicial de Terraform para conectarse a un entorno Proxmox utilizando el proveedor Telmate/proxmox.

---

## 📄 Archivo principal

### `providers.tf`

```hcl
terraform {
  required_providers {
    proxmox = {
      source  = "Telmate/proxmox"
      version = "3.0.1-rc3"
    }
  }
}

provider "proxmox" {
  pm_tls_insecure      = true
  pm_api_url           = "https://localhost:8006/api2/json"
  pm_api_token_id      = "terra@pve!te"
  pm_api_token_secret  = "69622"
}
