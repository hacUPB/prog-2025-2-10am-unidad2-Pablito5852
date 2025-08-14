# ejercicio 1 : verificacion de pesaje
En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.

## Pseudocodigo
```
LEER peso_aeronave
LEER peso_combustible
LEER peso_carga
LEER limite_max

    peso_total = peso_aeronave + peso_combustible + peso_carga

    SI peso_total <= limite_max ENTONCES
        ESCRIBIR "Listo para despegar. Peso total = ", peso_total
    SINO
        exceso = peso_total - limite_max
        ESCRIBIR "Excede el límite por ", exceso, " kg. Reducir carga/combustible."
    FIN SI
FIN
```
# Ejercicio 2: registro de altitudes en vuelo
Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.

## pseudocodigo
```
INICIO
    DEFINIR altitud COMO REAL
    DEFINIR i COMO ENTERO

    PARA i = 0 HASTA 5 HACER
        ESCRIBIR "Ingrese altitud en el minuto ", (i*10)
        LEER altitud
        ESCRIBIR "Minuto ", (i*10), ": ", altitud, " metros"
    FIN PARA
FIN
```
# Ejercicio 3: deteccion de turbulencias en trayecto
Un sensor mide la aceleración vertical de la aeronave en intervalos de un segundo durante un trayecto de 2 minutos. Si el valor medido supera un umbral, indicar que se ha detectado turbulencia en ese instante. Al final, mostrar cuántas turbulencias se detectaron.
## pseudocodigo
```
umbral = 1.5   
    aceleración_vertical_en_g 
    turbulencias_detectadas = 0

    PARA segundo = 1 HASTA 120 HACER
        LEER  aceleración_vertical_en_g 
        SI  aceleración_vertical_en_g  > umbral ENTONCES
            ESCRIBIR "Turbulencia detectada en segundo ", segundo
            turbulencias_detectadas = turbulencias_detectadas + 1
        FIN SI
    FIN PARA

    ESCRIBIR "Total de turbulencias detectadas: ", turbulencias_detectadas
FIN
```
