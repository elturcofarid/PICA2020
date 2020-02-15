# Productos!

[API Disponible V2](https://app.swaggerhub.com/apis/cepv2010/Producto/V2)

Dominio en el cual se consulta toda la gama de productos y sus respectivos parametros para que el usuario (cliente) tenga la posibilidad de obtener la información que requiera, dentro de los productos se encuentran sub-dominios o productos disponibles:

- Evento
- Transporte
- Hospedaje
- Paquete


## Sub-Dominios

### Evento

Es el encargado de obtener los eventos disponibles de acuerdo a unos parametros:

- Tipo de Evento
- Sub Tipo de Evento

| Dominio | Sub-dominio  | Atributos | Tipo | Respuesta | Estados | Descripción 
|--|--|--|--|--|--|--|
|  producto | evento/tipoEvento | estado | GET | ElementosDto | 200,404 | Encargado de obtener los tipos de eventos disponibles
| producto | evento/subTipoEvento | tipoEvento, estado | GET |  ElementosDto | 200,404 | Encargado de obtener los subtipos de acuerdo al tipo de evento seleccionado
| producto | evento | tipoEvento, subtipoEvento, fecha,ciudad,cantidadEntradas | GET | eventoDto | 200,204,404 | Encargado de obtener los resultados disponibles de eventos
