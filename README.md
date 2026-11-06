# Dokaidemy

Es la app donde cada uno sigue su plan de formación en DokaiDevs. Es la entrega de la etapa 4: se construye sobre [`plantilla-cliente`](https://github.com/Dokai-Devs/plantilla-cliente), así que usa el mismo stack y las mismas reglas que un proyecto de cliente.

Mientras no esté lista, el avance se sigue con un issue por entrega en los repos de práctica.

## Qué tiene que hacer (primera versión)

- **Personas con rol:** aprendiz o mentor.
- **Etapas del plan:** nombre, semanas y qué se entrega.
- **Entregas:** una por persona y etapa, con estado, link al PR o a la demo y notas.
- **Validación:** el mentor aprueba la entrega o pide cambios, con un comentario.
- **Permisos con RLS:** cada aprendiz ve y edita solo lo suyo; el mentor ve todo y valida. Cada regla tiene un test.
- **Webhook de GitHub:** cuando se mergea un PR que cierra un issue de entrega, Dokaidemy lo registra como evidencia. Valida la firma del webhook y el cuerpo con Zod.

## Qué no tiene (por ahora)

Cursos, cuestionarios, puntajes ni notificaciones.

## Cómo arrancar

1. Crear el diseño de datos en un issue y discutirlo con Pablo antes de escribir migraciones.
2. Empezar por login y roles, después las etapas y las entregas, y el webhook al final.
