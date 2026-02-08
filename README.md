# 📊 ICFES SQL AI Agent

Este proyecto implementa un agente inteligente capaz de consultar y analizar datos históricos de las pruebas **ICFES (Colombia)**. Utiliza una base de datos **SQL Server** dockerizada para el almacenamiento masivo y un agente de IA para la interpretación de consultas en lenguaje natural.

---

## 🚀 Estructura del Proyecto

```text
.
├── agent/              # Código del Agente (Python + LangChain)
├── data/               # Archivos CSV originales (Ignorados por Git)
├── scripts/            # Scripts SQL (Creación y Carga)
├── venv/               # Entorno virtual de Python
├── docker-compose.yml  # Infraestructura de Base de Datos
└── README.md           # Documentación
```

---

## 🛠️ Requisitos Previos

* **Docker & Docker Compose**: Instalado en Linux/WSL2.
* **SQL Server Management Studio (SSMS)**: O Azure Data Studio para visualización.
* **Python 3.10+**: Para el funcionamiento del agente.

--- 

## 📦 Configuración del Entorno

### 1. Levantar la Base de Datos
Desde la terminal, en la raíz del proyecto, ejecuta:

```bash
docker compose up -d
```

### 2. Conexión a la Base de Datos
Host: localhost,1433 (o la IP de WSL).

User: sa

Password: colombia123

Importante: Activar la opción Trust Server Certificate en el cliente SQL.

---

# 📈 Flujo de Datos (ICFES)

Descargar: Obtener los microdatos desde el portal oficial del ICFES.

Ubicar: Colocar los archivos en la carpeta /data.

Cargar: Ejecutar los scripts en /scripts/import_data.sql.

---
# 🤖 Agente de IA
El agente utiliza LangChain para transformar preguntas de usuario en consultas SQL directamente sobre la base de datos.

---

Creado con ❤️ por daniloengineer


