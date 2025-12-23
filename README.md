# Cafetería Isabelle ☕🍰

Proyecto académico (Universidad) orientado a simular una **cafetería online**: catálogo de productos (cafés, pasteles/postres), carrito de compras, flujo de pago y generación de boleta/confirmación. Incluye un módulo básico de **registro e inicio de sesión** usando **PHP + MySQL**.

---

## Cómo verlo?

Este proyecto es principalmente **front-end (HTML/CSS/JS)** con algunas páginas que usan **PHP** (login/registro/pago).  
Para que el login funcione necesitas ejecutarlo en un servidor local con PHP (por ejemplo **XAMPP**).

### Opción A: Solo ver la interfaz (sin login)
1. Abre `index.html` en tu navegador.
2. Navega por las secciones y páginas del catálogo.

### Opción B: Ejecutar con PHP + MySQL (recomendado)
**Requisitos**
- PHP 7+ (XAMPP/WAMP/Laragon)
- MySQL / MariaDB

**Pasos**
1. Copia la carpeta del proyecto dentro de tu servidor local:
   - XAMPP: `C:\xampp\htdocs\Cafeteria-Isa\`
2. Inicia **Apache** y **MySQL** desde XAMPP.
3. Crea la base de datos:
   - Nombre: `login`
4. Crea la tabla `usuarios`:

```sql
CREATE TABLE usuarios (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nombre VARCHAR(100) NOT NULL,
  correo VARCHAR(150) NOT NULL UNIQUE,
  usuario VARCHAR(100) NOT NULL,
  contrasena VARCHAR(255) NOT NULL
);
```

5. Verifica la conexión en `php/conexionbe.php` (por defecto):
   - host: `localhost`
   - user: `root`
   - password: *(vacío)*
   - database: `login`

6. Abre en el navegador:
   - `http://localhost/Cafeteria-Isa/index.html`
   - Para login/registro: `http://localhost/Cafeteria-Isa/cafeteria.php`

> Nota: Las contraseñas se almacenan hasheadas con **SHA-512** (ver `php/loginusuariobe.php` / `php/registrousuariobe.php`).

---

## ✨ Funcionalidades principales

- Landing / portada (`index.html`)
- Catálogo de productos (cafés, pasteles y postres)
- Carrito de compras (JS)
- Flujo de pago (pantalla de pago + backend simple)
- Boleta/confirmación
- Registro e inicio de sesión (PHP + MySQL)

---

## 🧰 Tecnologías utilizadas

- **HTML5**
- **CSS3**
- **JavaScript**
- **PHP**
- **MySQL/MariaDB**
- Librerías/CDN: Font Awesome, Boxicons, Google Fonts

---

## 🗂️ Estructura del proyecto

```text
Cafeteria Isa/
├─ index.html
├─ cafeteria.php              # Login/registro
├─ cafe.html
├─ pasteles.html
├─ postres.html
├─ carrito.html
├─ pago.html
├─ boleta.html
├─ css/
├─ js/
├─ img/
└─ php/
   ├─ conexionbe.php
   ├─ loginusuariobe.php
   ├─ registrousuariobe.php
   ├─ pago.php
   └─ logout.php / cerrarsesion.php
```

---

## 📸 Capturas

Puedes agregar aquí capturas del proyecto dentro de una carpeta `docs/`:

```md
![Home](docs/home.png)
![Carrito](docs/carrito.png)
```

---

## 👤 Autor

**Rodrigo**  
Proyecto académico - Universidad

Si tienes sugerencias o comentarios, ¡bienvenidos!
