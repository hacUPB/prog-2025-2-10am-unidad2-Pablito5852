# actividad 
1. archivo txt: 52,38 KB
2. datos punto flotante: 21,73 KB
3. datos enteros: 13,47 KB

Total:87,65 KB

EJERCICIOS FINALES DE REPASO

1. Explica, en tus propias palabras, por qué es necesario que las computadoras representen los datos en binario.

- Las computadoras necesitan representar los datos en binario porque están hechas de circuitos electrónicos que solo pueden detectar dos estados: encendido (1) y apagado (0). Estos dos estados se representan perfectamente con el sistema binario, que solo usa esos dos dígitos: 0 y 1.

A diferencia de nosotros, que usamos el sistema decimal (con diez números), los computadores no tienen manera física de representar más de dos estados de forma rápida, confiable y económica. Así que todo números, letras, imágenes, sonidos se convierte en una combinación de ceros y unos que los circuitos pueden leer, procesar y almacenar.

2. Convierte el número binario 10011011 a decimal y a hexadecimal.

- Colocamos los pesos de cada posición
  1   0   0   1   1   0   1   1
128   64 32   16  8   4   2   1
  Multiplicamos cada dígito por su peso y sumamos
  (1×128) + (0×64) + (0×32) + (1×16) + (1×8) + (0×4) + (1×2) + (1×1)
= 128 + 0 + 0 + 16 + 8 + 0 + 2 + 1
= **155**
Resultado en decimal: 155
-HEXADECIMAL:
Agrupamos el número binario en bloques de 4 bits, desde la derecha:
1001 1011
Ahora convertimos cada grupo a su equivalente hexadecimal:

1001 = 9

1011 = B

3. Investiga y describe cómo se representa una imagen en formato PNG en el disco.

- Una imagen PNG no se guarda como una simple "tabla de colores", sino que tiene una estructura específica con varias partes organizadas en bloques llamados chunks. Estos bloques contienen información sobre la imagen y sus datos.

Estructura general de un archivo PNG:
* Firma PNG (PNG signature):
Es un encabezado de 8 bytes que identifica que el archivo es PNG. Siempre empieza con los mismos números para que el sistema sepa qué tipo de archivo está leyendo.

* Chunks (bloques de datos):
Después de la firma, el archivo contiene varios bloques con información importante:

- IHDR (Header): Contiene los datos básicos: ancho, alto, profundidad de color, tipo de imagen, etc.

- PLTE (Palette): Solo si la imagen usa paleta de colores. Guarda la lista de colores.

- IDAT (Image Data): Aquí va la imagen comprimida, usando un algoritmo llamado Deflate (parecido a ZIP).

- tEXt / iTXt: Información opcional como texto, título, autor, etc.

- IEND (End): Marca el final del archivo.

¿Qué se guarda realmente en el disco?

En el disco, el archivo PNG es una secuencia de bytes organizada que incluye:

- Información de formato (firma)

- Dimensiones de la imagen

- Información de color (canales RGBA: rojo, verde, azul, y alfa para transparencia)

- Datos comprimidos del contenido de la imagen

- Información opcional

- Un final marcado

4. Analiza la siguiente situación: ¿Qué sucede si intentas almacenar un número mayor al que puede representar un byte (por ejemplo, 300)? ¿Cómo lo maneja Python?

- Un byte puede representar números del 0 al 255 Si intentas guardar un número como 300, simplemente no cabe en un solo byte.

Python no tiene ese límite para enteros, ya que maneja los números de forma dinámica. Por ejemplo: x = 300 print(x.to_bytes(2, 'big')) # Correcto: usa 2 bytes para representarlo

Pero si intentas hacer esto con solo 1 byte te da este error: x = 300 print(x.to_bytes(1, 'big')) # Error: OverflowError

Conclusión: Python evita errores silenciosos y te avisa cuando necesitas más espacio de almacenamiento para representar un número.

