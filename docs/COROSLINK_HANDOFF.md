# Flujo de intercambio con CorosLink

1. Guardar paquetes recibidos en `exports/incoming`.
2. Inspeccionarlos sin extraerlos ni modificar CorosLink.
3. Usar CorosLink para editar, previsualizar y exportar.
4. Guardar los paquetes finales en `exports/outgoing`.
5. No versionar cachés, bases de datos ni carpetas de AppData de CorosLink.
6. Usar “Send to COROS” solo cuando se solicite explícitamente.

Los paquetes COROS esperados contienen `info.json`, `config.txt`,
miniaturas, fondos y recursos PNG por resolución.
