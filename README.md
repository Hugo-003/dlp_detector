# Sistema DLP - Detector de fugas de datos

## Descripción
Este proyecto implementa un prototipo de sistema DLP (Data Loss Prevention) basado en ISO 27001:2022 (Control A.8.12). Detecta y enmascara datos sensibles en archivos TXT, PDF y Word (.docx), incluyendo DNI, email, teléfono, IBAN y tarjetas.

El prototipo permite:
- Analizar un archivo individual o toda una carpeta.
- Detectar datos sensibles y enmascararlos.
- Guardar los archivos enmascarados en una carpeta `masked_files`.
- Registrar todos los eventos y alertas en un log (`dlp_logs.txt`).

## Requisitos
Python 3.x y librerías necesarias:

pip install PyPDF2 python-docx reportlab

## Uso
1. Clona el repositorio:
git clone https://github.com/Hugo-003/dlp_detector.git
cd dlp_detector

2. Ejecuta el script:
python dlp_detectorV5.py

3. Introduce la ruta del archivo o carpeta a analizar (ejemplo Windows):
C:\Users\Hugo\Desktop\Universidad\Seguridad de datos\Trabajo final\dlp_test.txt

4. Todos los archivos enmascarados se generarán en la carpeta `masked_files`. Los logs se guardan en `dlp_logs.txt`.

## Archivos incluidos
- dlp_detectorV5.py : Script principal del DLP
- Archivos de ejemplo para testeo (opcional)
- README.md : Documentación y guía de uso

## Funcionalidades adicionales
- Escaneo recursivo de carpetas.
- Resumen global de incidencias en consola.
- Enmascarado manteniendo el tipo original del archivo (TXT, PDF, DOCX).

## Notas para la demo
- Se recomienda tener algunos archivos de ejemplo con datos sensibles para mostrar el funcionamiento.
- Los archivos enmascarados se encuentran en `masked_files`, mostrando que los datos críticos han sido ocultados.
- Se puede mostrar el `dlp_logs.txt` para evidenciar la detección de incidentes.
