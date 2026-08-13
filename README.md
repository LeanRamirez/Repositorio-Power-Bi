# Repositorio-Power-Bi

Estudiante: Leandro Maximiliano Ramírez
Correo: maxi3230lmr@gmail.com

Objetivo

El objetivo del trabajo fue limpiar, transformar y organizar los datos originales mediante Power Query, con el propósito de obtener información consistente y preparada para su posterior análisis.

Transformaciones realizadas

Las transformaciones se realizaron en el siguiente orden:

1. Renombrado de columnas

Primero se modificaron los nombres de las columnas para hacerlos más claros, uniformes y fáciles de interpretar.

Se utilizó el formato snake_case, que consiste en escribir los nombres en minúsculas y separar las palabras mediante guiones bajos. Por ejemplo:

Fecha Venta pasó a llamarse fecha_venta.
Total Ventas pasó a llamarse total_ventas.
Porcentaje Descuento pasó a llamarse porcentaje_descuento.

Este criterio permite mantener una estructura consistente y facilita el uso posterior de las columnas en herramientas de análisis, bases de datos o lenguajes de programación.

2. Corrección de los tipos de datos

Después se revisó el tipo de dato asignado a cada columna. El objetivo fue evitar errores en los cálculos, filtros y agrupaciones.

Se aplicaron los siguientes criterios:

Las columnas identificadoras se configuraron como números enteros o texto, según su contenido.
Las columnas con nombres u otros datos descriptivos se configuraron como texto.
La columna fecha_venta se configuró como fecha, porque representa el momento en el que se realizó cada transacción.
Las columnas con importes monetarios se configuraron como números decimales.
La columna porcentaje_descuento se configuró como porcentaje, porque sus valores representan una proporción aplicada sobre la venta.

La elección correcta de los tipos de datos permite que Power Query y las herramientas de análisis interpreten adecuadamente cada columna.

3. Tratamiento de valores nulos

Se identificaron valores nulos en la columna porcentaje_descuento. Estos valores se reemplazaron por 0,00 %.

El criterio utilizado fue considerar que, cuando una transacción no tenía un descuento registrado, no se había aplicado ningún descuento. Por lo tanto, el valor nulo podía interpretarse como un descuento del 0 %.

También se revisaron los valores nulos de la columna total_ventas. Los registros que no contenían un total válido se filtraron para evitar incorporar transacciones incompletas en los análisis posteriores.

4. Eliminación de filas vacías

Se eliminaron las filas completamente vacías porque no contenían información útil para el análisis.

Mantener estas filas podía generar registros innecesarios, alterar el conteo de observaciones y dificultar la revisión de la información.

5. Eliminación de registros duplicados

Se buscaron y eliminaron los registros duplicados para evitar que una misma observación fuera contabilizada más de una vez.

Esta transformación es importante porque los duplicados pueden provocar resultados incorrectos, como una sobreestimación de la cantidad de ventas o del importe total facturado.

6. Validación de la columna total_ventas

Se filtró la columna total_ventas para conservar únicamente los registros que contenían valores válidos.

El objetivo fue asegurar que las operaciones posteriores, como sumas, promedios y comparaciones, se realizaran sobre transacciones completas y correctamente registradas.

7. Separación de los datos

Finalmente, la tabla original se separó en dos tablas:

F_Ventas: contiene los datos relacionados con cada transacción.
D_Clientes: contiene los datos descriptivos correspondientes a los clientes.

El criterio utilizado fue separar la información según su función:

Los datos que describen quién es el cliente pertenecen a D_Clientes.
Los datos que describen qué ocurrió en cada operación pertenecen a F_Ventas.

Esta separación evita repetir innecesariamente los datos del cliente en cada venta y permite organizar la información mediante un modelo de hechos y dimensiones.

La tabla F_Ventas puede relacionarse con D_Clientes mediante el identificador del cliente. De esta manera, es posible analizar las ventas según las características de cada cliente sin almacenar sus datos descriptivos de forma repetida.

Resultado final

Después de aplicar las transformaciones, se obtuvo un conjunto de datos:

Con nombres de columnas consistentes.
Con tipos de datos correctamente definidos.
Sin filas completamente vacías.
Sin registros duplicados.
Con un criterio definido para el tratamiento de valores nulos.
Separado en una tabla de ventas y una tabla de clientes.
Preparado para realizar análisis y construir un modelo de datos.
Evidencia del proceso
