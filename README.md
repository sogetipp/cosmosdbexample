# Introducción

Este repositorio contiene los recursos necesarios para la formación de Cosmos DB impartido en Sogeti a finales del año 2021. Con estos recursos más el contenido de la formación en sí, son suficientes para hacer lo siguiente:

1. desarrollar un microservicio con arquitectura DDD en C# y .Net 5, 
2. crear una cuenta Cosmos DB en Azure, añadiendo datos y 
3. consultarlos desde el microservicio

# Contenido del repositorio

## documents for Cosmos DB.txt

Los datos a añadir a Cosmos DB. El modelo de datos consiste en tres libros pertenecientes a distintas secciones de una librería.

## Sogeti.Template.MicroserviceDddCosmosDb.vsix

Plantilla para crear automáticamente la solución y los proyectos del microservicio de ejemplo. Es un archivo ejecutable VSIX que instala la plantilla en Visual Studio. Tras la instalación, solo hay que crear un nuevo proyecto y buscar la plantilla por Sogeti.

# Troubleshooting

## GoneException

Al ejecutar el microservicio, durante la configuración del servicio de conexión con Cosmos DB puede aparecer esta excepción:

```
GoneException: The requested resource is no longer available at the server.
```

Para que funcione, hay que desconectar cualquier VPN que pudiera estar interfiriendo.

## VSIX Installer

Al intentar instalar la plantilla VSIX, el instalador da el siguiente error:

```
This extension is already installed to all applicable products.
```

Eso significa que ya hay una plantilla instalada en Visual Studio con el mismo nombre, probablemente de una formación anterior. Para poder instalar la nueva plantilla, hay que desinstalar la anterior en Visual Studio, desde _Extensions -> Manage Extensions -> Installed_.