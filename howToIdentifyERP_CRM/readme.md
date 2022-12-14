
# [馃嚜馃嚘](#identificar-y-estudiar-el-erpcrm-a-utilizar)
# [馃嚞馃嚙](#identify-and-study-of-erpcrm-to-use)

# Identificar y estudiar el ERP/CRM a utilizar

1. seleccionar el software a utilizar
En nuestro caso [odoo](https://www.odoo.com/)

2. 馃憖 ver los siguientes puntos 馃憖

  - [Tipos de implantaci贸n ](#tipos-de-implantaci贸n)
  - [Requerimientos hardware](#requerimientos-hardware)
  - [Sistema operativo ](#sistema-operativo)
  - [Pila tecnol贸gica de desarrollo  ](#pila-tecnol贸gica-de-desarrollo)
  - [Soporte t茅cnico ](#soporte-t茅cnico)
  - [Comunidades de usuarios ](#comunidades-de-usuarios)
  - [Acceso a documentaci贸n t茅cnica ](#acceso-a-documentaci贸n-t茅cnica)
  - [Tipo de empresas destino ](#tipo-de-empresas-destino)
  - [Facilidad de uso (UX/UI) ](#facilidad-de-uso-uxui)
  - [M贸dulos inclu铆dos. Diferenciar entre los m贸dulos del CRM y los del ERP ](#m%C3%B3dulos-incluidos-diferenciar-entre-los-m%C3%B3dulos-del-crm-y-los-del-erp)
  - [Coste seg煤n licencia requerida ](#coste-seg煤n-licencia-requerida)



## Tipos de implantaci贸n

### CRM
como CRM oodo tiene varios tipos de implantaci贸n
- operativo
- anal铆tico
- colaborativo

### ERP
en este caso es mas bien de prop贸sito general
- gen茅rico

### en local o en la nube
Odoo nos ofrece ambas soluciones siendo la version OnDemand la que ofrece de forma gratuita en su suscripci贸n One App

tambi茅n es posible montar todo lo necesario para trabajar con odoo de forma local para tener un servicio on Premise

## Requerimientos hardware

Un ordenador b谩sico que sea capaz de ejecutar Linux.

Como podemos decidir que tipo de CRM/ERP podemos montar vamos a definir que es lo que seria necesario en cada caso

- on Premise:
necesit谩remos una maquina en la que podamos alojar lo siguiente
  1. una base de datos de PostgreSQL
  2. el servicio de odoo

### Linux 馃惂

instalaremos Postgres como un servicio

```bash
~ sudo apt install postgresql -y
```

instalamos el servicio de odoo

```bash
wget -O - https://nightly.odoo.com/odoo.key | apt-key add -
echo "deb http://nightly.odoo.com/15.0/nightly/deb/ ./" >> /etc/apt/sources.list.d/odoo.list
apt-get update && apt-get install odoo
```

### windows 馃獰

necesitamos instalar [postgress](https://www.postgresql.org/)

podemos usar un instalador o un repositorio de github, veamos como clonar en github

vamos al terminal y escribimos lo siguiente

```bash
# nos situamos en el directorio donde queramos clonar y ejecutamos lo siguiente
git clone https://github.com/odoo/odoo.git

# para la version enterprise
git clone https://github.com/odoo/enterprise.git
```
una vez descargado podemos leer el readme del proyecto y seguir los pasos de instalaci贸n

### docker 馃悑

primero instalar [docker](https://www.docker.com/products/docker-desktop/)

luego podemos seguir la documentacion de la [imagen oficial](https://hub.docker.com/_/odoo/)

o simplemente podemos hace un `docker compose up` del siguiente archivo

```yml
version: '3.1'
services:
  web:
    image: odoo:14.0
    depends_on:
      - db
    ports:
      - "8069:8069"
  db:
    image: postgres:13
    environment:
      - POSTGRES_DB=postgres
      - POSTGRES_PASSWORD=odoo
      - POSTGRES_USER=odoo
```



## Sistema operativo

odoo se puede instalar f谩cilmente en :
- 馃獰***windows***馃獰 
- 馃惂***linux***馃惂

## Pila tecnol贸gica de desarrollo 

trabaja con las siguientes tecnolog铆as:

- HTML
- Javascript 
- CSS
- Python, para la l贸gica de negocio. Aunque se puede usar javascript, este ultimo esta deprecado
- postgreSql

## Soporte t茅cnico

cuenta con soporte t茅cnico en todo el mundo con diferentes sucursales, como normal general tiene el servicio t茅cnico en ingles pero tambi茅n es posible el servicio t茅cnico en espa帽ol y otros idiomas.


## Comunidades de usuarios

Odoo cuanta con una amplia comunidad de usuarios y muy activa, al ser un CRM/ERP de c贸digo abierto y gratuito la comunidad se ha volcado en dar soporte a los nuevos usuarios y ademas ir desarrollando problemas a distintas necesidades


## Acceso a documentaci贸n t茅cnica

es muy f谩cil de acceder desde la pagina de odoo hay varias secciones interesantes

- [Tutoriales](https://www.odoo.com/elearning)
- [documentaci贸n](https://www.odoo.com/page/docs)

ademas cuenta con enlaces a sus repositorios , foros y mas informaci贸n util

## Tipo de empresas destino

Odoo esta pensado para PYMES, aunque seg煤n sus creadores es escalable para grandes empresas

## Facilidad de uso (UX/UI)

podemos ver como es el uso de odoo a trav茅s de una [demo](https://demo.odoo.com/) que nos facilitan en la p谩gina en la cual vemos en vivo como funciona el servicio

se siente f谩cil de usar ya que de entrada tiene un menu con iconos que representas distintos puntos dentro de un CRM/ERP que hacen que sea muy f谩cil navegar, ademas dentro de cada uno de esos servicios todo es bastante intuitivo.


## M贸dulos incluidos. Diferenciar entre los m贸dulos del CRM y los del ERP

solo vamos a incluir algunos de los m贸dulos que incluye odoo por que tiene una cantidad de m贸dulos muy extensa.
- CRM
  - sales, ventas
  - suscriptions, suscripciones
  - Email marketing
- ERP
  - employees, empleados
  - inventory, inventario
  - accounting ,contabilidad
## Coste seg煤n licencia requerida

el coste para el servicio de entrada para una sola aplicaci贸n es de cero en para un servicio On demand, esto esta genial bien para aprender o para comenzar con un peque帽o negocio.

# Identify and study of ERP/CRM to use
<!-- TODO translate spanish version -->

- [Implements types](#implements-types)
- [Hardware requeriments](#hardware-requeriments)
- [Operating system](#operating-system)
- [Tech stack](#tech-stack)
- [Technichal support](#technichal-support)
- [Users community](#users-community)
- [Tech docummentation access](#tech-docummentation-access)
- [Target companies](#target-companies)
- [is easy to use (UX/UI) ](#is-easy-to-use-uxui)
- [Included modules. difference between CRM and ERP](#included-modules-difference-between-crm-and-erp)
- [Cost per license](#cost-per-license)

## Implements types
## Hardware requeriments
## Operating system
## Tech stack
## Technichal support
## Users community
## Tech docummentation access
## Target companies
## is easy to use (UX/UI) 
## Included modules. difference between CRM and ERP
## Cost per license