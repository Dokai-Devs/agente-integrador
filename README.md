# Agente integrador

Es el proyecto integrador del plan de formación de DokaiDevs: un producto chico de agente de IA para un negocio ficticio, hecho de punta a punta. Se construye sobre [`plantilla-cliente`](https://github.com/Dokai-Devs/plantilla-cliente), con el mismo stack y las mismas reglas que el proyecto de un cliente.

## Qué tiene

- **Landing del negocio**, con un chat.
- **Agente** que responde las preguntas frecuentes y toma consultas: nombre, contacto y mensaje.
  - Llama al modelo desde un solo módulo y tiene un límite de gasto.
  - Si no sabe algo, no inventa: deriva a una persona.
- **Panel de configuración con login**, donde el dueño del negocio:
  - edita las instrucciones del agente, las preguntas frecuentes, los horarios y los datos de contacto;
  - ve las consultas que entraron.
- **Base de datos en Supabase con RLS:** cada dueño ve solo su configuración y sus consultas, y cada regla tiene su test.
- **Deploy en Vercel** con un preview por PR, y CI con lint, typecheck y tests.

## Por etapas

| Etapa | Qué se suma |
| --- | --- |
| 3. Next.js y Vercel | La landing desplegada, con un chat de respuestas fijas |
| 4. Supabase y SQL | Login, el panel de configuración, las consultas guardadas con RLS, migraciones y un webhook de entrada validado con Zod |
| Cierre de la fase 2 | El agente conectado al modelo, que contesta con la configuración del panel y deriva lo que no sabe |
| Especialización en Agentes | Evals, pruebas de prompt injection, trazas y WhatsApp |

## Cómo arrancar

1. Crear el diseño de datos en un issue y discutirlo con Pablo antes de escribir migraciones.
2. Avanzar en el orden de la tabla: cada etapa termina con un PR mergeado y desplegado.
