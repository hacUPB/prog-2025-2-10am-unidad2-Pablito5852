# pseudocodigo
Inicio
Leer base, altura
Calcular área = (base * altura) / 2
Mostrar área
Fin

# Ejercicio 1

| **Símbolo**         | **Nombre**           | **Forma**       | **Función o Uso**                                                                   |
| ------------------- | -------------------- | --------------- | ----------------------------------------------------------------------------------- |
| 🔵 Inicio / Fin     | Terminal             | Óvalo o Elipse  | Indica el **inicio** o el **final** de un algoritmo.                                |
| 🟩 Proceso          | Proceso              | Rectángulo      | Representa una **acción**, como cálculos o asignación de valores.                   |
| 🟨 Entrada / Salida | Entrada / Salida     | Paralelogramo   | Se utiliza para **leer datos** o **mostrar resultados** al usuario.                 |
| 🔶 Decisión         | Condición / Decisión | Rombo           | Representa una **pregunta lógica**, donde el flujo depende de la respuesta (Sí/No). |
| ⚪ Conector          | Conector             | Círculo pequeño | Se usa para **unir partes** del diagrama cuando hay salto de una parte a otra.      |
| ➡️ Línea de Flujo   | Flujo de proceso     | Flecha          | Indica la **dirección** o el **orden** en que se ejecutan las operaciones.          |


<img width="382" height="635" alt="Captura de pantalla 2025-07-31 104545" src="https://github.com/user-attachments/assets/87e4985a-1173-486b-ae4b-f0c5a9622413" />

# Ejercicio 2
Construye un algoritmo que, al recibir como datos el ID del empleado y los seis primeros sueldos del año, calcule el ingreso total semestral y el promedio mensual, e imprima el ID del empleado, el ingreso total y el promedio mensual.

## Solución 
```
Inicio
Leer ID, S1, S2, S3, S4, S5, S6
Total = S1 + S2 + S3 + S4 + S5 + S6
Promedio = Total / 6
Escribir ID, total, Promedio
Fin
```

### Diagrama de flujo
![Ejercicio 2](<Ejercicio 2.png>)


# Ejercicio 3
Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.

|Variables| Tipo| Comentario|
|---------|-----|----------|
|Lapices  | Entrada| Cantidad de lapices|
|precio  | Salida| Precio total de los lapices|
|Valor_unidad| Intermedia | Valor unitario de cada lapiz|
|85, 90 | Constantes| No cambian|

## Pseudocodigo
```
Inicio
Leer Lapices
Si Lapices >= 1000:
    Valor_unidad = 85
Si no
    Valor_unidad = 90
Fin Si
Precio = Lapices * Valor_unidad
Escribir "El valor total es:", Precio
Fin
