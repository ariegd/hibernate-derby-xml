# Framework Hibernate
---------------------
https://www.tutorialspoint.com/hibernate/index.htm

Hibernate es un servicio de consulta y persistencia de objetos/relacional de alto rendimiento, que tiene la licencia de código abierto GNU Lesser General Public License (LGPL) y se puede descargar gratis. Hibernate no sólo se encarga del mapeo de clases Java a tablas de bases de datos (y de tipos de datos Java a tipos de datos SQL), sino que también proporciona funciones de consulta y recuperación de datos.

## Conexión mediante JDBC, Hibernate a base de datos Apache Derby
-----------------------------------------------------------------
https://stackoverflow.com/questions/3807503/what-is-the-purpose-of-two-config-files-for-hibernate/3808406#3808406

Si está utilizando la API patentada de Hibernate, necesitará hibernate.cfg.xml. Si está utilizando JPA, es decir, Hibernate EntityManager, necesitará persistence.xml.

Por lo tanto, generalmente no necesita ambos, ya que utiliza la API patentada de Hibernate o JPA.

Sin embargo, si estaba utilizando la API patentada de Hibernate y ya tiene hibernate.cfg.xml (y archivos de mapeo XML hbm.xml) pero desea comenzar a usar JPA, puede reutilizar los archivos de configuración existentes haciendo referencia a hibernate.cfg.xml en el persistence.xml en la propiedad hibernate.ejb.cfgfile y, por lo tanto, tendrá ambos archivos. Reutilizar archivos hbm.xml existentes es, en mi opinión, un escenario realista que podría justificar conservar ambos (incluso si probablemente migraría a anotaciones JPA a largo plazo).
