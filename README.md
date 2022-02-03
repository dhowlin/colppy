# Colppy - Despliegue de aplicacion con CloudFormation

Proyecto para el despliegue de una aplicación en AWS con CloudFormation. 

## Consideraciones previas

Algunas consideraciones previas con respecto a este test tecnico:

1. Mi conocimiento en cloudformation es muy escaso. Me siento mas comodo con Terraform a pesar de que tampoco soy un experto. Entiendo que por cuestiones de partnership con el proveedor, sea necesario que el codigo este en formato legible para cloudformation. Debido a lo mencionado, para poder intentar hacer el proyecto necesite un poco de tiempo para poder leer un poco acerca de Cloudformation y poder poner algunas ideas juntas.

2. No pude probar mucho el codigo debido a que no poseo una cuenta AWS propia. Asi que es posible que el codigo tenga errores o no funcione del todo. Aun asi, lo que intente plasmar un poco mas mi conocimiento sobre la infraestructura basica necesaria para este proyecto. 

3. Dado que un requisito necesario es que codigo del manifiesto sea apto para CI/CD, incluyo un diagrama en donde se explica el flujo desde Git, pasando por distintos servicios necesarios de AWS para poder generar un pipeline (CodePipeline, CodeBuild, etc). Sin embargo, no incluyo las configuraciones necesarias de dichos servicios por cuestiones de tiempo, alcanze y acceso a las herramientas. 

## Detalles y descricpion del archivo de infraestructura

El template para la creacion del stack en CloudFormation se presenta en formato de archivo YAML. El mismo contiene la infraestructura básica necesaria para el despliegue de una aplicación front-end simple. El mismo puede utilizarse como parte de un pipeline para CI/CD. Entre los componentes que se encuentran para el funcionamiento de la aplicacion se encuentran los siguientes definiciones:

- VPC, Internet Gateway y asociacion de ambos
- Subred Publica
- Route table para la subred publica, direcciones de ruteo, y asociacion de las mismas
- Balanceador de carga de aplicacion, listener del ALB y Target Group
- Instancia EC2 con la aplicacion y security group. 

## Diagramas de infraestructura

[Diagrama de Infraestructura para la aplicacion wbe](images/colppy-aws-infra-diagrama.drawio.png)

[Diagrama CI/CD](images/cicd-taskcat-pipeline.png)


