
# Sistema de Transporte Público: Modelo de Dominio

Este modelo de dominio representa un sistema de transporte público, incluyendo los elementos esenciales como vehículos, rutas, pasajeros, conductores, paradas, tarifas, sistemas de pago y la gestión de incidencias. El modelo busca ser lo más completo posible para reflejar las operaciones básicas y las relaciones clave entre los componentes del sistema.

## Diagramas

![Diagrama de Clases](images/DiagramaDeClases.png)

- Representa las entidades principales del sistema y sus relaciones.
- `SistemaDeTransportePublico` es la clase principal que incluye sistemas de pago, tarifas, flotas, planificación de rutas y gestión de incidencias.
- `Flota` agrupa a `Vehiculos` y `Conductores`. Cada `Vehiculo` sigue una `Ruta` específica, que incluye `Paradas` y `Horarios`.
- `SistemaDePago` incluye diferentes `TiposDeAbono` y `MetodosDePago`.
- `GestionDeIncidencias` se encarga de registrar `Incidencias`, las cuales pueden derivar en necesidades de `Mantenimiento`.

![Diagrama de Objetos](images/DiagramaDeObjetos.png)

- Proporciona un ejemplo de una instancia del sistema con datos específicos.
- `Vehiculo1` es un autobús conducido por `Conductor1` y transporta a `Pasajero1` en `Ruta1` con paradas y horarios específicos.
- El pago de `Pasajero1` se realiza con `Tarifa1` mediante el `MetodoDePago1`.
- `Incidencia1` representa un evento que afecta el trayecto del vehículo.

### Diagrama de Estados

- Muestra el flujo de estados de un pasajero durante el trayecto.
- Desde que el pasajero aborda el vehículo hasta que se baja en la parada deseada.
- Incluye el proceso de pago y contempla posibles incidencias que pueden afectar el trayecto.

## Glosario

- **SistemaDeTransportePublico**: Clase principal que agrupa todos los elementos del sistema.
- **SistemaDePago**: Componente para gestionar los pagos y tipos de abonos.
- **TipoDeAbono**: Representa las opciones de abonos disponibles (mensuales, semanales, etc.).
- **MetodoDePago**: Forma en que se realiza el pago (efectivo, tarjeta).
- **Tarifa**: Costo del viaje, asociado a un método de pago.
- **Flota**: Conjunto de vehículos en el sistema.
- **Conductor**: Persona que opera el vehículo en una ruta asignada.
- **Vehiculo**: Medio de transporte utilizado (bus, tranvía).
- **Pasajero**: Usuario que aborda el vehículo para realizar un trayecto.
- **Ruta**: Camino que sigue un vehículo, compuesto de paradas.
- **Parada**: Punto específico donde el vehículo puede detenerse.
- **Horario**: Tiempos asignados a las rutas.
- **PlanificacionDeRuta**: Gestión de las rutas y horarios.
- **GestionDeIncidencias**: Componente para registrar y gestionar problemas durante el trayecto.
- **Incidencia**: Evento que interfiere en el viaje, como tráfico o averías.
- **Mantenimiento**: Operaciones para reparar o prevenir problemas en los vehículos.
