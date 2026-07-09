# GTFO-Engine

Motor de búsqueda de alta velocidad para binarios de explotación (GTFOBins), optimizado para entornos de auditoría y pentesting.

## 🚀 Arquitectura
GTFO-Engine transforma la base de datos de [GTFOBins](https://gtfobins.github.io/) en una estructura local indexada, permitiendo consultas instantáneas a través de la terminal sin necesidad de acceso a Internet.

* **Motor:** Basado en `jq` para manipulación de JSON de alto rendimiento.
* **Interfaz:** Integración nativa con `fzf` para selección visual de binarios y payloads.
* **Flujo:** Integración con portapapeles del sistema para explotación directa.

## 🛠 Instalación
```bash
git clone git@github.com:DaBit-Sec/gtfo-engine.git
cd gtfo-engine
# Asegúrate de ejecutar el sync inicial
./bin/gtfo-sync
```
## 📋 Componentes

    gtfo: Interfaz de consulta rápida. Uso: go (alias recomendado).

    gtfo-sync: Motor de ingesta y validación de integridad JSON.

    gtfo-check: Monitor de salud que verifica actualizaciones en el repositorio oficial.

## ⚡ Flujo de Trabajo

    Consulta: Ejecuta go en tu terminal.

    Selección: Navega por Binario > Función > Payload usando fzf.

    Ejecución: El payload seleccionado se copia automáticamente al portapapeles.

    Log: Cada uso queda registrado en ~/Security/logs/exploits.log para fines de auditoría.

## 🛡 Seguridad y Auditoría

La herramienta incluye:

    Validación de integridad: Verificación automática de estructuras JSON (jq empty).

    Backups: Generación de copias de seguridad previas a cualquier sincronización.

    Trazabilidad: Registro persistente de payloads utilizados.

Desarrollado para flujos de trabajo de auditoría de alto rendimiento.

## ⚠️ Disclaimer
Esta herramienta fue diseñada conjuntamente por **The Mentor** y **DaBit**. 

Su uso es bajo tu propia responsabilidad. Ni los autores ni los colaboradores se hacen responsables del uso indebido o malintencionado que pueda darle. 

Se fomenta la colaboración; si decides utilizar, modificar o distribuir este código, te agradeceremos la mención. 

Happy Hacking.
