# 🐍 Django – Comandos básicos más usados

Este pequeño tutorial muestra los **comandos esenciales de Django** para crear y ejecutar un proyecto web paso a paso.

---

## 1️⃣ Crear un proyecto Django

```bash
django-admin startproject miproyecto
```

🔹 **¿Qué hace?**
Crea la estructura principal del proyecto.

📁 Se genera algo como:

```
miproyecto/
├── manage.py
└── miproyecto/
    ├── __init__.py
    ├── settings.py
    ├── urls.py
    ├── asgi.py
    └── wsgi.py
```

---

## 2️⃣ Entrar al proyecto

```bash
cd miproyecto
```

🔹 Todos los comandos importantes se ejecutan desde aquí usando `manage.py`.

---

## 3️⃣ Crear una aplicación

```bash
python manage.py startapp miapp
```

🔹 **¿Qué es una app?**
Una app es un módulo del proyecto (ej: usuarios, blog, productos).

📁 Estructura creada:

```
miapp/
├── admin.py
├── apps.py
├── models.py
├── views.py
├── tests.py
└── migrations/
```

⚠️ **Recuerda** agregar la app en `INSTALLED_APPS` dentro de `settings.py`.

---

## 4️⃣ Crear migraciones

```bash
python manage.py makemigrations
```

🔹 **¿Para qué sirve?**
Detecta cambios en `models.py` y crea archivos de migración (no toca la base de datos aún).

---

## 5️⃣ Aplicar migraciones

```bash
python manage.py migrate
```

🔹 **¿Qué hace?**
Aplica las migraciones y crea/actualiza las tablas en la base de datos.

---

## 6️⃣ Crear un superusuario

```bash
python manage.py createsuperuser
```

🔹 Permite crear un usuario administrador para acceder al panel de administración.

Luego podrás entrar en:

```
http://127.0.0.1:8000/admin
```

---

## 7️⃣ Ejecutar el servidor de desarrollo

```bash
python manage.py runserver
```

🔹 Inicia el servidor local.

🌐 Accesos:

* Sitio web: `http://127.0.0.1:8000`
* Admin: `http://127.0.0.1:8000/admin`

---

## 🧠 Resumen rápido

| Comando           | Función                    |
| ----------------- | -------------------------- |
| `startproject`    | Crea el proyecto           |
| `startapp`        | Crea una aplicación        |
| `makemigrations`  | Prepara cambios de modelos |
| `migrate`         | Aplica cambios a la DB     |
| `createsuperuser` | Usuario admin              |
| `runserver`       | Inicia el servidor         |

