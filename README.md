# agrovetsdev

Proyecto Django mínimo generado.

Instrucciones (Windows cmd):

1. Crear y activar virtualenv:

    python -m venv venv
    venv\Scripts\activate

2. Instalar dependencias:

    pip install -r requirements.txt

3. Migrar y ejecutar:

    python manage.py migrate
    python manage.py runserver

API REST y autenticación

Endpoints disponibles (base `/`):

- `POST /api/auth/register/` : registrar un usuario. Campos: `username`, `email` (opcional), `password`.
- `GET /api/auth/me/` : devuelve los datos del usuario autenticado (requiere sesión activa).

Probar usando la Browsable API de DRF:

1. Inicia el servidor:

    python manage.py runserver

2. Abre en el navegador:

    http://127.0.0.1:8000/api/auth/register/  (para crear cuenta)
    http://127.0.0.1:8000/api-auth/login/     (para iniciar sesión en la browsable API)
    http://127.0.0.1:8000/api/auth/me/        (para ver perfil autenticado)

Si prefieres usar curl desde Windows (PowerShell), puedes crear usuario y luego usar cookies para la sesión en el navegador; el flujo típico de autenticación para APIs sin JWT es usar sesiones o crear un endpoint de token personalizado.

