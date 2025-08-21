
# 🐾 Prueba Técnica — API CRUD de Animales (NestJS + TypeScript)

Este proyecto implementa una **API REST** para gestionar un recurso `animals`, permitiendo crear, consultar, actualizar y eliminar diferentes tipos de animales (`dog`, `cat`, `cow`).  
El desarrollo sigue **arquitectura hexagonal**, principios **SOLID**, y **POO** para encapsular el comportamiento de cada animal.

---

## 🚀 Tecnologías
- [NestJS](https://nestjs.com/) — Framework backend
- [TypeScript](https://www.typescriptlang.org/)
- [Docker & Docker Compose](https://www.docker.com/)
- [Jest](https://jestjs.io/) — Pruebas unitarias
- [Swagger](https://swagger.io/) — Documentación API
- Base de datos: configurable vía `docker-compose`

---

## 📦 Instalación y ejecución

### 🔹 Ejecución en **local**
```bash
# Instalar dependencias
npm install

# Levantar en modo desarrollo
npm run start:dev

# Modo producción
npm run start:prod
````

### 🔹 Ejecución con **Docker** (recomendada)

```bash
# Construir y levantar servicios (API + DB)
docker-compose up --build
```

La API quedará disponible en:
👉 `http://localhost:3000/api`

---

## 📖 Documentación

* **Swagger UI** disponible en:
  👉 `http://localhost:3000/api`

  También puedes revisar la definición en:
  [📄 Swagger Docs](https://github.com/andresfelipe3112/prueba_Andres_Felipe_Pinilla_Meneses/tree/main/documents/swagger)

* **Colección Postman** para probar los endpoints:
  [📄 Postman Collection](https://github.com/andresfelipe3112/prueba_Andres_Felipe_Pinilla_Meneses/tree/main/documents/posmant)

---

## 🧪 Pruebas

Ejecutar las pruebas unitarias con:

```bash
npm run test
```

---

## 📚 Alcance funcional

* **CRUD `/animals`**

  * **Create** → crear un animal (dog | cat | cow) con sus atributos.
  * **Read (by ID)** → obtener un animal por ID con toda su información y el sonido característico.
  * **Read (list)** → listar animales con filtros por tipo y paginación.
  * **Update** → actualizar atributos propios de un animal.
  * **Delete** → eliminar un animal por ID.

---

## 🧩 Comportamiento de dominio

Cada animal implementa:

* `emitSound()` → devuelve el sonido característico.
* `getAttributes()` → devuelve atributos específicos (ej. raza para perros, color para gatos, etc).

---

## 🏗️ Patrones de diseño

* **Factory Pattern** → creación de animales sin usar `if/else` o `switch`.
* **Repository Pattern** → desacoplar persistencia.

---

## ✅ Criterios cumplidos

* Clean Code en TypeScript
* Principios **SOLID**
* Arquitectura hexagonal
* Validaciones con DTOs (`class-validator`)
* Swagger con `@nestjs/swagger`
* Tests unitarios en dominio y casos de uso (Jest)
* Fácil de levantar con `docker-compose up`

---

## 👤 Autor

* **Andrés Felipe Pinilla Meneses**
* [LinkedIn](https://www.linkedin.com/in/andresfelipepinilla/)
* [Email](mailto:andresfelipe3112@gmail.com)

