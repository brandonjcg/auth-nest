# Proyecto de Registro e Inicio de Sesión con Roles

Este proyecto es una aplicación de autenticación que permite a los usuarios registrarse, iniciar sesión y acceder a recursos basados en roles. Utiliza PostgreSQL como base de datos.

## Características

- Registro de usuarios
- Inicio de sesión de usuarios
- Asignación de roles a usuarios
- Protección de rutas basadas en roles
- Generación de tokens JWT para autenticación

## Tecnologías Utilizadas

- **Backend**: NestJS
- **Base de datos**: PostgreSQL
- **Autenticación**: JWT (JSON Web Tokens)
- **Hashing de contraseñas**: bcrypt

## Requisitos Previos

- Node.js (v14 o superior)
- PostgreSQL
- npm o yarn

## Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/JuanjoCodedev/auth-nest.git
```

2. Instala las dependencias del proyecto:

```bash
npm install
```

3. Configura la base de datos PostgreSQL y crea un archivo `.dev.env` en la raíz del proyecto con la siguiente configuración:

```env
- HOSTDB=localhost
- PORTDB=5432
- USERNAMEDB=tu-usuario
- PASSDB=tu-contraseña
- DB=nombre-de-tu-base-de-datos
```

## Uso

1. Inicia el servidor:

   ```bash
   npm run start
   ```

2. El servidor estará disponible en `http://localhost:3000`

### Endpoints

#### Registro de Usuario

- **URL**: `user/create-account`
- **Método**: `POST`
- **Cuerpo**:
  ```json
  {
    "username": "nombre-de-usuario",
    "useremail": "correo@ejemplo.com",
    "userpassword": "123456789"
  }
  ```

#### Inicio de Sesión

- **URL**: `/user/login`
- **Método**: `POST`
- **Cuerpo**:

  ```json
  {
    "useremail": "correo@ejemplo.com",
    "userpassword": "123456789"
  }
  ```

### Roles

Los roles pueden ser asignados a los usuarios y utilizados para proteger rutas específicas. Ejemplo de roles: `admin`, `member`.

## Desarrollo

### Ejecución de la Aplicación en Desarrollo

```bash
npm run start:dev
```

### Compilación y Ejecución en Producción

```bash
npm run build
npm run start:prod
```

## Diagrama de Flujo

<img src="https://i.imgur.com/xMHjla4.jpg">

## Contribución

1. Haz un fork del repositorio.

2. Crea una nueva rama:

```bash
git checkout -b feature/nueva-caracteristica
```

3. Realiza tus cambios y haz commit:

```bash
git commit -am 'Añadir nueva característica'
```

4. Empuja tus cambios a la rama:

```bash
git push origin feature/nueva-caracteristica
```

5. Abre un Pull Request en GitHub, describiendo los cambios propuestos.

## Lincencia

Este proyecto está licenciado bajo la Licencia MIT.
