PROGRAMA \--\> LISTA\_FUNCIONES LISTA\_SENTENCIAS

LISTA\_FUNCIONES \--\> LISTA\_FUNCIONES FUNCION

LISTA\_FUNCIONES \--\> FUNCION

FUNCION \--\> **funcion** ID **(** LISTA\_ARGUMENTOS **)** LISTA\_SENTENCIAS **retorno (** E **)** **end function**

FUNCION \--\>  ~~epsilon~~

LISTA\_ARGUMENTOS \--\> LISTA\_ARGUMENTOS **,** ARGUMENTO

LISTA\_ARGUMENTOS \--\> ARGUMENTO

ARGUMENTO \--\> ID

LISTA\_SENTENCIAS \--\> SENTENCIA

LISTA\_SENTENCIAS \--\> LISTA\_SENTENCIAS SENTENCIA

SENTENCIA \--\> E **;**

SENTENCIA \--\> A **;**

SENTENCIA \--\> LEER **;**

SENTENICA \--\> ESCRIBIR **;**

SENTENCIA \--\> CONDICIONAL

SENTENCIA \--\> CICLO

SENTENCIA \--\> IMPORTAR

SENTENCIA \--\> ASIGNACION

CONDICIONAL \--\> IF

CONDICIONAL \--\> IF\_ELSE

IF \--\> **if (** CONDICION\_BOOLEANA **) {** LISTA\_SENTENCIAS **}**

IF \--\> **if (** CONDICION\_BOOLEANA **)** SENTENCIA

IF\_ELSE \--\> IF LISTA\_ELSE\_IF **else** SENTENCIA

IF\_ELSE \--\> IF LISTA\_ELSE\_IF **else {** LISTA\_SENTENCIAS **}**

LISTA\_ELSE\_IF \--\> LISTA\_ELSE\_IF **else if (** CONDICION\_BOOLEANA
**)** SENTENCIA

LISTA\_ELSE\_IF \--\> LISTA\_ELSE\_IF **else if (** CONDICION\_BOOLEANA
**) {** LISTA\_SENTENCIAS **}**

LISTA\_ELSE\_IF \--\> ~~epsilon~~

CONDICION\_BOOLEANA \--\> CONDICION\_LOGICA

CONDICION\_BOOLEANA \--\> CONDICION\_AND

CONDICION\_BOOLEANA \--\> CONDICION\_OR

CONDICION\_AND \--\> CONDICION\_BOOLEANA **&&** CONDICION\_BOOLEANA

CONDICION\_OR \--\> CONDICION\_BOOLEANA **\|\|** CONDICION\_BOOLEANA

CONDICION\_LOGICA \--\> E **\>** E

CONDICION\_LOGICA \--\> E **\>=** E

CONDICION\_LOGICA \--\> E **\<** E

CONDICION\_LOGICA \--\> E **\<=** E

CONDICION\_LOGICA \--\> E **==** E

CONDICION\_LOGICA \--\> E **¡=** E

CICLO \--\> CICLO\_FOR

CICLO \--\> CICLO\_WHILE

CICLO\_FOR \--\> **for** ID **in** ARRAY **{** LISTA\_SENTENCIAS **}**

CICLO\_WHILE \--\> **while (** CONDICION\_BOOLEANA **)** **{**
LISTA\_SENTENCIAS **}**

CICLO\_WHILE \--\> **while (** CONDICION\_BOOLEANA **)** SENTENCIA

IMPORTAR \--\> **importar** RUTA

IMPORTAR \--\> **desde** ID **importar** RUTA

RUTA \--\> RUTA **.** ID

RUTA \--\> ID

ASIGNACION \--\> ID **=** A

LEER \--\> **leer(** ID **)**

ESCRIBIR \--\> **log (** E **)**

ARRAY \--\> **\[** LISTA\_E **\]**

LISTA\_E \--\> LISTA\_E **,** E

LISTA\_E \--\> E

ESTRUCTURA \--\> **{** LISTA\_MIEMBROS **}**

LISTA\_MIEMBROS \--\> LISTA\_MIEMBROS **,** MIEMBRO

LISTA\_MIEMBROS \--\> MIEMBRO

MIEMBRO \--\> ID **:** E

A \--\> ARRAY

A \--\> ESTRUCTURA

A \--\> STRING

A \--\> CONDICION\_BOOLEANA

E \--\> E **+** T

E \--\> E **--** T

E \--\> ACCESO\_ARRAY

E\--\> ACCESO\_ESTRUCTURA

E \--\> **nill**

E \--\> T

E \--\> **true**

E \--\> **false**

T \--\> T **\*** F

T \--\> T **/** F

T \--\> F

F \--\> ID

ACCESO\_ARRAY \--\> ID **\[** E **\]**

ACCESO\_ESTRUCTURA \--\> ID **.** ID

ID \--\> identificador

F \--\> constante

STRING \--\> cadena\_texto
