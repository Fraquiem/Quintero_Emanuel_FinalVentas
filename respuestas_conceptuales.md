# Respuestas conceptuales

1. **¿Por qué usar `_loaded_at` y no `fecha_venta`?** `_loaded_at` indica cuándo llegó la venta a raw; `fecha_venta` indica cuándo ocurrió. Una venta antigua puede cargarse hoy, por lo que su fecha de negocio no mide la actualidad de la carga. Freshness compara la carga más reciente con la hora actual, pero no demuestra que hayan llegado todas las ventas esperadas.

2. **¿Por qué las pruebas de integridad no garantizan actualidad?** Las pruebas de unicidad y campos obligatorios comprueban propiedades de los datos presentes, pero pueden pasar aunque la fuente no se haya actualizado recientemente. Por eso se necesita comprobar freshness por separado.
