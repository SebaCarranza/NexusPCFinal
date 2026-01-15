# 🛒 Nexus PC – E-commerce en React

**Nexus PC** es un **e-commerce desarrollado en React** como **Proyecto Final del curso de React JS en Coderhouse**.  
La aplicación permite navegar productos, gestionar un carrito de compras y finalizar una compra real, generando órdenes en **Firebase Firestore** con control de stock.

---

## 🎯 Objetivo del proyecto

El objetivo de **Nexus PC** es aplicar y consolidar los conceptos fundamentales de React aprendidos durante el curso, integrando una solución completa de e-commerce con base de datos real.

Se trabajó especialmente en:

- Componentización
- Manejo de estado
- Ruteo
- Context API
- Integración con Firebase
- Lógica de negocio (stock, carrito y órdenes)

---

## 🚀 Funcionalidades principales

- 📦 Listado de productos obtenidos desde **Firebase Firestore**
- 🔍 Vista de detalle de cada producto
- 🛒 Carrito de compras global con **Context API**
- 💾 Persistencia del carrito en **LocalStorage**
- ➕ Agregar y eliminar productos
- 🔢 Control de cantidades con validación de stock
- 🚫 Bloqueo de productos sin stock
- 💳 Checkout con formulario validado
- 🧾 Generación de órdenes de compra en Firestore
- 📉 Descuento automático de stock al confirmar la compra
- 🎉 Animación visual al finalizar la compra

---

## 🛠️ Tecnologías utilizadas

### Frontend
- **React**
- **React Router DOM**
- **React Hook Form**
- **Context API**

### Backend / Base de datos
- **Firebase**
  - Firestore (base de datos NoSQL)
  - Batch Writes para actualización segura de stock

### Persistencia
- **LocalStorage**

---

## 📚 Librerías utilizadas

- 🔹 **react-router-dom**: Navegación entre vistas
- 🔹 **react-hook-form**: Manejo y validación del formulario de checkout
- 🔹 **canvas-confetti**: Animación visual al confirmar la compra



🛒 **Manejo del carrito**

El carrito se maneja mediante **Context API**, permitiendo acceso global desde toda la aplicación.

### Productos en el carrito

Cada producto almacenado contiene:

- 🔹 **id**: Identificador interno del producto
- 🔹 **docId**: Identificador del documento en Firestore
- 🔹 **cantidad**: Unidades agregadas

### Beneficios de la separación

- 🔹 Usar **id** para la lógica de interfaz
- 🔹 Usar **docId** para operaciones críticas en Firestore (stock y órdenes)

### Persistencia

- 🔹 El carrito se persiste automáticamente en **LocalStorage**

**Estructura del Proyecto**

src/
│
├── components/
│   ├── NavBar
│   ├── ItemListContainer
│   ├── ItemDetailContainer
│   ├── ItemDetail
│   ├── ItemCount
│   ├── Cart
│   └── Checkout
│
├── contexto/
│   └── CartContext.jsx
│
├── firebase/
│   └── FireBaseConfig.js
│
├── App.jsx
└── main.jsx


💳 **Proceso de Checkout**

1️⃣ Validación del formulario con React Hook Form  
2️⃣ Verificación del stock disponible en Firestore  
3️⃣ Actualización del stock utilizando writeBatch  
4️⃣ Creación de la orden de compra en la colección `ordenes`  
5️⃣ Confirmación visual de la compra  
6️⃣ Limpieza del carrito al finalizar el proceso


✅ **Buenas prácticas aplicadas**

- 🔹 **Componentes reutilizables**  
- 🔹 **Separación clara de responsabilidades**  
- 🔹 **Estado global con Context API**  
- 🔹 **Validaciones**  
- 🔹 **Persistencia controlada de datos**  
- 🔹 **Integración real con base de datos**  
- 🔹 **Manejo de errores y estados límite** (stock insuficiente)


🌐 **Deploy**

El proyecto se encuentra deployado en Vercel:

👉 https://nexus-pc.vercel.app/

👨‍💻 **Autor**

Sebastian Carranza
Curso: React JS – Coderhouse

📄 **Observaciones**

Nexus PC es un proyecto desarrollado con fines educativos, enfocado en simular un e-commerce real, aplicando buenas prácticas de React y una integración completa con Firebase.
