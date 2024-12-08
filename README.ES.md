# Authify  

Authify es una API moderna y segura para la gestión de usuarios y autenticación. Construida con Node.js y TypeScript, esta API ofrece una solución escalable y flexible para manejar roles, permisos y flujos de autenticación en aplicaciones web.  

## Características principales  
- **Autenticación JWT**: Gestión segura y sin estado de sesiones de usuario.  
- **Roles y permisos**: Soporte para roles jerárquicos y personalizables.  
- **Verificación de correos**: Confirmación de cuentas mediante enlaces únicos enviados al correo.  
- **Recuperación de contraseñas**: Envío de enlaces seguros para restablecer contraseñas olvidadas.  
- **Auditoría**: Registro de accesos para mejorar la seguridad y el monitoreo de usuarios.  
- **Diseño modular**: Fácil de personalizar y ampliar según las necesidades del proyecto.  

---

## Tecnologías utilizadas  
- **Node.js**  
- **Express.js**  
- **TypeScript**  
- **JWT (JSON Web Tokens)**  
- **bcrypt** para el hash de contraseñas.  
- **Nodemailer** para el envío de correos electrónicos.  
- **PostgreSQL** (opcionalmente MongoDB) como base de datos.  

---

## Instalación  

1. Clona el repositorio:  
   ```bash
   git clone https://github.com/tuusuario/Authify.git
   cd Authify
   ```

2. Instala las dependencias:
  ```bash
  npm install
  ```

3. Configura las variables de entorno:
- Crea un archivo .env en la raíz del proyecto con las siguientes claves:
  ```env
  PORT=3000
  DATABASE_URL=postgresql://usuario:contraseña@localhost:5432/authify
  JWT_SECRET=tu_secreto
  SMTP_HOST=smtp.ejemplo.com
  SMTP_PORT=587
  SMTP_USER=tu_correo
  SMTP_PASSWORD=tu_contraseña
  ```

Inicia la aplicación:
```bash
npm run dev
```

Endpoints principales

Autenticación

POST /auth/register
Registra un nuevo usuario.

POST /auth/login
Inicia sesión y devuelve un token JWT.

POST /auth/forgot-password
Envía un enlace para restablecer la contraseña.

POST /auth/reset-password
Permite establecer una nueva contraseña.

Gestión de usuarios

GET /users
Lista de usuarios (solo para administradores).

GET /users/:id
Detalles de un usuario específico.

PUT /users/:id
Actualiza información de usuario.

DELETE /users/:id
Elimina o desactiva un usuario.

Scripts disponibles

npm run dev: Inicia el servidor en modo desarrollo.
npm run build: Compila el proyecto para producción.
npm start: Inicia el servidor en modo producción.
npm run lint: Analiza el código en busca de problemas de estilo o sintaxis.

Contribuciones
Las contribuciones son bienvenidas. Por favor, crea un fork del repositorio, realiza tus cambios y envía un pull request con una descripción clara.

Licencia
Este proyecto está licenciado bajo la MIT License.
