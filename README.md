# Rails GPS Waypoints App

## Instrucción
Crea una aplicación en Rails que pueda aceptar waypoints de GPS asociados a un vehículo y luego mostrarlos en un mapa.

## El problema
Desarrolla una aplicación en Rails que acepte waypoints de GPS asociados a un vehículo y los muestre en un mapa. Un waypoint de GPS representa una ubicación basada en un par de coordenadas de latitud/longitud y un momento en el tiempo. Un vehículo se representa por un identificador único alfanumérico y puede tener múltiples waypoints de GPS.

Específicamente, la aplicación debe tener los siguientes endpoints:

### Endpoints

#### 1. JSON API
- **Endpoint**: `/api/v1/gps`
- **Descripción**: acepta waypoints de GPS asociados a un vehículo.
- **Formato esperado**:
  ```json
  {
    "latitude": 20.23,
    "longitude": -0.56,
    "sent_at": "2016-06-02 20:45:00",
    "vehicle_identifier": "HA-3452"
  }
Si no existe un vehículo con ese identificador, créalo.


#### 2. HTML
- **Endpoint**:  /show
- 
- **Descripción**:  muestra la coordenada más reciente de cada vehículo en un mapa.

- **Nota**: Puedes elegir cualquier proveedor de mapas, como Google Maps, Open Street Map, Bing Maps, Mapbox, etc.



## Cosas a considerar
Todos los waypoints históricos deben almacenarse.

No se requiere autenticación para los endpoints.

Los waypoints recibidos a través de la API deben ser procesados en un sistema de procesamiento de trabajos en segundo plano.
Muestra (posición y nombre) y filtra vehículos en el mapa usando React como librería de frontend.

## Configuración recomendada

Ruby >= 2.5.2
Ruby on Rails >= 6
Base de datos: Postgres
Job Processor: Sidekiq
Redis
Contenedores: Docker y Docker-Compose
Mapas: Google Maps API
