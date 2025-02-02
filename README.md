# telegramTask
23-1 tarea grupo de Elliot
Tarea:  Fundamentos de AWS - Investigación Teórica

Objetivo: Comprender los servicios básicos y los conceptos clave de Amazon Web Services (AWS).

Instrucciones: Investiga los siguientes servicios y conceptos de AWS. Para cada uno, proporciona una breve descripción de su función, un caso de uso práctico.

Servicios:

1. S3 (Simple Storage Service): ¿Qué es? ¿Para qué se usa?

Es un servicio de almacenamiento en la nube donde se pueden guardar archivos de cualquier tipo y desde cualquier lugar de manera segura, escalable y accesible.

Se usa para almacenar fotos, videos, documentos, copias de seguridad, registros o incluso alojar sitios web estáticos (como un portafolio).

Como ejemplo tenemos una plataforma de streaming, que usa S3 para guardar y distribuir su contenido sin preocuparse por servidores o espacio.

2. IAM (Identity and Access Management): ¿Qué es? ¿Para qué se usa?
Es el servicio de AWS que gestiona quién puede acceder a qué recursos dentro de la nube. Permite crear usuarios, roles y establecer permisos específicos para controlar la seguridad.

Sirve para definir quién puede hacer qué dentro de AWS, evitando accesos no autorizados y mejorando la seguridad.

Como una empresa que crea un usuario IAM con permisos solo para leer archivos en S3, pero sin poder eliminarlos. Así, un empleado puede ver los datos sin riesgo de borrarlos accidentalmente.

3. VPC (Virtual Private Cloud): ¿Qué es? ¿Para qué se usa?
Es una red privada dentro de AWS donde se puede lanzar y controlar recursos como servidores, bases de datos y aplicaciones con reglas de acceso personalizadas.

Se usa para aislar y proteger recursos en la nube, definiendo quién y cómo pueden acceder a ellos. Permite crear subredes públicas y privadas, configurar firewalls y establecer conexiones seguras con otras redes.

Una empresa crea una VPC con dos subredes:
  a. Una pública para su servidor web accesible desde internet.
  b. Una privada para su DB, accesible solo desde el servidor web.

4. RDS (Relational Database Service): ¿Qué es? ¿Para qué se usa?
Es un servicio administrado de bases de datos relacionales en AWS que facilita la configuración, operación y escalado de DB como MySQL, PostgreSQL, SQL Server, entre otros.

Para gestionar bases de datos sin preocuparse por tareas como instalación, mantenimiento, copias de seguridad y actualizaciones.

Ejemplo, una tienda en línea usa RDS con MySQL para almacenar información de productos, clientes y pedidos. AWS se encarga de la seguridad, el rendimiento y los respaldos automáticos, evitando que la empresa tenga que administrar servidores de base de datos manualmente.
   
5. EBS (Elastic Block Storage): ¿Qué es? ¿Para qué se usa?
Es un servicio de almacenamiento en bloque para instancias de EC2. Funciona como un disco duro en la nube que se puede adjuntar a servidores virtuales (EC2).

Sirve para almacenar datos de sistemas operativos, aplicaciones y bases de datos en instancias EC2. Permite ampliar el almacenamiento sin perder datos y ofrece copias de seguridad (snapshots).

Ejemplo, una empresa ejecuta un servidor en EC2 con una aplicación web. Usa EBS para almacenar archivos y bases de datos, asegurando que si la instancia se detiene o reinicia, los datos siguen intactos.

6. Route 53: ¿Qué es? ¿Para qué se usa? 
Es el servicio de DNS (Domain Name System) de AWS que traduce nombres de dominio en direcciones IP y gestiona el tráfico de internet de manera escalable y confiable.

Sirve, para registrar dominios, gestionar zonas DNS y direccionar tráfico de manera inteligente a servidores, aplicaciones o balanceadores de carga en AWS o en otros lugares.

Ejemplo, una empresa tiene su sitio web alojado en S3 y usa Route 53 para conectar su dominio www.miempresa.com con el bucket de S3. Esto permite que los usuarios accedan al sitio escribiendo el dominio en su navegador en lugar de una IP.

Conceptos:

a. Regiones y Zonas de Disponibilidad: Define estos conceptos y explica su importancia en la arquitectura de AWS.

Es un área geográfica donde AWS tiene múltiples centros de datos. Cada región es independiente de las demás y ofrece servicios con baja latencia y alta disponibilidad.

Zona de Disponibilidad (AZ - Availability Zone):
Dentro de cada región, hay varias zonas de disponibilidad. Cada AZ es un conjunto de centros de datos físicamente separados, pero conectados con alta velocidad y baja latencia.

Importancia en la arquitectura de AWS:
  a. Alta disponibilidad: si una zona falla, otra puede seguir funcionando.
  b. Resiliencia: distribuir aplicaciones en varias AZs reduce el riesgo de interrupciones.
  c. Baja latencia: permite colocar recursos más cerca de los usuarios.
  d. Escalabilidad: facilita la distribución de cargas de trabajo en múltiples ubicaciones.

🔹 Ejemplo:
Un ecommerce usa dos zonas de disponibilidad en la región de EE.UU.-Este. Si una AZ falla, la otra sigue operando, evitando la caída del servicio.

Básicamente, usar múltiples AZs dentro de una región garantiza que las aplicaciones sean rápidas, seguras y siempre estén disponibles. 

2. AMI (Amazon Machine Image): ¿Qué es una AMI y para qué se utiliza?  Explica los diferentes tipos de AMIs.

Una AMI (Amazon Machine Image) es una plantilla que contiene todo lo necesario para lanzar una instancia EC2 en AWS. Incluye el sistema operativo, aplicaciones, configuraciones y permisos.

Se usa para crear instancias EC2 de manera rápida y consistente, evitando instalar y configurar todo manualmente en cada nueva máquina.
Tipos de AMIs:

1️⃣ AMIs de AWS

    Proporcionadas por AWS con sistemas operativos preconfigurados como Amazon Linux, Ubuntu o Windows Server.

2️⃣ AMIs personalizadas

    Creadas por los usuarios para incluir software, configuraciones y permisos específicos. Útil para replicar entornos con rapidez.

3️⃣ AMIs del Marketplace

    Ofrecidas por terceros con aplicaciones y servicios preinstalados (Ejemplo: AMIs con WordPress, bases de datos, firewalls, etc.).

4️⃣ AMIs propias (Privadas o Compartidas)

    AMIs personalizadas que pueden ser privadas (solo para un usuario) o compartidas con otras cuentas de AWS.
