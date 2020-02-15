# Productos!

[API Disponible V2](https://app.swaggerhub.com/apis/cepv2010/Producto/V2)

Dominio en el cual se consulta toda la gama de productos y sus respectivos parametros para que el usuario (cliente) tenga la posibilidad de obtener la información que requiera, dentro de los productos se encuentran sub-dominios o productos disponibles:

- Evento
- Transporte
- Hospedaje


## Sub-Dominios

### Evento

Es el encargado de obtener los eventos disponibles de acuerdo a unos parametros:

- Tipo de Evento
- Sub Tipo de Evento

| Dominio | Sub-dominio  | Atributos | Tipo | Tipo SubDominio | Respuesta | Estados | Descripción 
|--|--|--|--|--|--|--|--|
|  producto | evento/tipoEvento | estado | GET | Query | ElementosDto | 200,404 | Encargado de obtener los tipos de eventos disponibles
| producto | evento/subTipoEvento | tipoEvento, estado | GET | Query | ElementosDto | 200,404 | Encargado de obtener los subtipos de acuerdo al tipo de evento seleccionado
| producto | evento | tipoEvento, subtipoEvento, fecha,ciudad,cantidadEntradas | GET | Query | eventoDto | 200,204,404 | Encargado de obtener los resultados disponibles de eventos


### Transporte

Es el encargado de obtener la disponibilidad de transporte sea terrestre o aereo de acuerdo a unos parametros:

- Tipo de transporte
- Clase

| Dominio | Sub-dominio  | Atributos | Tipo | Tipo SubDominio | Respuesta | Estados | Descripción 
|--|--|--|--|--|--|--|--|
| producto | transporte/clase | estado | GET | Query | ElementosDto | 200, 404 |  Encargado de obtener las clase de transportes es decir si es clase economica, ejecutiva o primera clase
| producto | transporte/tipoTransporte | estado | GET | Query | ElementosDto | 200, 404 | Encargado de obtener los tipos de transportes 
| producto | transporte | clase,tipoTransporte,fechaDesde, fechaHasta (Opcional),pasajeros,ciudadDesde, ciudadHasta (Opcional) | GET | Query | TransporteDto | 200,204,404 | Encargado de obtener los resultados disonibles de transporte

### Hospedaje

Es el encargado de obtener la disponibilidad de hospedaje de acuerdo a unos parametros:

| Dominio | Sub-dominio  | Atributos | Tipo | Tipo SubDominio | Respuesta | Estados | Descripción 
|--|--|--|--|--|--|--|--|
| producto | hospedaje | fechaDesde, fechaHasta, ciudad, nroHabitaciones, nroPersonas | GET | Query | hospedajeDto-tipoHabitacionDto | 200,204,404 | Encargado de obtener los resultadosdisponibles de hospedaje
