# API Personas ISC305

API REST en Laravel para listar, consultar, crear, actualizar y eliminar personas.
El proyecto Laravel está en la carpeta `backend`. La colección de Postman está en `postman`.

## Requisitos

- PHP 8.3 o superior compatible con Laravel 13, con la extensión `pdo_mysql`.
- Composer 2, Git, MySQL y Postman.

## Instalación en Windows

Crea una base de datos MySQL llamada `isc305_unidad3`. Desde la raíz del repositorio, ejecuta:

```powershell
cd backend
composer install
Copy-Item .env.example .env
php artisan key:generate
```

En el archivo `.env` local, configura la conexión. Ajusta el usuario y la contraseña a tu instalación.

```dotenv
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=isc305_unidad3
DB_USERNAME=root
DB_PASSWORD=
```

Después ejecuta:

```powershell
php artisan migrate
php artisan serve
```

Importa el JSON de la carpeta `postman`. Usa la dirección que muestre Laravel, normalmente `http://127.0.0.1:8000`. Envía `Accept: application/json` en las solicitudes y usa un cuerpo JSON para POST y PUT.

## Endpoints

| Método | Ruta | Operación |
| --- | --- | --- |
| GET | `/api/hola` | Devuelve un saludo |
| GET | `/api/personas` | Lista las personas |
| GET | `/api/personas/{id}` | Consulta una persona |
| POST | `/api/personas` | Crea una persona |
| PUT | `/api/personas/{id}` | Actualiza una persona |
| DELETE | `/api/personas/{id}` | Elimina una persona |