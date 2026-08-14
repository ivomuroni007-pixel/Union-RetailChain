¿Cuántas filas devuelve cada consulta y por qué son distintas? Explicá con ejemplos concretos de los datos qué filas se eliminaron con UNION.
La primer consulta devuelve 11 filas. El uso de UNION es para eliminar los registros duplicados y mantener valores únicos de las dos sucursales, norte y sur. Respondiendo a la consulta y otorgando un listado con los productos únicos que comercializa entre ambas sucursales. Las filas eliminadas fueron las repetidas del producto con id: 103, 104 y 106. 
La segunda consulta devuelve solo 1 fila. Union-All fué utilizada para agrupar los datos de ambas sucursales y, mediante el uso de medidas aritméticas, como 'COUNT', agrupar aún mas los registros y  responder a la pregunta de negocio. 

¿Por qué UNION ALL es más eficiente que UNION? ¿Qué operación adicional realiza UNION internamente que consume más recursos?
Porque el UNION ALL devuelve todos los registros, incluso los duplicados. Mientras qué, UNION, consume mas recursos porque debe eliminar los duplicados. Puede decirse que sea mas eficiente el primero por razones de velocidad, almacenamiento y recursos, pero considero que ambos pueden ser igual de eficientes, si cada uno se ejecuta en el contexto adecuado. 

¿En qué casos de negocio usarías cada uno? Dá al menos dos ejemplos reales distintos a los del ejercicio.
UNION: lo usaría para casos en los que necesito combinar información de fuentes diferentes y no necesito registros duplicados.
Ejemplos: 
. Teniendo los registros de ingresos y salidas del personal de trabajo de una franquicia con sucursales en distintos puntos geográficos. Quisiera saber mi lista de empleados total.
. En una empresa se quiere saber el listado único de proveedores.
UNION ALL: para casos donde me interesa combinar información y no perder ningún registro de vista. 
Ejemplos: 
. En las sucursales de una cadena de bar/restaurantes quisiera saber qué productos generan mas operaciones de venta.
. Empresa corporativa con sucursales en diferentes puntos del país necesitaría realizar un reporte de las inasistencias del personal. Obteniendo los datos desde los registros de ingresos diarios.


¿Qué pasa si las columnas de ambas consultas no coinciden en número o tipo? ¿Qué error genera SQL?
Ambas consultas deben devolver la misma cantidad de columnas y los tipos de datos deben ser compatibles. Si la cantidad de columnas es diferente, SQL que indica que las consultas tienen que tener mismo número de expresiones. Si los tipos de datos no son compatibles, SQL genera un error de conversión de datos.

