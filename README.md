# Priorix - Proyecto de Diseño y Arquitectura de Software

### Introducción

Este proyecto fue realizado por **Yuly Dayana Rodriguez Salcedo, Juan David Sanchez Roldan y Brayan Presiga Sepulveda** de la carrera de Ingeniería Informática de la Universidad de La Sabana para la asignatura de Diseño y Arquitectura de Software. El objetivo principal es poner en práctica y fortalecer la comprensión de conceptos fundamentales, tales como los atributos de calidad, los principios SOLID, los patrones de diseño, la cohesión y el acoplamiento. Esto se logra a través del planteamiento y desarrollo de una solución a una problemática identificada por los estudiantes, la cual se resuelve mediante la creación de un programa informático.

---

## 1. Presentación del Problema

La vida universitaria suele implicar la acumulación de trabajos y entregas en fechas cercanas, lo que dificulta una adecuada gestión del tiempo y puede afectar el rendimiento académico y el bienestar de los estudiantes. Este proyecto busca abordar esta problemática mediante una aplicación que simplifique la planificación y organización del tiempo destinado a tareas académicas, permitiendo distribuir de manera más eficiente las cargas de trabajo, así como incentivar una constancia en el seguimiento de estos horarios.

[Ver video ilustrativo de la problemática objetivo.](https://youtube.com/shorts/tAdiVAWbGZE?si=CvS60jZ6_VirIGKn)

Con el fin de cumplir este objetivo, se han identificado y planteado los siguientes requerimientos funcionales:

---

## 2. Requerimientos Funcionales y Diagrama de Casos de Uso

### 2.1. Gestión de eventos y tareas

* La aplicación debe permitir agregar diferentes tipos de actividades (eventos, tareas, proyectos, entre otros), las cuales deben poder visualizarse de forma clara dentro de un calendario de forma diaria, semanal o mensual.
* La aplicación debe proporcionar un espacio para definir:

  * El tipo de actividad.
  * El tiempo estimado requerido para completarla.
  * El tiempo máximo que se dedicará de forma continua o el número de espacios máximos para su desarrollo.
  * El nivel de prioridad.
  * Una etiqueta que permita su clasificación.
* La aplicación debe permitir realizar ajustes manuales en la planificación de las actividades.

---

### 2.2. Planificación automática del tiempo

* La aplicación debe permitir definir horarios de disponibilidad para la realización de las actividades.
* La aplicación debe planificar automáticamente los espacios de trabajo dentro de los horarios definidos, teniendo en cuenta:

  * El tiempo máximo por sesión.
  * El número de sesiones definidas por el usuario.
* La aplicación debe permitir definir actividades fijas que no se modifiquen durante la planificación automática.
* La aplicación debe permitir configurar si dichas actividades fijas se repiten semanalmente y establecer una fecha límite para su repetición.
* La aplicación debe alertar al usuario cuando la configuración establecida sea incompatible con la correcta planificación de una actividad y sugerir ajustes necesarios para cumplir con su desarrollo.

---

### 2.3. Seguimiento y estadísticas

* La aplicación debe registrar la finalización de tareas con el fin de generar estadísticas que incentiven la disciplina del usuario.
* La aplicación debe permitir visualizar la constancia mediante:

  * La representación de tareas completadas y pendientes dentro del calendario (por ejemplo, mediante códigos de color).
  * Gráficos con el porcentaje de realización de actividades por día, semana y mes.
  * Una racha de días consecutivos en los que se hayan completado todas las tareas.
  * La evolución de una mascota virtual basada en un sistema de experiencia, obtenida por el uso del modo de enfoque y la finalización de tareas.

---

### 2.4. Modo de concentración y descansos

* La aplicación debe contar con un modo de concentración que permita configurar un cronómetro para marcar el tiempo de trabajo destinado a cada tarea.
* La aplicación debe permitir establecer intervalos de descanso asociados a las sesiones de concentración.

---

### 2.5. Diagrama de Casos de Uso

Finalmente, antes de comenzar con el diseño se construye un diagrama de casos de uso para finalizar la etapa de comprensión de la solución que se buscaba implementar.

_**Imagen del diagrama UML de casos de uso.**_
![Diagrama de Casos de Uso](https://github.com/user-attachments/assets/1a20b1d3-a316-489a-b34f-bb5d9ec24f10)


## 3. Fundamentos de Ingeniería de Software

El sistema prioriza diversos atributos de calidad con el fin de garantizar su correcto funcionamiento, facilidad de uso y capacidad de evolución a lo largo del tiempo. Entre los principales atributos considerados se encuentran:

---

### 3.1. Usabilidad

Dado que el propósito principal de la aplicación es simplificar la planificación y organización del tiempo académico, resulta fundamental que su uso sea intuitivo y fácil de comprender. Por esta razón, se prioriza que los usuarios puedan definir sus actividades, configurar su planificación y realizar ajustes sin enfrentar procesos complejos o confusos, facilitando así su adopción y uso constante en la vida universitaria.

---

### 3.2. Fiabilidad

La fiabilidad es un atributo clave, ya que cualquier falla en el funcionamiento del sistema podría generar desorganización en las actividades académicas y aumentar el estrés del usuario. En este sentido, se busca que la aplicación funcione de manera consistente y que la información registrada se mantenga íntegra, de modo que el estudiante pueda confiar en que su planificación se ejecutará según lo previsto.

---

### 3.3. Mantenibilidad

El sistema se diseña bajo principios de arquitectura modular con el objetivo de facilitar su mantenimiento y evolución a lo largo del tiempo. Esto permitirá realizar mejoras en el motor de planificación automática o incorporar nuevas funcionalidades, como elementos de seguimiento o gamificación, sin afectar el resto del sistema, asegurando así su adaptabilidad a nuevas necesidades o cambios futuros.

---

### 3.4. Rendimiento

Debido a que la aplicación incorpora un motor de planificación automática encargado de distribuir actividades en el tiempo disponible del usuario, el rendimiento se convierte en un factor crítico. Es necesario que el sistema procese esta información de forma eficiente y rápida para evitar interrupciones en la experiencia de uso y garantizar que la automatización represente una ayuda real en la gestión del tiempo.

---

En conjunto, priorizar atributos como la usabilidad, la fiabilidad, la mantenibilidad y el rendimiento permite que la aplicación deje de ser simplemente una agenda digital y pase a comportarse más como un asistente personal. Al combinar una interfaz intuitiva con un sistema de planificación eficiente y mecanismos de gamificación que evolucionan con el uso, el proyecto no solo ayuda a gestionar las entregas académicas, sino que también contribuye a disminuir la carga cognitiva y el estrés propios de la vida universitaria.

---

# 4. Patrones de diseño utilizados

Durante el diseño del sistema surgieron distintos problemas asociados principalmente a la necesidad de mantener la coherencia de la información entre módulos que cumplen funciones diferentes, así como a la posibilidad de adaptar el comportamiento del planificador y de los mecanismos de seguimiento sin comprometer el resto del sistema. A partir de estas necesidades se decidió incorporar ciertos patrones de diseño que permitieran resolver estos inconvenientes de forma desacoplada.

_**Imagen del diagrama UML de clases completo.**_
![Diagrama de Clases](https://github.com/user-attachments/assets/b215433d-0863-4503-91a2-8158d0282359)

---

## 4.1 Singleton

Uno de los primeros retos identificados estaba relacionado con el sistema de gamificación implementado mediante la mascota virtual. Dado que su progreso depende de múltiples factores —como la finalización de tareas, el uso del modo de concentración o el cumplimiento de objetivos diarios—, era necesario que toda la aplicación trabajara siempre sobre el mismo estado de dicha entidad.

Si cada módulo encargado de actualizar el progreso pudiera acceder a instancias distintas de esta mascota, podrían generarse inconsistencias en los valores de experiencia o nivel, afectando directamente el funcionamiento general del sistema. Para evitar este problema, se optó por centralizar la gestión de su estado en una única instancia accesible desde los distintos componentes encargados de registrar el avance del usuario.

De esta manera, la utilización del patrón Singleton permite mantener una única referencia al progreso del usuario a lo largo de todo el sistema.

_**Imagen de la implementación del patron de diseño creacional: Singleton, en la clase Pet, dentro del diagrama UML de clases.**_
<img width="407" height="618" alt="image" src="https://github.com/user-attachments/assets/d9ae4fc6-d6df-43eb-ac6e-8d02299ab4f9" />

---

## 4.2 Strategy

Otro de los problemas fundamentales del sistema estaba relacionado con la necesidad de adaptar el comportamiento de ciertos procesos sin tener que modificar constantemente su implementación principal. Este inconveniente se presentaba especialmente en tres situaciones distintas dentro del diagrama de clases:

* La planificación automática de actividades.
* La gestión de intervalos de trabajo y descanso dentro del modo de concentración.
* La generación de histogramas para visualizar el progreso del usuario.

En cada uno de estos casos, el sistema debía ejecutar una tarea específica (planificar, temporizar o representar métricas), pero existían múltiples formas válidas de hacerlo dependiendo de las preferencias del usuario o del contexto de uso.

Por ejemplo, dentro del planificador podían aplicarse distintos criterios de organización de actividades, mientras que el temporizador debía permitir implementar diferentes técnicas de concentración. De forma similar, los histogramas encargados de representar el progreso podían variar según la métrica que se deseara visualizar.

Para resolver este problema se decidió encapsular estas variaciones de comportamiento en componentes independientes que pudieran intercambiarse sin alterar la lógica de los módulos que los utilizan. Así, tanto el planificador como el temporizador o el generador de estadísticas pueden modificar su funcionamiento interno sin necesidad de cambiar su estructura general.

_**Imagen de la implementación del patron de diseño de comportamiento: Strategy, para el planificador, dentro del diagrama UML de clases.**_
<img width="1032" height="737" alt="image" src="https://github.com/user-attachments/assets/193b159e-cd53-4925-9311-738078c74d3e" />

---

_**Imagen de la implementación del patron de diseño de comportamiento: Strategy, para el modo de concetración, dentro del diagrama UML de clases.**_
<img width="1201" height="764" alt="image" src="https://github.com/user-attachments/assets/596abcab-ff73-45fb-958d-466a13362c27" />

---

_**Imagen de la implementación del patron de diseño de comportamiento: Strategy, para la generación de los histogramas, dentro del diagrama UML de clases.**_
<img width="1832" height="780" alt="image" src="https://github.com/user-attachments/assets/c638f610-8b8e-4e0e-b00b-4d6e617f8604" />

---

## 4.3 Observer

A medida que se definía el comportamiento del sistema, se hizo evidente que muchas acciones realizadas por el usuario no tenían un único efecto dentro de la aplicación. Un ejemplo claro de esto ocurre cuando una actividad es marcada como completada.

Este evento no solo afecta el estado de la actividad en sí misma, sino que también implica actualizar los indicadores visuales del calendario, registrar información para las estadísticas diarias y modificar el progreso asociado a la mascota virtual.

Inicialmente, esto suponía que el módulo encargado de gestionar las actividades debía comunicarse directamente con todos aquellos componentes que dependían de estos cambios, generando un alto nivel de acoplamiento entre ellos. Para evitar este problema, se optó por implementar un mecanismo de notificación que permitiera a los distintos módulos reaccionar ante cambios en el estado de una actividad sin necesidad de establecer dependencias directas entre ellos.

De esta forma, el sistema encargado de gestionar las actividades simplemente informa cuando ocurre una modificación relevante, permitiendo que los módulos de seguimiento o gamificación respondan de manera independiente.

_**Imagen de la implementación del patron de diseño de comportamiento: Observer, para la completitud de tareas, dentro del diagrama UML de clases.**_
<img width="1189" height="782" alt="image" src="https://github.com/user-attachments/assets/e277d419-9353-4063-a624-e90be4bfcb75" />

---

## 4.4 Factory Method

Finalmente, durante el diseño de la visualización del calendario surgió la necesidad de representar la información de distintas formas, como vistas diarias, semanales o mensuales. Aunque todas estas representaciones comparten el mismo propósito, su construcción varía dependiendo del tipo de visualización requerido.

Incorporar directamente la lógica de creación de estas vistas dentro de los componentes que las utilizan habría generado dependencias innecesarias y dificultado la incorporación de nuevas formas de representación en el futuro. Por esta razón, se decidió delegar este proceso de creación a componentes especializados encargados de generar la vista adecuada según el contexto.

_**Imagen de la implementación del patron de diseño creacional: Facthory Method, para la creación de los diferentes estilos de visualización de las tareas, dentro del diagrama UML de clases.**_
<img width="1507" height="755" alt="image" src="https://github.com/user-attachments/assets/ea8084b1-d2fe-4e14-bca4-b2f8df8f8dea" />

---

# 5. Aplicación de Principios SOLID en el Sistema

---

## 5.1. Principio de Responsabilidad Única (SRP)

Dentro del sistema, cada componente ha sido diseñado para cumplir con una única función claramente definida. La lógica encargada de gestionar la creación y el estado de las actividades académicas se encuentra separada de aquella que administra su planificación, seguimiento o representación gráfica.

De igual manera, la gestión del progreso asociado a los elementos de gamificación se concentra en un único componente responsable de mantener su estado, mientras que el cálculo de estadísticas o la actualización de indicadores visuales se delega a módulos independientes que reaccionan ante los cambios en el sistema.

Esta separación de responsabilidades contribuye directamente al atributo de **mantenibilidad**, ya que facilita la modificación o mejora de un componente sin afectar el resto del sistema, y al de **fiabilidad**, al reducir la probabilidad de errores derivados de responsabilidades compartidas entre módulos.

---

## 5.2. Principio de Abierto/Cerrado (OCP)

El sistema ha sido estructurado de manera que sus funcionalidades puedan ampliarse sin necesidad de modificar el comportamiento previamente implementado. En este sentido, es posible incorporar nuevos criterios de planificación automática, nuevas métricas de seguimiento o nuevas técnicas de gestión del tiempo sin alterar los módulos existentes que utilizan estas funcionalidades.

Este principio se evidencia en el funcionamiento del motor de planificación automática, el generador de estadísticas y el modo de concentración, los cuales han sido diseñados para trabajar con diferentes estrategias intercambiables.

La aplicación de este principio favorece la **mantenibilidad** del sistema, al permitir su evolución sin comprometer su estabilidad, y la **escalabilidad funcional**, al facilitar la incorporación de nuevas metodologías de organización del tiempo o visualización del progreso.

---

## 5.3. Principio de Inversión de Dependencias (DIP)

Los componentes principales del sistema dependen de abstracciones que definen comportamientos generales, en lugar de depender directamente de implementaciones específicas. Esto se evidencia en el funcionamiento del planificador de actividades, el generador de estadísticas y el temporizador del modo de concentración, cuya lógica se apoya en contratos que representan distintas estrategias de organización, cálculo o temporización.

Como resultado, la incorporación de nuevas formas de planificación del tiempo, cálculo de métricas de progreso o gestión de intervalos de trabajo y descanso no requiere modificar el funcionamiento interno de estos componentes, sino únicamente proporcionar una nueva implementación que cumpla con el comportamiento esperado.

Este enfoque contribuye a la **flexibilidad**, **mantenibilidad** y **portabilidad** del sistema, permitiendo su adaptación a nuevos requerimientos funcionales sin afectar la lógica principal.

---

# 6. Análisis técnico del diseño propuesto

Al observar el sistema en conjunto, es posible notar que muchas de las decisiones tomadas durante su diseño no solo buscaban resolver problemas funcionales inmediatos, sino también priorizar atributos de calidad como la mantenibilidady la fiabilidad, evitando que el crecimiento del sistema terminara generando dependencias innecesarias entre sus componentes.

Por ejemplo, al separar claramente la representación de las actividades de su planificación, o al diferenciar los módulos encargados de gestionar el progreso del usuario de aquellos que administran el tiempo de trabajo, se logró que cada parte del sistema tuviera un propósito bastante específico. Esto impacta directamente en el atributo de mantenibilidad, ya que permite comprender con mayor facilidad el rol de cada componente dentro del sistema. A su vez, esta decisión contribuye a mantener una alta cohesión, dado que clases como AActivity, Planner, Timer, Pet o DailySummary concentran su comportamiento en torno a una única responsabilidad bien definida.

Esta forma de organizar el sistema también influye en la fiabilidad, ya que al evitar que una misma clase asuma múltiples funciones, se reduce la probabilidad de errores derivados de responsabilidades mezcladas. Desde el punto de vista estructural, esto disminuye el acoplamiento funcional entre módulos que, de otro modo, tendrían que interactuar de forma más estrecha para cumplir tareas relacionadas.

De manera similar, el hecho de que el planificador, el temporizador y los módulos encargados de generar histogramas trabajen con comportamientos intercambiables permite priorizar nuevamente la mantenibilidad del sistema. Gracias a esto, es posible modificar o extender la forma en que se organizan las actividades, se gestionan los intervalos de trabajo o se visualiza el progreso sin afectar el funcionamiento de las clases que dependen de estos procesos. Esta independencia reduce el acoplamiento estructural, ya que dichos componentes no están ligados a implementaciones específicas.

Algo parecido ocurre con el manejo de cambios en el estado de las actividades. Cuando una tarea es completada, distintos elementos del sistema necesitan reaccionar ante este evento, como el registro de estadísticas o la actualización del progreso del usuario. Sin embargo, esta comunicación se realiza sin que exista una relación directa entre todos los módulos involucrados. Esto contribuye tanto a la fiabilidad, al asegurar que todos los componentes se mantengan sincronizados, como a la mantenibilidad, al evitar dependencias rígidas entre ellos. Desde el punto de vista del diseño, esta decisión tiene un impacto claro en la reducción del acoplamiento, ya que permite que los módulos reaccionen de forma independiente ante un mismo cambio de estado.

Finalmente, al centralizar la gestión del progreso del usuario en un único componente, se prioriza la fiabilidad del sistema al garantizar que todos los módulos trabajen sobre una misma fuente de información. Esta centralización evita que distintas partes de la aplicación mantengan copias independientes del mismo estado, lo cual no solo mejora la coherencia de los datos, sino que también limita la cantidad de relaciones necesarias entre componentes, reduciendo nuevamente el acoplamiento entre ellos.

Adicionalmente, esta distribución clara de responsabilidades también tiene un impacto sobre la usabilidad del sistema. Al concentrar gran parte de la interacción del usuario en la creación y configuración de las actividades, el funcionamiento general de la aplicación se simplifica, ya que el usuario únicamente necesita comprender cómo definir sus tareas para poder hacer uso efectivo del planificador, el modo de concentración o los mecanismos de seguimiento. Esta simplicidad en la funcionalidad principal reduce la carga cognitiva durante el uso de la aplicación, permitiendo que el resto de los módulos operen de forma transparente sin requerir una intervención constante por parte del usuario.

En conjunto, estas decisiones permiten que el sistema mantenga una estructura donde se priorizan atributos de calidad como la mantenibilidad, la fiabilidad y la usabilidad, apoyándose en una alta cohesión interna de las clases y un bajo nivel de acoplamiento entre los distintos módulos, facilitando su mantenimiento, reduciendo la posibilidad de errores derivados de interacciones complejas y permitiendo su evolución sin comprometer su funcionamiento general.

---

# 7. Créditos y Roles

* Yuly Dayana Rodriguez Salcedo - Prototipado en Figma y Elaboración Video respecto al planteamiento de la Problemática
* Juan David Sanchez Roldan - Documentación y Diseño de Diagrama UML de Casos de Uso
* Brayan Presiga Sepulveda - Documentación y Diseño de Diagrama UML de Clases



