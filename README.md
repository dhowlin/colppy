# Colppy - Despliegue de aplicacion con CloudFormation

Proyecto para el despliegue de una aplicación en AWS con CloudFormation. 

## Detalles y descricpion del archivo de infraestructura

El template para la creacion del stack en CloudFormation se presenta en formato de archivo YAML. El mismo contiene la infraestructura básica necesaria para el despliegue de una aplicación front-end simple. El mismo puede utilizarse como parte de un pipeline para CI/CD. Entre los componentes que se encuentran para el funcionamiento de la aplicacion se encuentran los siguientes definiciones:

- VPC, Internet Gateway y asociacion de ambos
- Subred Publica
- Route table para la subred publica, direcciones de ruteo, y asociacion de las mismas
- Balanceador de carga de aplicacion, listener del ALB y Target Group
- Instancia EC2 con la aplicacion y security group. 

## Diagramas de infraestructura

