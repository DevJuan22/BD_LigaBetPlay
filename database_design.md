# Diseño de Base de Datos - Liga BetPlay

## Colecciones y Relaciones

### 1. Jugadores
- **Campos:**
  - `_id`: Identificador único.
  - `nombre`: Nombre del jugador.
  - `posicion`: Posición en el campo.
  - `edad`: Edad del jugador.
  - `nacionalidad`: Nacionalidad del jugador.
  - `equipo_id`: Identificador del equipo al que pertenece.
- **Relación:**
  Relacionado con la colección `Equipos` a través del campo `equipo_id`.

### 2. Equipos
- **Campos:**
  - `_id`: Identificador único.
  - `nombre`: Nombre del equipo.
  - `ciudad`: Ciudad del equipo.
  - `estadio`: Nombre del estadio.
  - `entrenador`: Nombre del entrenador.

### 3. Encuentros
- **Campos:**
  - `_id`: Identificador único.
  - `equipo_local`: Nombre del equipo local.
  - `equipo_visitante`: Nombre del equipo visitante.
  - `resultado`: Marcador final.
  - `puntos_local`: Puntos obtenidos por el equipo local.
  - `puntos_visitante`: Puntos obtenidos por el equipo visitante.
- **Relación:**
  Involucra dos equipos, relacionados por `equipo_local` y `equipo_visitante`.

### 4. Entrenadores
- **Campos:**
  - `_id`: Identificador único.
  - `nombre`: Nombre del entrenador.
  - `equipo`: Nombre del equipo que entrena.
- **Relación:**
  Relacionado con la colección `Equipos` a través del campo `equipo`.

### 5. Posiciones
- **Campos:**
  - `_id`: Identificador único.
  - `equipo`: Nombre del equipo.
  - `puntos`: Total de puntos.
  - `partidosJugados`: Número de partidos jugados.
  - `victorias`: Número de victorias.
  - `empates`: Número de empates.
  - `derrotas`: Número de derrotas.
  - `golesFavor`: Goles anotados.
  - `golesContra`: Goles recibidos.
  - `diferenciaGoles`: Diferencia entre goles a favor y en contra.
- **Relación:**
  Calculada a partir de los datos de `Encuentros`.
