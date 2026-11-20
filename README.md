# Laboratorio n8n en Docker: workflow de decisión de Calbuco

Este repositorio contiene el laboratorio de la Clase 7: una instancia local de n8n con PostgreSQL (Docker Compose) y el workflow «Lab Calbuco», que clasifica cuatro documentos de prueba en Aprobado, Pendiente o Contingencia según el monto (umbral: mayor que 500000).

## Contenido
- `compose.yaml`: servicios postgres, n8n y api-lab del curso.
- `.env.ejemplo`: plantilla de variables de entorno (el archivo `.env` real NO se sube al repositorio).
- `lab-calbuco.json`: workflow exportado desde n8n.

## Cómo levantar el laboratorio
1. Copiar `.env.ejemplo` como `.env` (`Copy-Item .env.ejemplo .env` en PowerShell, `cp .env.ejemplo .env` en Linux).
2. Ejecutar `docker compose up -d` y comprobar con `docker compose ps`.
3. Abrir `http://localhost:5690` (n8n) y `http://localhost:5690/healthz` (salud). Importar `lab-calbuco.json` desde el menú del editor.
