# PokeTEC
Aventura Pokémon por turnos en Python: combates con tipos y estados, captura, evoluciones, mundo con entrenadores, IA y guardado.
# ⚡ Poke-TEC v2

> Proyecto en Python 3 con `tkinter` + `Pillow`. Sin dependencias pesadas, con motor de juego separado de la interfaz y 104 pruebas automáticas.

## Características

| Área | Qué incluye |
|---|---|
| **Combate** | Turnos con daño basado en estadísticas, 13 tipos con ventajas y desventajas, STAB, críticos, precisión y prioridad |
| **Estados** | Quemadura, parálisis, veneno y sueño |
| **Pokémon** | 55 especies, 56 movimientos, niveles, experiencia, nuevos ataques y evoluciones (por nivel y piedra) |
| **Equipo y objetos** | Equipo de hasta 6, Caja, mochila por bolsillos, 19 objetos, tienda y Centro Pokémon |
| **Captura** | Poké Balls con probabilidad según salud, estado y tipo de ball |
| **Mundo** | 6 zonas, hierba alta con encuentros aleatorios, 16 entrenadores, medallas que abren el camino y misiones |
| **IA rival** | Fácil, normal y difícil: elige por daño esperado, explota debilidades, remata y cambia de Pokémon |
| **Partidas** | Autoguardado, copia de seguridad y recuperación de archivos corruptos; tabla de récords |
| **Interfaz** | Menú animado, barras de PS y EXP dinámicas, efectos de ataque, diálogos y soporte de teclado y ratón |

### Controles

| Acción | Teclas |
|---|---|
| Moverse / elegir | Flechas o `W A S D` |
| Aceptar / interactuar | `Enter`, `Z` o `Espacio` |
| Atrás | `Esc` o `X` |
| Menú de pausa | `M` o `Tab` |

## Estructura

```
poketec/
  engine/   Reglas del juego, sin interfaz: combate, IA, mundo, guardado, misiones
  ui/       Pantallas y dibujo (tkinter), sobre un Renderer abstracto
legacy/     Código original, conservado
tests/      Pruebas del motor y de la interfaz sin ventana
docs/       CHANGELOG
```

El motor nunca importa la interfaz, así que se puede probar sin abrir ninguna ventana y ampliar con nuevas especies,
movimientos o zonas añadiendo datos.
