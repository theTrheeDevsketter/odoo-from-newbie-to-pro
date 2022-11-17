
# [🇪🇦](#identificar-y-estudiar-el-erpcrm-a-utilizar)
# [🇬🇧](#identify-and-study-of-erpcrm-to-use)

# Identificar y estudiar el ERP/CRM a utilizar

1. seleccionar el software a utilizar
En nuestro caso [odoo](https://www.odoo.com/)

2. 👀 ver los siguientes puntos 👀

  - [Tipos de implantación ](#tipos-de-implantación)
  - [Requerimientos hardware](#requerimientos-hardware)
  - [Sistema operativo ](#sistema-operativo)
  - [Pila tecnológica de desarrollo  ](#pila-tecnológica-de-desarrollo)
  - [Soporte técnico ](#soporte-técnico)
  - [Comunidades de usuarios ](#comunidades-de-usuarios)
  - [Acceso a documentación técnica ](#acceso-a-documentación-técnica)
  - [Tipo de empresas destino ](#tipo-de-empresas-destino)
  - [Facilidad de uso (UX/UI) ](#facilidad-de-uso-uxui)
  - [Módulos incluídos. Diferenciar entre los módulos del CRM y los del ERP ](#m%C3%B3dulos-incluidos-diferenciar-entre-los-m%C3%B3dulos-del-crm-y-los-del-erp)
  - [Coste según licencia requerida ](#coste-según-licencia-requerida)



## Tipos de implantación

### CRM
como CRM oodo tiene varios tipos de implantación
- operativo
- analítico
- colaborativo

### ERP
en este caso es mas bien de propósito general
- genérico

### en local o en la nube
Odoo nos ofrece ambas soluciones siendo la version OnDemand la que ofrece de forma gratuita en su suscripción One App

también es posible montar todo lo necesario para trabajar con odoo de forma local para tener un servicio on Premise

## Requerimientos hardware

Un ordenador básico que sea capaz de ejecutar Linux.

Como podemos decidir que tipo de CRM/ERP podemos montar vamos a definir que es lo que seria necesario en cada caso

- on Premise:
necesitáremos una maquina en la que podamos alojar lo siguiente
  1. una base de datos de PostgreSQL
  2. el servicio de odoo

### Linux 🐧

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

### windows 🪟

necesitamos instalar [postgress](https://www.postgresql.org/)

podemos usar un instalador o un repositorio de github, veamos como clonar en github

vamos al terminal y escribimos lo siguiente

```bash
# nos situamos en el directorio donde queramos clonar y ejecutamos lo siguiente
git clone https://github.com/odoo/odoo.git

# para la version enterprise
git clone https://github.com/odoo/enterprise.git
```
una vez descargado podemos leer el readme del proyecto y seguir los pasos de instalación

### docker 🐋

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

odoo se puede instalar fácilmente en :
- 🪟***windows***🪟 
- 🐧***linux***🐧

## Pila tecnológica de desarrollo 

trabaja con las siguientes tecnologías:

- HTML
- Javascript 
- CSS
- Python, para la lógica de negocio. Aunque se puede usar javascript, este ultimo esta deprecado
- postgreSql

## Soporte técnico

cuenta con soporte técnico en todo el mundo con diferentes sucursales, como normal general tiene el servicio técnico en ingles pero también es posible el servicio técnico en español y otros idiomas.


## Comunidades de usuarios

Odoo cuanta con una amplia comunidad de usuarios y muy activa, al ser un CRM/ERP de código abierto y gratuito la comunidad se ha volcado en dar soporte a los nuevos usuarios y ademas ir desarrollando problemas a distintas necesidades


## Acceso a documentación técnica

es muy fácil de acceder desde la pagina de odoo hay varias secciones interesantes

- [Tutoriales](https://www.odoo.com/elearning)
- [documentación](https://www.odoo.com/page/docs)

ademas cuenta con enlaces a sus repositorios , foros y mas información util

## Tipo de empresas destino

Odoo esta pensado para PYMES, aunque según sus creadores es escalable para grandes empresas

## Facilidad de uso (UX/UI)

podemos ver como es el uso de odoo a través de una [demo](https://demo.odoo.com/) que nos facilitan en la página en la cual vemos en vivo como funciona el servicio

se siente fácil de usar ya que de entrada tiene un menu con iconos que representas distintos puntos dentro de un CRM/ERP que hacen que sea muy fácil navegar, ademas dentro de cada uno de esos servicios todo es bastante intuitivo.


## Módulos incluidos. Diferenciar entre los módulos del CRM y los del ERP

solo vamos a incluir algunos de los módulos que incluye odoo por que tiene una cantidad de módulos muy extensa.
- CRM
  - sales, ventas
  - suscriptions, suscripciones
  - Email marketing
- ERP
  - employees, empleados
  - inventory, inventario
  - accounting ,contabilidad
## Coste según licencia requerida

el coste para el servicio de entrada para una sola aplicación es de cero en para un servicio On demand, esto esta genial bien para aprender o para comenzar con un pequeño negocio.

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