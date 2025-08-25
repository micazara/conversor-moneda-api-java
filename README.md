# 💱 Conversor de Monedas en Java

Este es un **conversor de monedas por consola** desarrollado en **Java**.  
Consume la API pública de [ExchangeRate API](https://www.exchangerate-api.com/) para obtener tasas de cambio en tiempo real y permite realizar conversiones entre distintas monedas.

# Índice

- [ Caracteristicas](#caracteristicas)
- [🛠️ Tecnologías utilizadas](#️-tecnologías-utilizadas)
- [▶️ Ejecución manual con `javac`](#️-ejecución-manual-con-javac)
- [🔑 API Key](#-api-key)
- [⚙️ Agregar Gson en Eclipse](#️-agregar-gson-en-eclipse)
- [📝 Uso](#-uso) 
---

##  Caracteristicas

- Menú interactivo por consola.
- Conversión en tiempo real entre:
  - Dólar (USD) ↔ Peso argentino (ARS)
  - Dólar (USD) ↔ Real brasileño (BRL)
  - Dólar (USD) ↔ Peso colombiano (COP)
  - Dólar (USD) ↔ Peso chileno (CLP)
- Manejo de errores de entrada.
- Historial de conversiones realizadas durante la ejecución.

---

## 🛠️ Tecnologías utilizadas

- **Java 17+**
- **HttpClient** para realizar las peticiones HTTP.
- **Gson** para parsear las respuestas JSON.
- **ExchangeRate API** como proveedor de datos de conversión.

---

## ▶️ Ejecución manual con `javac`

1. Cloná este repositorio:
  ```bash
   git clone https://github.com/tuusuario/conversor-monedas-java.git
   cd conversor-monedas-java
```

3. Descargá [Gson](https://repo1.maven.org/maven2/com/google/code/gson/gson/2.13.0/gson-2.13.0.jar)

Guardalo dentro de una carpeta lib/ en tu proyecto.
La estructura quedaría:
.
├─ bin/
├─ lib/
│   └─ gson-2.13.0.jar
├─ src/
└─ README.md

3. Compilá el proyecto:
  ```bash 
  javac -d bin -cp "lib/gson-2.13.0.jar" src/com/aluracursos/modelos/*.java src/com/aluracursos/principal/*.java
```
4. Ejecutá la aplicación:
  ```bash
  java -cp "bin;lib/gson-2.13.0.jar" com.aluracursos.principal.Principal
```

---

## 🔑 API Key

Este proyecto requiere una API Key de ExchangeRate API. En la clase HttpManager.java encontrarás esta línea:

  ```bash
this.apiKey = "TU_API_KEY";
```

👉 Reemplazá TU_API_KEY por tu propia clave obtenida en [ExchangeRate API](https://www.exchangerate-api.com/).

--- 

## ⚙️ Agregar Gson en Eclipse

Si usás **Eclipse**, podés agregar Gson sin crear lib/ ni compilar con -cp manualmente:

1. Click derecho sobre el proyecto → **Properties.**
2. En el menú de la izquierda, elegí **Java Build Path.**
3. Pestaña **Libraries** → botón **Add External JARs….**
4. Seleccioná el archivo **gson-2.13.0.jar** (puede estar en Descargas o donde lo hayas guardado al descargarlo).
5. Aceptá → Eclipse lo mete automáticamente en el **classpath** del proyecto.

---

## 📝 Uso

Este proyecto fue creado con fines **educativos** y para **práctica personal**.  
Podés usarlo o modificarlo libremente, pero **no se ofrece soporte ni garantías** de funcionamiento.  
Si lo compartís, agradezco que mantengas la referencia al autor original.
