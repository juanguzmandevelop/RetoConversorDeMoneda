# Conversor de Monedas en Java — POO + API + HttpClient + Gson

Este proyecto es un **Conversor de Monedas en Java**, desarrollado con una arquitectura basada en **Programación Orientada a Objetos (POO)**, consumo de API REST con `HttpClient`, análisis de JSON con **Gson**, y una interfaz de usuario por consola.

El conversor permite consultar tasas de cambio reales utilizando la API pública:

👉 https://www.exchangerate-api.com/

---

## Características principales

✔ Arquitectura en POO  
✔ Uso de paquetes organizados (`domain`, `service`, `model`, `ui`)  
✔ Consumo de API con **HttpClient**  
✔ Parsing JSON con **Gson**  
✔ Menú interactivo en consola  
✔ Conversión entre varias monedas  
✔ Manejo de errores básico  
✔ Código limpio, modular y mantenible  

---

## 📁 Estructura del Proyecto

```
src/
└── com
    └── conversor
        ├── Main.java
        ├── domain/
        │     └── Converter.java
        ├── model/
        │     └── ExchangeRateResponse.java
        ├── service/
        │     └── CurrencyApiService.java
        └── ui/
              └── Menu.java
```

---

## 🚀 Tecnologías utilizadas

- **Java 17+**
- **HttpClient (Java Standard Library)**
- **Gson** (Google JSON library)
- **API ExchangeRate**
- **POO (Programación Orientada a Objetos)**

---

## 🧠 Funcionamiento

1. El usuario selecciona una opción en el menú.
2. Se captura la moneda base y la moneda destino.
3. Se envía una solicitud HTTP a la API:
   ```
   https://v6.exchangerate-api.com/v6/TU_API_KEY/latest/<BASE>
   ```
4. Se recibe un JSON con todas las tasas de cambio.
5. Gson convierte el JSON en un objeto `ExchangeRateResponse`.
6. El conversor calcula el valor convertido:
   ```
   resultado = valor * tasa
   ```
7. Se imprime el resultado en pantalla.

---

## 📌 Ejemplo de uso (Vista en consola)

```
***************************************************
 Sea bienvenido/a al Conversor de Moneda =]

 1) USD => ARS
 2) ARS => USD
 3) USD => BRL
 4) BRL => USD
 5) USD => COP
 6) COP => USD
 7) Salir

 Elija una opción válida:
***************************************************

Ingrese el valor a convertir: 4000
=========================================
4000 COP = 0.95 USD
Tasa aplicada: 0.0002378
=========================================
```

---

## 🧩 Paquetes y Clases

### **📦 com.conversor.model**
#### `ExchangeRateResponse`
Representa la respuesta JSON de la API y permite acceder a los valores mediante Gson.

---

### **📦 com.conversor.domain**
#### `Converter`
Contiene la lógica principal para convertir un monto entre dos monedas.

---

### **📦 com.conversor.service**
#### `CurrencyApiService`
Realiza la llamada HTTP a la API y convierte el JSON en un objeto Java.

---

### **📦 com.conversor.ui**
#### `Menu`
Interfaz textual completa que permite al usuario interactuar con el conversor.

---

### **📦 com.conversor**
#### `Main`
Ejecuta la aplicación inicializando el menú.

---

## 🔑 Requisitos

- Java 17 o superior
- Biblioteca Gson agregada al proyecto
- Conexión a Internet
- API Key válida de ExchangeRate API

---

## ▶️ Cómo ejecutar el proyecto

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/tuusuario/conversor-moneda.git
   ```

2. Importar el proyecto en **IntelliJ IDEA**

3. Asegurarse de agregar **Gson** como dependencia

4. Ejecutar la clase:
   ```
   com.conversor.Main
   ```

---

## 🛠 Mejoras futuras

- Validación avanzada de errores  
- Más monedas soportadas  
- Exportar historial de conversiones  
- Manejo de excepciones personalizadas  
- Implementación con herencia y polimorfismo  
- Interfaz gráfica con JavaFX  

---

## 👨‍💻 Autor

Proyecto desarrollado por *Tu Nombre* como parte del aprendizaje de Java, POO y consumo de APIs.

---

## 📜 Licencia

Este proyecto es de uso educativo y libre distribución.
