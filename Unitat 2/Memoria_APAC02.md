# Memòria Apac02 - Gestió d'incidencies v1.0
Partint de l'anterior practica del login he anat creant lo que anava necesitant per a la aplicacio seguint la documentacio del exemple de "Contactes",
però intentant posar coses com el *MaterialCardView* i la activitat d'edicio d'incidencies amb un *ScrollView"

La aplicacio del Login sols tenia un MainActivity y un altra activity per donar la venvinguda, els pasos que he seguit en
aquesta aplicacio han sigut
- Crear un nou projecte "APAC02"
- Copiar el codi del login cambiant en el activity_main l'imatge de capçalera.
- Crear **ListaIncidencias**, on apareixen totes les incidencies que hi han enmagatzenades.
- Crear el *layout* per a **incidencia_layout** per a que se carregue en la llista d'incidencies amb el diseny configurat.
- Copiar dels recursos **Incidencia.kt**
- Crear **IncidenciaViewHolder**
- Crear el Adaptador **AdaptadorIncidencias.kt**
- Modificar alguns dels arxius per a gestionar els esdeveniments del click i click llarg
- Crear l'activitat d'edicio d'incidencies **EditaIncidencia.kt**

El que mes m'ha costat es fer cuadrar els objectes dins del scrollview o del materialCardView, ja que no m'apareixen punt d'anclatje per a poderho fer de forma
mes sencilla. TAmbe he tingut un problema amb l'espiner, ja qeu al copiarlo al directori res/values el ha ficat dins dùn tema
i m'ha donat problemes. Tampoc savia com ficar l'opcio del menu per a crear una nova incidencia en la barra de l'aplicacio,
però al final seguint els apunt era mes sencill de lo que pareixia.
