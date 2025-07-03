# 📦 rasPoE: Raspberry Pi 5 con PoE, NVMe y Docker

**rasPoE** es un proyecto experimental orientado a construir una infraestructura modular basada en Raspberry Pi 5, aprovechando tecnologías como Power over Ethernet (PoE), almacenamiento NVMe. El objetivo es lograr una arquitectura eficiente, documentada y escalable para homelabs y entornos híbridos.

## 🧠 Características

- Alimentación vía PoE para nodos autónomos y organizados.
- Integración de discos NVMe para alto rendimiento y durabilidad.
- Nodos especializados con HATs:
  - PoE+ (52Pi P30)
  - NVMe USB (52Pi N06)
- Consumo eléctrico optimizado y monitoreado.

## 🧱 Estructura

rasPoE/ ├── README.md ├── diagrams/ │   └── arquitectura.png ├── scripts/ │   ├── clone-to-nvme.sh │   ├── validate-uuid.sh │   └── raspoe-monitor.sh ├── docs/ │   ├── consumo.md │   ├── config-poe.md │   └── setup-nvme.md

## 🔌 Hardware usado

| Nodo | HAT         | Función principal         |
|------|-------------|---------------------------|
| Node 1 | 52Pi P30     | PoE + almacenamiento externo |
| Node 2 | 52Pi N06     | NVMe por USB 3.0             |
| Node 3 | AI HAT oficial | Inferencia IA por PCIe       |

Switch central: TP-Link TL-SG2210P (PoE+ 10 puertos)

## ⚙️ Scripts incluidos

- `clone-to-nvme.sh`: clona sistema de microSD a disco NVMe
- `validate-uuid.sh`: verifica PARTUUIDs en `cmdline.txt` y `fstab`
- `raspoe-monitor.sh`: evalúa consumo estimado por nodo y total

## 📈 Consumo eléctrico estimado

- Nodos: ~6–12 W c/u
- Switch PoE+: ~61 W total
- Costo mensual estimado: ~$134.3 MXN (@$2.36/kWh)

## 📚 Documentación

Revisa la carpeta `docs/` para configuraciones detalladas de VLANs, NTP, RAID y scripts personalizados.

## 📸 Diagrama de arquitectura

![rasPoE Arquitectura](diagrams/arquitectura.png)

## 🚀 Próximos pasos

- Integración con K3s/Kubernetes usando ROCK 5A como *workers*
- Automatización con Ansible para despliegue modular
- Publicación de métricas energéticas y rendimiento

## 🔌 Hardware usado

| Nodo | HAT         | Función principal         |
|------|-------------|---------------------------|
| Node 1 | 52Pi P30     | PoE + almacenamiento externo |

Router principal ER7212PC

## ⚙️ Scripts incluidos

- `clone-to-nvme.sh`: clona sistema de microSD a disco NVMe
- `validate-uuid.sh`: verifica PARTUUIDs en `cmdline.txt` y `fstab`
- `raspoe-monitor.sh`: evalúa consumo estimado por nodo y total

## 📈 Consumo eléctrico estimado

- Nodos: ~6–12 W c/u
- Router PoE+: ~150 W total
- Costo mensual estimado: ~$134.3 MXN (@$2.36/kWh)

## 📚 Documentación

Revisa la carpeta `docs/` para configuraciones detalladas de VLANs, NTP, RAID y scripts personalizados.

## 📸 Diagrama de arquitectura

![rasPoE Arquitectura](diagrams/arquitectura.png)

## 🚀 Próximos pasos

- Integración con K3s/Kubernetes usando ROCK 5A como *workers*
- Automatización con Ansible para despliegue modular
- Publicación de métricas energéticas y rendimiento

---
