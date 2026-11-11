# SQL-Server-DBA-Labs

# Laboratorio de Administración de Bases de Datos con SQL Server

Repositorio de prácticas de administración de bases de datos, enfocado en respaldos, automatización, almacenamiento y notificaciones con Microsoft SQL Server.

Los ejercicios se realizaron en un entorno local de laboratorio utilizando AdventureWorks2022.

## Objetivo

Desarrollar habilidades prácticas de administración de bases de datos y documentar los procedimientos y scripts utilizados durante mi formación como DBA.

## Herramientas utilizadas

- Microsoft SQL Server Developer Edition.
- SQL Server Management Studio (SSMS).
- T-SQL.
- SQL Server Agent.
- Database Mail.
- AdventureWorks2022.

## Prácticas realizadas

### 1. Preparación del entorno

- Instalación de SQL Server y SSMS.
- Restauración de AdventureWorks2022 para utilizarla como base de práctica.
- Exploración de objetos y propiedades de la base de datos.

### 2. Administración del almacenamiento

- Creación de una base de datos.
- Configuración de un grupo de archivos adicional.
- Incorporación de archivos de datos.
- Creación de una tabla dentro del grupo de archivos seleccionado.
- Carga de datos desde AdventureWorks2022.
- Observación del crecimiento y uso de espacio.

**Conceptos trabajados:** archivos MDF, NDF y LDF, filegroups y crecimiento automático.

### 3. Respaldos de bases de datos

- Ejecución de respaldos completos.
- Ejecución de respaldos diferenciales.
- Ejecución de respaldos del registro de transacciones.
- Generación de nombres de archivo con fecha y hora.

Ejemplo de nomenclatura:

```text
AdventureWorks2022-YYYY-MM-DD_HH-MM-SS.bak
AdventureWorks2022-YYYY-MM-DD_HH-MM-SS.dif
AdventureWorks2022-YYYY-MM-DD_HH-MM-SS.trn
```

### 4. Automatización con SQL Server Agent

- Creación de jobs para ejecutar respaldos.
- Configuración de pasos y programaciones.
- Revisión del historial y estado de ejecución.
- Habilitación y deshabilitación de jobs para controlar el consumo de espacio del laboratorio.

Programaciones utilizadas en la práctica:

| Tipo de respaldo | Frecuencia configurada |
|------------------|------------------------|
| Completo | Cada hora |
| Diferencial | Cada 30 minutos |
| Registro de transacciones | Cada 5 a 10 minutos |

Estas frecuencias se utilizaron con fines de aprendizaje. Una estrategia de producción debe definirse según los requisitos de recuperación, la carga de trabajo y el almacenamiento disponible.

### 5. Configuración de Database Mail

- Configuración de una cuenta y un perfil de correo.
- Configuración del servidor SMTP.
- Envío y recepción de un correo de prueba.

### 6. Consulta de metadatos y almacenamiento

- Consultas sobre columnas y esquemas mediante vistas de catálogo como `sys.columns` y `sys.schemas`.
- Generación de reportes de uso de disco.
- Revisión del espacio utilizado por las tablas.
- Exploración del reporte de clasificación de datos.

## Aprendizajes

Estas prácticas me han permitido:

- Comprender la función de los distintos tipos de respaldo.
- Automatizar tareas mediante SQL Server Agent.
- Revisar ejecuciones y detectar errores en jobs.
- Diferenciar archivos de datos, archivos de log y grupos de archivos.
- Consultar información de la estructura y el almacenamiento de una base de datos.
- Configurar el envío de correos desde SQL Server.

## Próximas prácticas

- Documentar una secuencia de restauración de respaldos completos, diferenciales y logs.
- Configurar notificaciones de resultados de jobs.
- Practicar la administración de usuarios, roles y permisos.
- Ampliar los ejercicios de monitoreo y diagnóstico de bloqueos.

## Alcance

Este repositorio documenta ejercicios de aprendizaje realizados en un entorno de laboratorio. No contiene datos, credenciales ni configuraciones internas de la institución donde realizo mi pasantía.

## Autora

**Valerie De La Cruz**

Estudiante de término de Ingeniería de Software, con enfoque en Administración de Bases de Datos.

[Perfil de GitHub](https://github.com/ValerieDC)
