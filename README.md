# 📊 ICFES SQL AI Agent

Este proyecto implementa un agente inteligente capaz de consultar y analizar datos históricos de las pruebas **ICFES (Colombia)**. Utiliza una base de datos **SQL Server** dockerizada para el almacenamiento masivo y un agente de IA para la interpretación de consultas en lenguaje natural.

---

## 🚀 Estructura del Proyecto

```text
.
├── data/               # Archivos CSV originales del ICFES (ignorar en Git)
├── scripts/            # Scripts SQL para limpieza y carga (Bulk Insert)
├── agent/              # Código del Agente (Python + LangChain/OpenAI)
├── docker-compose.yml  # Configuración de SQL Server 2022
└── README.md

🛠️ Requisitos Previos
Docker & Docker Compose (instalado en Linux/WSL2).

SQL Server Management Studio (SSMS) o Azure Data Studio (para visualización).

Python 3.10+ (para el agente).

📦 Configuración del Entorno
1. Levantar la Base de Datos
Desde la terminal, en la raíz del proyecto, ejecuta:

docker compose up -d

2. Conexión a la Base de Datos
Host: localhost,1433 (o la IP de WSL)

User: sa

Password: colombia123 (definida en el compose)

Auth: SQL Server Authentication

Importante: Activar la opción Trust Server Certificate en el cliente SQL.

📈 Flujo de Datos (ICFES)
Descargar los microdatos desde el portal oficial ICFES Interactivo.

Colocar los archivos en la carpeta /data.

Ejecutar los scripts de /scripts/import_data.sql para cargar la información.

🤖 Agente de IA
El agente utiliza LangChain para transformar preguntas de usuario en consultas SQL. (Próximamente: Instrucciones de ejecución del agente).

Creado con ❤️ por daniloengineer