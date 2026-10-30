# Plan de auditoría: control de acceso al computador del gimnasio

**Asignatura:** Auditoría de Sistemas (ET0114)  
**Taller:** Del riesgo priorizado al plan de auditoría  
**Organización:** Gimnasio local  
**Docente:** Juan Duque  
**Fecha de exposición:** 30 de octubre de 2026  
**Fecha de entrega:** 1 de noviembre de 2026  
**Integrantes:** [Agregar nombres completos]

---

## 1. Contexto del caso

La organización seleccionada es un gimnasio local que maneja información de sus clientes mediante un cuaderno físico y un archivo de Excel almacenado en el computador del lugar. En el cuaderno se registran datos como el nombre, documento de identidad, número de celular y la información relacionada con los pagos. Después, el administrador pasa parte de esta información al archivo de Excel para llevar un control de los clientes y sus mensualidades.

Durante el levantamiento de información se identificó que el computador no tiene contraseña de inicio de sesión. También se indicó que varias personas pueden acceder al archivo de Excel, aunque todavía no se conocen con exactitud los permisos de cada una. Por esta razón, se considera importante revisar cómo se controla el acceso al equipo y cómo se protege la información almacenada.

## 2. Riesgo seleccionado y justificación

Se seleccionó el riesgo **R-03 — Acceso no autorizado al computador**, conservando el identificador de la matriz inicial de riesgos.

| Elemento | Descripción |
|---|---|
| **Activo o proceso** | Computador del gimnasio. |
| **Amenaza** | Una persona sin autorización accede al computador y consulta o modifica la información almacenada. |
| **Vulnerabilidad** | El computador no tiene contraseña de inicio de sesión. |
| **Riesgo y consecuencia** | Una persona podría acceder al equipo sin autorización y consultar, modificar o eliminar información de los clientes. |
| **Probabilidad** | 4 |
| **Impacto** | 4 |
| **Nivel** | 16 |

### Justificación

Se seleccionó este riesgo porque tiene uno de los niveles más altos de la matriz y afecta directamente la protección de la información de los clientes. Además, se identificó una vulnerabilidad concreta: el computador no tiene contraseña de inicio de sesión. Esto permite plantear una auditoría enfocada en verificar cómo se controla el acceso al equipo y qué medidas existen para evitar que personas no autorizadas puedan consultar o modificar la información.

El riesgo también es viable para una auditoría delimitada porque se puede revisar el equipo, sus cuentas de usuario, la configuración de inicio de sesión y los permisos del archivo de Excel. Sin embargo, todavía hay información que debe solicitarse o confirmarse durante la revisión, por lo que el plan no da por hecho que existan controles adicionales.

## 3. Objetivo de auditoría

**Determinar si los controles de acceso al computador del gimnasio permiten evitar que personas no autorizadas ingresen al equipo y puedan consultar, modificar o eliminar la información de los clientes almacenada en él.**

El objetivo es verificable porque se puede contrastar la configuración del equipo y los permisos de acceso con las condiciones de seguridad definidas para la auditoría. La revisión permitirá identificar qué mecanismos existen, quiénes pueden utilizar el computador y si la información está protegida frente a accesos no autorizados.

## 4. Alcance funcional

| Elemento | Alcance propuesto |
|---|---|
| **Proceso o función** | Control de acceso al computador y protección de la información almacenada. |
| **Sistema o componente** | Computador del gimnasio y archivo de Excel donde se registra información de los clientes. |
| **Población** | Cuentas de usuario configuradas en el computador, mecanismos de inicio de sesión y permisos de acceso al archivo de Excel. |
| **Periodo** | Se revisará el estado actual de la configuración. Si existen registros históricos de acceso o cambios, se solicitarán los correspondientes a los tres meses anteriores a la auditoría. |
| **Áreas o responsables** | Administrador del gimnasio y personas que tengan autorización para utilizar el computador. |
| **Inclusiones** | Inicio de sesión, cuentas de usuario, protección mediante contraseña, bloqueo de pantalla y permisos del archivo de Excel. |
| **Exclusiones** | Seguridad de la red, cámaras, copias de seguridad, pagos por QR y otros equipos que no estén relacionados directamente con el acceso al computador. |

La revisión se concentra en el computador porque es el componente donde se almacena el archivo de Excel. No se pretende evaluar toda la seguridad informática del gimnasio ni concluir sobre controles que no estén dentro de este alcance.

**Limitación del alcance:** todavía no se conoce el sistema operativo del computador ni si existen registros de inicio de sesión o de modificación de archivos. Esta información se solicitará al administrador. Si no existen registros, la auditoría podrá revisar la configuración actual, pero no podrá confirmar con el mismo nivel de detalle quién accedió al equipo durante el periodo anterior.

## 5. Criterios de evaluación

Los criterios permiten establecer qué condición se espera encontrar y contra qué fuente se comparará la evidencia. Para este riesgo se utilizarán como referencia los controles de seguridad de la información de ISO/IEC 27001:2022 y los objetivos de gestión de accesos relacionados con COBIT 2019.

No se afirma que el gimnasio tenga políticas internas documentadas. Si existe una política o procedimiento de acceso, se solicitará para verificar su vigencia y utilizarlo como criterio interno. Si no existe, se dejará registrado como una condición por confirmar y no se presentará como un incumplimiento demostrado antes de ejecutar la auditoría.

| Control o aspecto | Condición esperada para la auditoría | Fuente y aplicación |
|---|---|---|
| **Identificación de usuarios** | Debe ser posible identificar qué personas están autorizadas para utilizar el computador y qué cuenta utiliza cada una. | ISO/IEC 27001:2022, control 5.16 (gestión de identidades) y 5.18 (derechos de acceso). |
| **Autenticación de acceso** | El ingreso al computador debe contar con un mecanismo de autenticación que impida el acceso libre de personas no autorizadas. Se revisará si existe contraseña u otro mecanismo y cómo está configurado. | ISO/IEC 27001:2022, controles 5.17 (información de autenticación) y 8.5 (autenticación segura). |
| **Restricción de acceso a la información** | El archivo de Excel debe estar disponible únicamente para las personas que necesiten utilizarlo según sus funciones. | ISO/IEC 27001:2022, control 8.3 (restricción de acceso a la información). |
| **Gestión de cuentas y permisos** | Las cuentas y los permisos deben corresponder a las personas autorizadas y a las actividades que realizan. Los accesos que ya no sean necesarios deberían retirarse. | COBIT 2019, objetivo DSS05 (Managed Security Services), como orientación para revisar la gestión de accesos. |
| **Procedimiento interno** | Si el gimnasio cuenta con una política o procedimiento de acceso, la configuración y la forma de uso del equipo deberían corresponder con lo establecido allí. | Política o procedimiento interno vigente, **por confirmar mediante solicitud al administrador**. No se presupone que exista. |

Los marcos se utilizan como fuentes de criterios y orientación. No se evaluará el cumplimiento completo de ISO/IEC 27001 ni de COBIT, sino únicamente los aspectos relacionados con el riesgo R-03.

## 6. Programa de trabajo

La auditoría se desarrollará mediante dos procedimientos complementarios. Primero se buscará comprender cómo está diseñado el control de acceso y después se revisará si la configuración y los elementos disponibles corresponden con las condiciones esperadas.

### 6.1. Procedimiento 1: revisar el diseño del control de acceso

**Propósito:** conocer cómo debería funcionar el acceso al computador, quién puede utilizarlo y qué mecanismos están definidos para proteger la información.

**Actividades propuestas:**

1. Solicitar al administrador que explique quiénes utilizan el computador y qué actividades realiza cada persona.
2. Solicitar la lista de personas autorizadas y compararla con las cuentas de usuario configuradas en el equipo.
3. Revisar si existe una política, instrucción o procedimiento que indique cómo se debe ingresar al computador y quién puede acceder al archivo de Excel.
4. Inspeccionar la configuración de inicio de sesión para identificar si el equipo solicita contraseña u otro mecanismo de autenticación.
5. Revisar los permisos del archivo de Excel y determinar qué usuarios pueden abrirlo, modificarlo o eliminarlo.
6. Comparar lo encontrado con los criterios definidos en el apartado anterior.

**Población o muestra:** todas las cuentas de usuario configuradas en el computador y los permisos del archivo de Excel. Si el equipo tiene varias cuentas, se revisarán todas, ya que se espera que sea una población pequeña.

**Evidencia esperada:**
- Lista de personas autorizadas para utilizar el computador.
- Capturas o registro de la configuración de inicio de sesión, con autorización del responsable.
- Listado de cuentas de usuario configuradas.
- Configuración de permisos del archivo de Excel.
- Política o procedimiento interno, si existe.
- Notas de la entrevista con el administrador, utilizadas como apoyo y no como única evidencia.

**Posibles excepciones:**
- No se puede identificar quién está autorizado para utilizar el computador.
- El equipo permite el ingreso sin autenticación.
- Existen cuentas que no corresponden a personas autorizadas o cuya finalidad no se puede explicar.
- El archivo de Excel puede ser modificado por personas que no necesitan hacerlo.
- No existe un procedimiento para definir o retirar permisos. Esto se registrará según la evidencia disponible, sin asumir automáticamente un incumplimiento.

### 6.2. Procedimiento 2: verificar la operación del control

**Propósito:** comprobar si los mecanismos de acceso que se encuentren configurados funcionan de acuerdo con las condiciones esperadas y si los permisos limitan el acceso a la información.

**Actividades propuestas:**

1. Con autorización del administrador, realizar una prueba controlada de inicio de sesión para verificar si el equipo exige autenticación antes de permitir el acceso.
2. Revisar con el administrador las cuentas existentes y comprobar si corresponden con las personas autorizadas.
3. Seleccionar las cuentas o perfiles disponibles y verificar qué permisos tienen sobre el archivo de Excel.
4. Comparar los permisos encontrados con las funciones de las personas autorizadas. No se realizarán cambios ni se eliminará información durante las pruebas.
5. Si existen registros de inicio de sesión o de cambios, solicitar los disponibles para los tres meses anteriores a la auditoría y revisar si permiten identificar accesos o modificaciones.
6. Registrar cada diferencia entre la configuración observada y los criterios de evaluación. Cuando no exista evidencia suficiente, clasificar el punto como no verificable en lugar de asumir que el control funciona o que no funciona.

**Población o muestra:** se revisarán todas las cuentas configuradas y los permisos del archivo de Excel. Para los registros históricos, se solicitará la población disponible del periodo definido. Si el volumen es alto, se propondrá una muestra que incluya registros de diferentes fechas y usuarios. El tamaño se definirá cuando se conozca la cantidad real de registros.

**Evidencia esperada:**
- Resultado documentado de la prueba controlada de inicio de sesión.
- Relación de cuentas y permisos revisados.
- Comparación entre personas autorizadas y cuentas existentes.
- Registros de inicio de sesión o de modificaciones, si el equipo los genera y conserva.
- Hoja de trabajo del auditor con las pruebas realizadas, resultados y excepciones.

**Posibles excepciones:**
- El computador permite ingresar sin autenticación.
- Una cuenta activa pertenece a una persona que no está autorizada.
- Los permisos permiten modificar el archivo a personas que no necesitan hacerlo.
- No se pueden identificar los usuarios que realizan cambios, cuando el control definido requiere esa identificación.
- No existen registros para comprobar la operación histórica del control. Esto se reportará como limitación de evidencia y no como prueba automática de que hubo un acceso no autorizado.

### 6.3. Fila de trazabilidad

| ID del riesgo | Control a evaluar | Criterio y fuente | Procedimiento | Población o muestra | Evidencia esperada |
|---|---|---|---|---|---|
| R-03 | Identificación y autenticación para ingresar al computador. | ISO/IEC 27001:2022, controles 5.16, 5.17 y 8.5. Política interna, si existe, por confirmar. | Inspeccionar la configuración de inicio de sesión y realizar una prueba controlada con autorización. | Todas las cuentas del computador y configuración actual. | Capturas autorizadas de configuración, listado de cuentas y resultado de la prueba. |
| R-03 | Restricción de acceso al archivo de Excel. | ISO/IEC 27001:2022, control 8.3; COBIT 2019, objetivo DSS05. | Revisar permisos y compararlos con las funciones y autorizaciones de los usuarios. | Todas las cuentas y permisos disponibles sobre el archivo. | Configuración de permisos, lista de personas autorizadas y hoja de comparación. |
| R-03 | Administración de cuentas y seguimiento de accesos, si existen registros. | ISO/IEC 27001:2022, controles 5.18 y 8.15 (registro de eventos); criterio interno por confirmar. | Solicitar los registros disponibles y revisar si permiten identificar usuarios y eventos durante el periodo. | Registros disponibles de los tres meses anteriores; muestra por definir según el volumen real. | Registros de acceso o cambios, si existen, y hoja de revisión de excepciones. |

## 7. Organización de la ejecución propuesta

### 7.1. Fases y cronograma

El siguiente cronograma es una propuesta para ejecutar la auditoría. Las fechas exactas dependerán de la disponibilidad del administrador y de la autorización para revisar el computador.

| Fase | Actividades | Duración estimada | Resultado esperado |
|---|---|---:|---|
| **1. Preparación** | Confirmar objetivo, alcance, criterios, responsables y permisos para realizar la revisión. | 1 día | Plan de trabajo y solicitud de información. |
| **2. Solicitud de información** | Solicitar lista de usuarios autorizados, procedimiento de acceso, cuentas y registros disponibles. | 1 día | Información recibida o relación de información pendiente. |
| **3. Revisión del diseño** | Inspeccionar la configuración, las cuentas y los permisos del archivo de Excel. | 1 día | Hoja de trabajo del procedimiento 1. |
| **4. Verificación de operación** | Realizar pruebas controladas y revisar los registros disponibles. | 1 a 2 días | Hoja de trabajo del procedimiento 2 y excepciones identificadas. |
| **5. Cierre** | Comparar resultados con los criterios, documentar limitaciones y preparar las conclusiones de la auditoría. | 1 día | Documento de resultados, si la auditoría llega a ejecutarse. |

### 7.2. Responsables

| Responsable | Función propuesta |
|---|---|
| Integrante 1 | Coordinar el plan, organizar la información y revisar que los procedimientos respondan al objetivo. |
| Integrante 2 | Preparar la lista de criterios y revisar la documentación solicitada. |
| Integrante 3 | Apoyar la inspección de cuentas, autenticación y permisos, siempre con autorización. |
| Administrador del gimnasio | Explicar el proceso, indicar quiénes están autorizados y facilitar la evidencia disponible. |

Si el equipo tiene menos o más integrantes, las funciones se pueden distribuir entre los miembros reales. El administrador participa como responsable de la organización y no como integrante del equipo auditor.

### 7.3. Recursos y dependencias

**Recursos necesarios:**
- Acceso autorizado al computador del gimnasio.
- Disponibilidad del administrador o responsable del equipo.
- Lista de personas autorizadas para utilizar el computador, si existe.
- Acceso de consulta a la configuración de cuentas y permisos.
- Documentación interna relacionada con el acceso, si existe.
- Formato u hoja de trabajo para registrar pruebas y excepciones.

**Dependencias:**
- Autorización del gimnasio para revisar el computador.
- Disponibilidad del administrador para explicar el proceso.
- Posibilidad de consultar la configuración sin alterar información.
- Existencia y disponibilidad de registros históricos, si se pretende revisar el periodo anterior.

### 7.4. Actividades que se pueden realizar y actividades pendientes

Con la información actual se puede preparar el objetivo, el alcance, los criterios y los procedimientos. También se puede dejar identificada la vulnerabilidad reportada: el computador no tiene contraseña.

La inspección técnica, las pruebas de inicio de sesión y la revisión de permisos solo se podrán realizar cuando el gimnasio autorice el acceso al equipo. La revisión de registros históricos dependerá de que el computador o el sistema utilizado los genere y conserve.

## 8. Supuestos y limitaciones

### 8.1. Hechos conocidos del caso

- El gimnasio registra información de los clientes en un cuaderno físico y posteriormente pasa parte de ella a un archivo de Excel.
- El archivo de Excel se encuentra almacenado en el computador del gimnasio.
- Se indicó que el computador no tiene contraseña.
- Se indicó que varias personas pueden acceder al archivo de Excel.

Estos datos corresponden a la información suministrada durante el levantamiento inicial del caso. No equivalen a una verificación técnica realizada por el equipo auditor.

### 8.2. Supuestos de trabajo

- Se considera que el computador y el archivo de Excel son relevantes para el funcionamiento administrativo del gimnasio.
- Se plantea que el administrador puede explicar quiénes utilizan el equipo y facilitar la revisión, pero esto debe confirmarse.
- Se propone revisar todas las cuentas y permisos disponibles porque se espera que la cantidad sea manejable. La cantidad real todavía se desconoce.

### 8.3. Información por solicitar

- Sistema operativo instalado en el computador.
- Lista de personas autorizadas para utilizarlo.
- Cuentas de usuario configuradas y permisos asignados.
- Existencia de algún procedimiento o instrucción para controlar el acceso.
- Configuración de inicio de sesión y bloqueo de pantalla.
- Registros de inicio de sesión o modificación de archivos, si existen.
- Personas que tienen permiso para abrir, modificar o eliminar el archivo de Excel.

### 8.4. Propuestas del equipo

- Evaluar la autenticación para ingresar al computador.
- Revisar que las cuentas y permisos correspondan con las personas autorizadas.
- Comprobar que el archivo de Excel no esté disponible para personas que no necesitan utilizarlo.
- Solicitar y revisar registros históricos cuando estén disponibles.

### 8.5. Limitaciones

El equipo todavía no ha ejecutado la auditoría ni ha tenido acceso técnico al computador. Por lo tanto, este documento es un plan propuesto y no presenta resultados, hallazgos ni porcentajes de cumplimiento.

Si el gimnasio no permite revisar el equipo o no conserva registros de acceso, algunas pruebas no podrán realizarse. En ese caso, la conclusión deberá limitarse a la evidencia que sí se haya podido obtener. La falta de registros no demuestra por sí sola que haya ocurrido un acceso no autorizado.

## 9. Relación con los marcos de referencia seleccionados

Para este riesgo se retoman únicamente los marcos que tienen relación directa con el control de acceso.

### ISO/IEC 27001

Se utiliza como referencia principal porque establece un marco para gestionar la seguridad de la información. Para este plan interesan especialmente los controles relacionados con la gestión de identidades, la información de autenticación, los derechos de acceso, la restricción de acceso a la información y la autenticación segura.

### COBIT 2019

Se utiliza como referencia complementaria para orientar la gestión de los accesos y la administración de los servicios de seguridad. Ayuda a revisar si las responsabilidades y los permisos están definidos y si el acceso a la información se administra de forma controlada.

### Ley 1581 de 2012

No será un criterio principal para probar la configuración técnica del inicio de sesión. Sin embargo, se mantiene como marco legal relacionado con la protección de los datos personales que almacena el gimnasio. Su aplicación se relaciona con el deber de proteger esa información y con el tratamiento adecuado de los datos de los clientes.

## 10. Conclusión

El riesgo R-03 fue seleccionado porque presenta un nivel de 16 en la matriz y porque se identificó que el computador del gimnasio no tiene contraseña de inicio de sesión. Esta condición hace necesario revisar cómo se controla el acceso al equipo y quiénes pueden consultar o modificar la información almacenada.

El plan propuesto define un objetivo verificable, un alcance delimitado, criterios relacionados con ISO/IEC 27001 y COBIT 2019 y dos procedimientos complementarios para revisar el diseño y la operación de los controles. También establece qué evidencia se solicitaría y qué limitaciones podrían presentarse.

La auditoría todavía no se ha ejecutado. Por eso, no se afirma que el gimnasio cumpla o incumpla los marcos de referencia. Las conclusiones reales dependerán de la evidencia que se pueda obtener durante la revisión.

## 11. Fuentes y documentos de referencia

- **Taller: del riesgo priorizado al plan de auditoría.** Guía de trabajo de la asignatura Auditoría de Sistemas (ET0114), docente Juan Duque, octubre de 2026.
- **Taller de matriz de riesgos — Sesión 7.** Documento utilizado para construir la matriz inicial de riesgos del gimnasio.
- **ISO/IEC 27001:2022.** Sistema de gestión de seguridad de la información y controles de referencia del Anexo A relacionados con acceso e identidad.
- **COBIT 2019.** Marco de gobierno y gestión de la información y tecnología, utilizado como referencia complementaria.
- **Ley 1581 de 2012.** Régimen general de protección de datos personales en Colombia.

**Anexo:** incluir o enlazar la versión vigente de la matriz inicial de riesgos, conservando el identificador R-03 seleccionado en este plan.
