# Alambú · Reservas de Turnos

App de agendamiento de turnos para Alambú (Belleza y Bienestar).

## Stack

- HTML + CSS + JavaScript (vanilla, sin frameworks)
- [Supabase](https://supabase.com) como base de datos (turnos)
- Despliegue en [Vercel](https://vercel.com)

## Funcionalidad

- Selección de servicio
- Calendario y horarios disponibles (consulta turnos existentes en Supabase)
- Formulario de datos del cliente
- Confirmación + envío de resumen por WhatsApp
- Panel de administración (protegido con contraseña) para ver los turnos del día

## Configuración

Las credenciales de Supabase (URL y clave pública `anon`/`publishable`) están
definidas directamente en `index.html`, en la sección `SUPABASE`. Son claves
**públicas**, pensadas para usarse en el frontend; el acceso a los datos está
controlado por las políticas de Row Level Security (RLS) configuradas en la
tabla `turnos`.

## Cambiar la contraseña del panel admin

En `index.html`, buscar:

```js
const ADMIN_PASSWORD = 'alambu2025';
```

y cambiarla por una contraseña propia antes de publicar.
