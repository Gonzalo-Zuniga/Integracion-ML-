# **Integracion-ML**

Este repositorio contiene los elementos necesarios para comprender la implementación de un flujo de *Machine Learning* orientado a la detección de anomalías y su integración futura con servicios AWS para automatización, notificación y despliegue.

---

## ** Archivos del repositorio**

### **1. `Sumativa_S6.ipynb` — Programa principal (ML)**

Este notebook contiene **todo el desarrollo del modelo**, incluyendo:

- Preparación y análisis exploratorio de datos  
- Construcción del modelo de Machine Learning  
- Evaluación, métricas y resultados  
- Pruebas de umbrales para alertas  
- Lógica de identificación de casos anómalos  

**Apertura recomendada:**
- Google Colab  
- Jupyter Notebook  

**Importante:**  
El dataset **no está incluido** debido a contener información sensible.  
Si se requiere acceso, solicitar vía correo: **xxxxx**.

Debido a la cantidad de celdas, el notebook puede tardar en ejecutar completamente.  
Se recomienda usar **“Ejecutar todo”** en Colab o Jupyter.

---

### **2. `back-end | front-end.ipynb` — Arquitectura AWS + HTML de correo**

Este notebook contiene:

- Explicación y construcción del **diagrama del backend**, utilizado para generar la imagen PNG incluida en el repositorio.  
- Descripción de la **arquitectura futura** para implementar un flujo automatizado en AWS:
  - Amazon S3 (entrada de datos)  
  - AWS Glue (ETL)  
  - Amazon S3 (salida)  
  - SageMaker (procesamiento con ML)  
  - Athena (consulta de resultados)  
  - SNS (envío de alertas por correo electrónico)  

- Una **plantilla en HTML** para simular el correo de notificación enviado por Amazon SNS cuando se detecta una anomalía.

 **Nota técnica:**  
Este notebook debe abrirse **exclusivamente en Google Colab**, debido al uso de librerías específicas no disponibles por defecto en entornos locales.

---

### **3. `Diagrama AWS.png` — Arquitectura del backend**

La imagen representa el diagrama generado desde el notebook correspondiente.  
Refleja cómo sería la implementación del backend diseñada para:

- Procesar los datos  
- Ejecutar el modelo de ML  
- Detectar anomalías  
- Generar alertas  
- Enviar notificaciones mediante SNS  

Este flujo cubre **desde la entrada de datos hasta el envío de un correo HTML** con la alerta.

---

## ** Resumen del flujo de arquitectura (alto nivel)**

1. **Amazon S3 (input)** → almacenamiento del dataset original  
2. **AWS Glue** → procesos ETL  
3. **Amazon S3 (output)** → almacenamiento de datos transformados  
4. **Amazon SageMaker** → ejecución del modelo de Machine Learning  
5. **Amazon Athena** → consulta de los resultados procesados  
6. **Amazon SNS** → envío automático de alertas  
7. **HTML básico** → simulación del correo recibido por el usuario final  

---

## ** Contacto para dataset**

Debido a la sensibilidad de los datos, el dataset debe solicitarse a:

📧 **g.zuigaguerra@uandresbello.edu**

---

## **✔ Recomendación de uso del repositorio**

1. Abrir **Sumativa_S6.ipynb** → ejecutar todo para visualizar modelo, métricas y resultados.  
2. Abrir **back-end | front-end.ipynb** en **Google Colab** → revisar diagrama, arquitectura y correo HTML.  
3. Revisar **Diagrama AWS.png** → arquitectura visual del backend y flujo de alertas.

---

