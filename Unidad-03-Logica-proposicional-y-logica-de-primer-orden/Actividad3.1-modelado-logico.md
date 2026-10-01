Actividad de aprendizaje — 3.1 Lógica proposicional y lógica de primer orden
Unidad 3. Representación del conocimiento y razonamiento
Nombre de la actividad
Modelado lógico de un dominio y derivación de conocimiento
Propósito
Aplicar lógica proposicional y lógica de primer orden para representar conocimiento de un dominio acotado, distinguiendo hechos, relaciones, reglas y conclusiones derivadas.
La actividad busca que el estudiante comprenda que la lógica en Inteligencia Artificial no se utiliza únicamente para verificar fórmulas, sino como un lenguaje formal para construir bases de conocimiento sobre las cuales posteriormente pueden realizarse procesos de inferencia.
________________________________________
Situación de trabajo
Se utilizará como dominio principal una pequeña red informática.
Considere los siguientes elementos:
a) PC1, PC2 y PC3 son equipos
b) Router1 y Router2 son routers
c) PC1 y PC2 están conectados a Router1
d) PC3 está conectado a Router2
e) Router1 está operativo
f) Router2 no está operativo
g) Todo equipo conectado a un router operativo tiene acceso a la red
h) Todo equipo con acceso a la red puede utilizar los servicios institucionales
________________________________________
Instrucciones
Parte 1. Identificación del conocimiento
Clasifique la información del dominio en:
a) Objetos
Los objetos representan las entidades individuales que existen dentro del dominio.
Objeto	Tipo
PC1	Equipo
PC2	Equipo
PC3	Equipo
Router1	Router
Router2	Router

b) Propiedades
Las propiedades describen características de los objetos.
En este dominio tenemos:
•	Router1 está operativo.
•	Router2 no está operativo.
•	PC1 es un equipo.
•	PC2 es un equipo.
•	PC3 es un equipo.
•	Router1 es un router.
•	Router2 es un router.
Una propiedad puede expresarse mediante un predicado de un solo argumento, por ejemplo:
Operativo(Router1)
que significa que Router1 está operativo.
c) Relaciones
Las relaciones indican cómo se vinculan dos o más objetos.
En este dominio tenemos:
•	PC1 está conectado a Router1.
•	PC2 está conectado a Router1.
•	PC3 está conectado a Router2.


Estas relaciones pueden representarse mediante el predicado:
Conectado(PC1, Router1)
La relación involucra dos objetos: un equipo y un router.
d) Reglas
Las reglas representan conocimiento general que permite obtener nuevas conclusiones.
La primera regla es:
Si un equipo está conectado a un router operativo, entonces tiene acceso a la red.
La segunda regla es:
Si un equipo tiene acceso a la red, entonces puede utilizar los servicios institucionales.
Estas reglas son importantes porque permiten obtener conocimiento que no se encuentra almacenado directamente como un hecho.

Presente una explicación breve de cada categoría e indique por qué cada elemento pertenece a ella.
________________________________________
Parte 2. Representación mediante lógica proposicional
Seleccione al menos seis afirmaciones del dominio y represéntelas mediante proposiciones.
Ejemplo:
[ R1 = ext{Router1 está operativo} ]
Posteriormente formule al menos dos reglas proposicionales utilizando conectores lógicos.
Ejemplo:
[ (C1 \land R1) ightarrow A1 ]
Explique con lenguaje natural qué representa cada fórmula:
En lógica proposicional cada afirmación completa se representa mediante un símbolo que puede ser verdadero o falso.
Se pueden definir las siguientes proposiciones:
Símbolo	Proposición
E1	PC1 es un equipo
E2	PC2 es un equipo
E3	PC3 es un equipo
R1	Router1 es un router
R2	Router2 es un router
O1	Router1 está operativo
¬O2	Router2 no está operativo
C1	PC1 está conectado a Router1
C2	PC2 está conectado a Router1
C3	PC3 está conectado a Router2
A1	PC1 tiene acceso a la red
A2	PC2 tiene acceso a la red
A3	PC3 tiene acceso a la red
S1	PC1 puede utilizar los servicios institucionales
S2	PC2 puede utilizar los servicios institucionales
S3	PC3 puede utilizar los servicios institucionales
Se han seleccionado más de seis afirmaciones para mostrar de manera más completa el dominio.
Regla proposicional 1
Podemos representar el acceso de PC1 mediante:
(C1 ∧ O1) → A1
Esta expresión significa:
Si PC1 está conectado a Router1 y Router1 está operativo, entonces PC1 tiene acceso a la red.
Para PC2:
(C2 ∧ O1) → A2
Para PC3:
(C3 ∧ O2) → A3
Sin embargo, como sabemos que Router2 no está operativo, no podemos afirmar O2.
Regla proposicional 2
La segunda regla general del dominio puede representarse mediante:
A1 → S1
y:
A2 → S2
y:
A3 → S3
Estas expresiones significan:
Si un equipo tiene acceso a la red, entonces puede utilizar los servicios institucionales.
Observación
La principal característica de esta representación es que cada equipo requiere proposiciones y reglas particulares.
Por ejemplo, para tres equipos tenemos que definir A1, A2 y A3.
Esto funciona correctamente para un dominio pequeño, pero se vuelve poco práctico cuando aumenta considerablemente el número de equipos.

________________________________________
Parte 3. Representación mediante lógica de primer orden
Reformule el dominio utilizando:
a) Constantes
Las constantes representan objetos concretos del dominio:
PC1, PC2, PC3, Router1, Router2
Cada una identifica una entidad específica.
b) Predicados
Se utilizarán los siguientes predicados:
•	Equipo(x): x es un equipo.
•	Router(x): x es un router.
•	Operativo(x): x está operativo.
•	Conectado(x,y): x está conectado a y.
•	TieneAcceso(x): x tiene acceso a la red.
•	UsaServicios(x): x puede utilizar los servicios institucionales.

c) Variables
x,y
d) Cuantificador universal
∀
e) Cuantificador existencial
∃
Incluya como mínimo:
a) Cinco hechos
Equipo(PC3)
Router(Router1)
Router(Router2)
Conectado(PC1, Router1)
Conectado(PC2, Router1)

b) Dos relaciones
Las principales relaciones del dominio son:
Conectado(PC1, Router1)
y:
Conectado(PC2, Router1)
También:
Conectado(PC3, Router2)
El predicado Conectado(x,y) representa una relación entre un equipo y un router.

c) Dos reglas generales con cuantificador universal
La regla:
Todo equipo conectado a un router operativo tiene acceso a la red.
puede representarse mediante:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ Operativo(r)) → TieneAcceso(x))
La expresión se interpreta de la siguiente manera:
•	∀x: para cualquier objeto x.
•	∀r: para cualquier objeto r.
•	Equipo(x): x debe ser un equipo.
•	Router(r): r debe ser un router.
•	Conectado(x,r): x debe estar conectado a r.
•	Operativo(r): el router debe estar operativo.
•	TieneAcceso(x): como consecuencia, el equipo tiene acceso.
La ventaja es que una sola regla puede utilizarse para PC1, PC2, PC3 o cualquier otro equipo que posteriormente se incorpore al sistema.

d) Una expresión que utilice cuantificador existencial.
El cuantificador existencial ∃ permite expresar que existe al menos un objeto que cumple una determinada condición.
En nuestro dominio podemos expresar:
∃x (Equipo(x) ∧ Conectado(x, Router2))
Esta expresión significa:
Existe al menos un equipo conectado a Router2.
Sabemos que la afirmación es verdadera porque:
Conectado(PC3, Router2)
y:
Equipo(PC3)
Por lo tanto, PC3 constituye al menos un ejemplo que satisface la expresión existencial.
También podemos expresar:
∃r (Router(r) ∧ ¬Operativo(r))
que significa:
Existe al menos un router que no está operativo.
Esta expresión también es verdadera porque:
Router(Router2)
y:
¬Operativo(Router2)

Ejemplo de regla:
[ orall x orall r ((Equipo(x) \land Router(r) \land Conectado(x,r) \land Operativo(r))
ightarrow TieneAcceso(x)) ]
________________________________________

Parte 4. Derivación de conocimiento
A partir de los hechos y reglas definidos, determine qué conclusiones pueden derivarse.
Analice al menos los siguientes casos:
a) ¿PC1 tiene acceso a la red?
Tenemos los siguientes hechos:
Equipo(PC1)
Router(Router1)
Conectado(PC1, Router1)
Operativo(Router1)
Aplicamos la regla:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ Operativo(r)) → TieneAcceso(x))
Sustituyendo:
•	x = PC1
•	r = Router1
obtenemos:
TieneAcceso(PC1)
Conclusión
PC1 tiene acceso a la red.
Posteriormente, mediante la segunda regla:
TieneAcceso(PC1) → UsaServicios(PC1)
también podemos concluir:
UsaServicios(PC1)
Por lo tanto, PC1 puede utilizar los servicios institucionales.

b) ¿PC2 tiene acceso a la red?
Tenemos:
Equipo(PC2)
Router(Router1)
Conectado(PC2, Router1)
Operativo(Router1)
Aplicando nuevamente la regla general:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ Operativo(r)) → TieneAcceso(x))
sustituimos:
•	x = PC2
•	r = Router1
Obtenemos:
TieneAcceso(PC2)
Conclusión
PC2 tiene acceso a la red.
Aplicando la segunda regla:
TieneAcceso(PC2) → UsaServicios(PC2)
también podemos concluir:
UsaServicios(PC2)

c) ¿PC3 tiene acceso a la red?
Tenemos:
Equipo(PC3)
Router(Router2)
Conectado(PC3, Router2)
pero también:
¬Operativo(Router2)
La regla de acceso exige:
Operativo(Router2)
Sin embargo, el conocimiento disponible indica precisamente lo contrario:
¬Operativo(Router2)
Por lo tanto, no se cumplen todas las condiciones necesarias para aplicar la regla.
Conclusión
No puede derivarse que PC3 tenga acceso a la red a partir de la base de conocimiento proporcionada.
Es importante expresar esta conclusión correctamente.
No debemos confundir:
"No se puede demostrar que PC3 tenga acceso"
con:
"Se ha demostrado que PC3 no tiene acceso."
En este dominio, el hecho de que Router2 no esté operativo hace razonable modelar que PC3 no tiene acceso, pero la regla proporcionada solamente permite derivar acceso cuando el router está operativo.
Si quisiéramos representar formalmente la regla adicional:
Un equipo conectado a un router que no está operativo no tiene acceso.
podríamos definir:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ ¬Operativo(r)) → ¬TieneAcceso(x))
Con esta regla adicional sí podríamos derivar formalmente:
¬TieneAcceso(PC3)

d) ¿Existe algún equipo conectado a un router no operativo?
Tenemos:
Equipo(PC3)
Conectado(PC3, Router2)
Router(Router2)
¬Operativo(Router2)
Podemos expresar la consulta mediante:
∃x∃r (Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ ¬Operativo(r))
La expresión es verdadera porque existen:
•	x = PC3
•	r = Router2
Por lo tanto:
Existe al menos un equipo conectado a un router no operativo.
El ejemplo que satisface la condición es:
PC3 conectado a Router2.

Para cada respuesta indique:
a) Hechos utilizados
b) Regla aplicada
c) Conclusión obtenida

Resumen de las derivaciones
Consulta	Hechos utilizados	Regla	Conclusión
PC1 tiene acceso	PC1 conectado a Router1 + Router1 operativo	Regla de acceso	TieneAcceso(PC1)
PC2 tiene acceso	PC2 conectado a Router1 + Router1 operativo	Regla de acceso	TieneAcceso(PC2)
PC3 tiene acceso	PC3 conectado a Router2 + Router2 no operativo	La regla no puede activarse	No se deriva TieneAcceso(PC3)
Existe equipo conectado a router no operativo	PC3 conectado a Router2 + Router2 no operativo	Cuantificador existencial	La existencia queda demostrada

________________________________________
Parte 5. Comparación entre representaciones
Explique brevemente:
a) Qué información resultó más sencilla de representar con lógica proposicional
La lógica proposicional resulta sencilla para representar hechos concretos.
Por ejemplo:
O1 = Router1 está operativo
C1 = PC1 está conectado a Router1
A1 = PC1 tiene acceso a la red
Estas proposiciones son fáciles de comprender y manipular cuando el dominio es pequeño.
La principal ventaja es su simplicidad.
Sin embargo, cada situación debe representarse mediante proposiciones independientes.

b) Qué ventajas presentó la lógica de primer orden
La lógica de primer orden permite representar explícitamente:
•	objetos;
•	propiedades;
•	relaciones;
•	variables;
•	reglas generales;
•	cuantificadores.
Por ejemplo:
Conectado(PC1, Router1)
representa directamente la relación entre dos objetos.
Además:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ Operativo(r)) → TieneAcceso(x))
permite expresar una regla general aplicable a cualquier equipo y cualquier router.
Esto evita crear una regla independiente para cada equipo.
________________________________________

c) Qué problemas aparecerían si el dominio tuviera 1,000 equipos y 100 routers
En lógica proposicional el número de proposiciones y reglas aumentaría considerablemente.
Por ejemplo, podrían ser necesarias proposiciones como:
C1, C2, C3, ..., C1000
para representar diferentes conexiones.
También serían necesarias muchas reglas particulares para determinar el acceso de cada equipo.
Esto provocaría:
•	mayor cantidad de símbolos;
•	mayor cantidad de reglas;
•	mayor dificultad para mantener la base de conocimiento;
•	mayor posibilidad de errores;
•	menor reutilización del conocimiento.
En cambio, mediante lógica de primer orden una sola regla general puede aplicarse a los 1,000 equipos y 100 routers.

d) Por qué una regla con variables y cuantificadores es más reutilizable que múltiples reglas proposicionales particulares
Porque no está asociada a un objeto específico.
Por ejemplo:
∀x∀r ((Equipo(x) ∧ Router(r) ∧ Conectado(x,r) ∧ Operativo(r)) → TieneAcceso(x))
no menciona específicamente a PC1, PC2 o PC3.
La variable x puede representar cualquier equipo y la variable r cualquier router.
Por lo tanto, la misma regla puede utilizarse cuando se agreguen:
•	PC4;
•	PC5;
•	PC100;
•	PC1000;
•	Router3;
•	Router4;
•	Router100.
Esta capacidad de generalización constituye una de las principales ventajas de la lógica de primer orden frente a la lógica proposicional.

________________________________________
Parte 6. Extensión del dominio
Incorpore al menos dos nuevos elementos al dominio.
Puede agregar, por ejemplo:
a) Servidores
b) Usuarios
c) Servicios
d) Puntos de acceso
e) Switches
Defina al menos una nueva relación y una nueva regla de primer orden.
Después explique qué nuevo conocimiento podría derivarse.
Para ampliar el dominio se incorporarán dos nuevos elementos:
•	Servidor1
•	Usuario1
También se agregará una nueva relación:
Accede(Usuario, Servidor)
que representa que un usuario puede acceder a un servidor.
Nuevos hechos
Podemos agregar:
Servidor(Servidor1)
Usuario(Usuario1)
UsaServicios(PC1)
También podemos establecer:
Accede(Usuario1, Servidor1)
Nueva relación
La relación:
Accede(Usuario1, Servidor1)
significa:
Usuario1 accede a Servidor1.
Esta relación permite conectar objetos de diferentes tipos dentro del dominio.
________________________________________
Nueva regla de primer orden
Podemos establecer la siguiente regla:
Todo usuario que pueda acceder a un equipo con acceso a la red puede utilizar los servicios institucionales.
Una forma simplificada de representar una regla relacionada con los usuarios sería:
∀u∀s ((Usuario(u) ∧ Servidor(s) ∧ Accede(u,s)) → PuedeUsarServicio(u))
donde:
•	Usuario(u) identifica a un usuario.
•	Servidor(s) identifica a un servidor.
•	Accede(u,s) representa la relación entre el usuario y el servidor.
•	PuedeUsarServicio(u) indica que el usuario puede utilizar los servicios.
Nuevo conocimiento derivable
Si tenemos:
Usuario(Usuario1)
Servidor(Servidor1)
Accede(Usuario1, Servidor1)
entonces, mediante la regla anterior, podemos concluir:
PuedeUsarServicio(Usuario1)
Esto demuestra cómo una base de conocimiento puede ampliarse incorporando nuevos objetos, relaciones y reglas sin tener que modificar las reglas existentes.

________________________________________
Producto a entregar
El estudiante deberá entregar un documento breve o archivo Markdown que incluya:
a) Descripción del dominio
b) Identificación de objetos, propiedades, relaciones y reglas
c) Representación proposicional
d) Representación en lógica de primer orden
e) Derivaciones realizadas
f) Comparación entre ambos tipos de lógica
g) Extensión propuesta
h) Reflexión final
Extensión sugerida: 3 a 5 páginas, sin considerar portada ni referencias.
________________________________________
Evidencia de aprendizaje esperada
Al finalizar la actividad, el estudiante deberá ser capaz de:
a) Traducir conocimiento expresado en lenguaje natural a representaciones lógicas
b) Distinguir entre proposiciones, predicados, objetos, relaciones y cuantificadores
c) Formular reglas generales mediante lógica de primer orden
d) Derivar conclusiones a partir de hechos y reglas
e) Analizar las ventajas y limitaciones de diferentes formas de representación lógica
________________________________________
Criterios de evaluación
Criterio	Descripción	Ponderación
Identificación del conocimiento	Distingue correctamente objetos, propiedades, relaciones y reglas	15 %
Lógica proposicional	Representa correctamente hechos y reglas mediante proposiciones	20 %
Lógica de primer orden	Utiliza adecuadamente predicados, variables y cuantificadores	30 %
Derivación de conclusiones	Justifica correctamente las conclusiones obtenidas	20 %
Comparación y reflexión	Analiza diferencias, ventajas y limitaciones de ambas representaciones	10 %
Presentación	Entrega clara, organizada y con notación consistente	5 %
Total: 100 %
________________________________________
Preguntas de reflexión final
Responda brevemente:
a) ¿Qué diferencia existe entre almacenar un hecho y representar conocimiento?
b) ¿Por qué la lógica de primer orden resulta más adecuada para dominios con múltiples objetos y relaciones?
c) ¿Qué conocimiento se encontraba explícitamente en la base y cuál tuvo que derivarse?
d) ¿Qué limitaciones tendría este modelo para representar información incompleta o incierta?
La última pregunta servirá como conexión con el subtema 3.4 Razonamiento no monótono e incierto.

Reflexión Final:
La actividad permitió observar que la lógica puede utilizarse en Inteligencia Artificial como mecanismo para representar conocimiento y no solamente para evaluar expresiones lógicas.
La lógica proposicional permite representar de manera sencilla hechos concretos, pero presenta limitaciones cuando el número de objetos y relaciones aumenta. El cambio la lógica de primer orden permite representar objetos mediante constantes. Relaciones mediante predicados, y conocimiento general mediante variables y cuantificadores.





