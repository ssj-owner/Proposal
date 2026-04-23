- name: draw.io CLI

  uses: severgroup-tt/actions-drawio-cli@v1.0.0
# Propuesta TP DSW

## Grupo

### Integrantes

| Legajo | Apellido y Nombre |
|:--|:--|
| 54796 | Vázquez, Guido Hernán |
| 55036 | Gallo Fiocca, Santino |

### Repositorios

* [Frontend app](#)
* [Backend app](#)

---

## Watch Party

### Descripción

Watch Party es una aplicación web que permite a grupos de amigos ver videos o películas de forma sincronizada en tiempo real. Un usuario crea una sala privada y comparte un código de acceso o enlace de invitación. El host administra la reproducción del video y la lista de reproducción, mientras que todos los participantes ven el mismo segundo del video simultáneamente. La comunicación se realiza mediante un chat en tiempo real con soporte de reacciones durante la reproducción.

### Modelo

[Ver diagrama ERD] https://drive.google.com/file/d/1RWh6HsINsxnodFpOT5HX63GRPlculIHQ/view?usp=sharing

---

## Alcance Funcional

### Regularidad

| Req | Detalle |
|:-|:-|
| CRUD simple | 1. CRUD Video<br>2. CRUD Usuario |
| CRUD dependiente | 1. CRUD Playlist {depende de} CRUD Sala y CRUD Video |
| Listado + detalle | 1. Listado de salas filtrado por estado (activa/cerrada), muestra nombre de sala, host y cantidad de participantes => detalle muestra datos completos de la sala, playlist actual y participantes conectados |
| CUU/Epic | 1. Crear sala e invitar participantes mediante código de acceso<br>2. Sincronizar reproducción de video en tiempo real entre todos los participantes de la sala |

### Aprobación Directa o en Examen

| Req | Detalle |
|:-|:-|
| CRUD | 1. CRUD Usuario<br>2. CRUD Sala<br>3. CRUD Video<br>4. CRUD Participante<br>5. CRUD Playlist<br>6. CRUD Mensaje |
| CUU/Epic | 1. Crear sala e invitar participantes mediante código de acceso<br>2. Sincronizar reproducción de video en tiempo real entre todos los participantes de la sala |

### Alcance Adicional Voluntario


| Req | Detalle |
|:-|:-|
| Listados | 1. Historial de salas del usuario filtrado por fecha, muestra nombre de sala, fecha y duración de la reunión<br>2. Listado de videos de la playlist filtrado por plataforma, muestra nombre, duración y quién lo agregó |
| CUU/Epic | 1. Gestionar playlist en tiempo real (agregar, quitar y reordenar videos durante la sesión)<br>2. Chat con reacciones en tiempo real durante la reproducción |
| Otros | 1. Notificación al unirse un nuevo participante a la sala<br>2. Indicador de latencia y estado de conexión por participante |
