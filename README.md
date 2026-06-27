# LoStockistas - Proyecto de Manejo y Control de Stock

Aplicación web para la gestión de stock, proveedores, artículos, ventas y órdenes de compra.
El sistema permite administrar productos, asociarlos a proveedores, registrar ventas, controlar el stock disponible y gestionar órdenes de compra para reponer mercadería.

El proyecto está dividido en dos partes:

* `LoStockistas-Back`: backend desarrollado con Java Spring Boot.
* `LoStockistas-Front`: frontend desarrollado con Next.js / React.

---

## Funcionalidades principales

* Gestión de artículos.
* Gestión de proveedores.
* Asociación de artículos con proveedores.
* Registro de ventas.
* Gestión de órdenes de compra.
* Control de stock.
* Carga y visualización de información relacionada a inventario.

---

## Tecnologías utilizadas

### Backend

* Java
* Spring Boot
* Gradle
* Spring Data JPA
* MySQL
* Cloudinary, para manejo de imágenes si corresponde

### Frontend

* Next.js
* React
* TypeScript
* Tailwind CSS
* Componentes UI reutilizables

---

## Requisitos previos

Antes de ejecutar el proyecto, tener instalado:

* Java 17 o superior.
* Node.js 18 o superior.
* npm.
* MySQL.
* Git.

---

## Cómo ejecutar el proyecto

Primero clonar el repositorio:

```bash
git clone https://github.com/JoacoGiuliani/Proyecto-Manejo-y-control-de-Stock.git
```

Entrar a la carpeta del proyecto:

```bash
cd Proyecto-Manejo-y-control-de-Stock
```

---

# 1. Ejecutar el Backend

Entrar a la carpeta del backend:

```bash
cd LoStockistas-Back
```

Configurar la conexión a la base de datos en:

```bash
src/main/resources/application.properties
```

Ejemplo de configuración local:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/lostockistas
spring.datasource.username=root
spring.datasource.password=tu_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Crear la base de datos en MySQL:

```sql
CREATE DATABASE lostockistas;
```

Luego ejecutar el backend.

En Windows:

```bash
gradlew.bat bootRun
```

En Linux / Mac:

```bash
./gradlew bootRun
```

El backend debería quedar corriendo en:

```bash
http://localhost:8080
```

---

# 2. Ejecutar el Frontend

Abrir otra terminal y volver a la raíz del proyecto.

Entrar a la carpeta del frontend:

```bash
cd LoStockistas-Front
```

Instalar dependencias:

```bash
npm install
```

Configurar la URL del backend.

Crear o modificar el archivo `.env.local` con:

```env
NEXT_PUBLIC_API_URL=http://localhost:8080/api
```

Luego ejecutar el frontend:

```bash
npm run dev
```

La aplicación debería quedar disponible en:

```bash
http://localhost:3000
```

---

## Orden recomendado para probar la app

1. Levantar MySQL.
2. Crear la base de datos `lostockistas`.
3. Ejecutar el backend desde `LoStockistas-Back`.
4. Ejecutar el frontend desde `LoStockistas-Front`.
5. Abrir el navegador en `http://localhost:3000`.

---

## Comandos útiles

Instalar dependencias del frontend:

```bash
npm install
```

Ejecutar frontend:

```bash
npm run dev
```

Ejecutar backend:

```bash
gradlew.bat bootRun
```

---

## Notas

Si el frontend no se conecta al backend, revisar que:

* El backend esté corriendo correctamente.
* La URL `NEXT_PUBLIC_API_URL` apunte a `http://localhost:8080/api`.
* La base de datos MySQL esté creada y activa.
* Las credenciales de `application.properties` sean correctas.
* No haya otro servicio usando los puertos `8080` o `3000`.

---
