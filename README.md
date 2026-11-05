# ValenciAPort GreenCloud

**Autor:** Víctor Arcón Barberá  
**NIA:** 10884442  
**Módulo:** Proyecto (2º ASIR)  

## Descripción del Proyecto
ValenciAPort GreenCloud es una solución de infraestructura de nube privada local y sostenible ("Green IT"), diseñada específicamente para una pyme del sector transitario y aduanero ubicada en la ZAL del Puerto de Valencia (20 usuarios concurrentes) [cite: 1, 12, 15].

## Objetivo de la Infraestructura
Proporcionar un entorno de alta disponibilidad, seguro y eficiente energéticamente (PUE objetivo de 1.27) para consolidar los servicios críticos de la empresa (ERP aduanero, gestión documental con Nextcloud, copias inmutables con Proxmox Backup Server y control perimetral con pfSense), garantizando el cumplimiento estricto del Esquema Nacional de Seguridad (ENS) y del RGPD [cite: 12, 16, 18].

## Tecnologías Utilizadas
- **Hipervisor:** Proxmox VE (KVM y LXC) [cite: 16]
- **Redes y Seguridad:** pfSense (Firewall SPI, segmentación VLAN 802.1Q, WireGuard VPN) [cite: 16]
- **Almacenamiento:** OpenZFS (ZFS Mirror / RAID10) [cite: 16]
- **Automatización (IaC):** Ansible (Inventarios, roles modulares y Ansible Vault) [cite: 16]
- **Monitorización:** Prometheus y Grafana (Telemetría de rendimiento y consumo energético kWh) [cite: 16]
- **Control de Versiones:** Git y GitHub (`victorarcon`) [cite: 16]

## Estructura del Repositorio
valenciaport-greencloud/
├── playbooks/
│   └── site.yml
├── roles/
│   ├── seguridad/
│   ├── monitorizacion/
│   ├── servicios_web/
│   └── firewall/
├── variables/
├── plantillas/
├── inventario/
├── documentacion/
└── README.md
