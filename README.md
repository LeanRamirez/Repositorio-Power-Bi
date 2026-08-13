# Repositorio-Power-Bi

Leandro Maximiliano Ramirez 
maxi3230lmr@gmail.com

Documentación Redactá un breve documento (puede ser un archivo .docx o un README.md) donde expliques:
Qué transformaciones realizaste y en qué orden. Por qué elegiste cada tipo de dato. Cómo resolviste los valores nulos y duplicados encontrados. Qué criterio usaste para separar los datos del cliente de los de la transacción.

Lo primero que hice fue actualizar los nombres de las columnas para que sean legibles para un usuario final usando snake_case. Lo siguiente fue corregir el tipo de datos necesario para cada columna, formatear la columna fecha_venta a el tipo de dato date, también se actualizo el dato de porcentaje de descuento a porcentaje, acto seguido se modificaron los cambios null por el valor 0,00%. Se eliminaron las filas duplicadas y vacías. Filtramos la columna_total ventas para que solo sean visibles los valores correctos y no contenga valores nulos. Para terminar normalizamos la tabla en dos tablas, F-Ventas y D-Clientes detectando que columnas corresponde a cada una de las tablas.
