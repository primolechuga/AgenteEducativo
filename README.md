# Agente Educativo  🤖📚

Este proyecto es un **Agente Educativo Inteligente** que permite generar materiales educativos a partir de la estructura de un curso. El agente procesa archivos en formatos `.txt`, `.pdf` o `.docx` que contienen el programa del curso, extrae la información importante mediante técnicas de procesamiento de lenguaje natural y utiliza el LLM de Gemini para generar contenido educativo por tema. Los materiales generados incluyen:

- **Notas de clase**
- **Problemas de práctica con soluciones**
- **Preguntas para discusión**
- **Objetivos de aprendizaje**
- **Recursos de aprendizaje sugeridos**

Finalmente, el agente valida la calidad del material generado y entrega un PDF con todo el contenido. 

Dentro de los archivos del proyecto, se incluyen materiales de ejemplo para probar el agente y verificar su funcionamiento. 

---

## Características

- **Entrada Flexible:** Acepta archivos en formato `.txt`, `.pdf` o `.docx` que contengan la estructura del curso.
- **Extracción de Información:** Utiliza procesamiento de lenguaje natural para extraer la información relevante del programa.
- **Generación de Contenidos:** Con el LLM de Gemini, genera diversos materiales educativos de forma automática y personalizada.
- **Validación de Calidad:** Evalúa la calidad del material generado mediante métricas de relevancia, completitud, claridad, entre otras.
- **Salida en PDF:** Convierte el contenido generado a PDF, facilitando su distribución y uso en el aula.

---

## Requisitos

- **API Key de Gemini:**  
  Para utilizar el LLM de Gemini, se debe disponer de una API Key. [Genera tu API Key aquí](https://ai.google.dev/gemini-api/docs/api-key?hl=es-419).

- **Dependencias de Python:**  
  Asegúrate de tener instaladas las siguientes dependencias:
  - `pypandoc`
  - `markdown`
  - `ipywidgets`
  - Otras dependencias que se indiquen en la documentación interna.

- **Distribución LaTeX:**  
  Para la conversión a PDF, es necesario tener instalada una distribución de LaTeX (por ejemplo, **MiKTeX** o **TeX Live**).  
  _Nota:_ Si encuentras errores de paquetes faltantes (como `unicode-math.sty`), actualiza o instala los paquetes requeridos.

---

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/primolechuga/AgenteEducativo
   cd AgenteEducativo
    ```
2. Crea y activa un entorno virtual (opcional pero recomendado):
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```

3. Instala las dependencias

4. Configura tu API Key de Gemini según se indique en el archivo de configuración o en las instrucciones del proyecto.

---
## Uso
El proyecto se compone de varios módulos, cada uno responsable de una parte del proceso:

1. **Rate Limiter**: Controla la frecuencia de las solicitudes a la API de Gemini.
2. **LLM Engine**: Inicializa el modelo de lenguaje (Gemini) utilizando la API Key.
3. **Content Generator**: Utiliza el LLM para generar el contenido educativo por tema.
4. **Document Processor**: Procesa y extrae la información importante del archivo del programa del curso.

5. **dict_to_pdf**: Convierte el contenido generado a PDF usando pypandoc.
6. **Evaluator**: Evalúa la calidad del contenido generado basándose en diversas métricas.

## Ejecución en Jupyter Notebook
El repositorio incluye celdas interactivas (usando ipywidgets) para la carga del archivo, el procesamiento y la generación del material educativo. La celda final ejecuta el agente y genera el PDF. Asegúrate de ejecutar las celdas en el siguiente orden:

**Inicialización de módulos**:
Ejecuta las celdas correspondientes a Rate Limiter, LLM Engine, Content Generator, Document Processor, dict_to_pdf y Evaluator.

**Ejecución del Agente**:
La última celda contiene el agente interactivo que permite:

* Subir el archivo .
* Procesar el archivo .
* Generar y validar el contenido educativo.
* Descargar el PDF generado.
---
## Uso Responsable
Es importante validar la información resultante del proceso y usar el material generado con responsabilidad. El contenido producido por el agente debe ser revisado por expertos antes de su aplicación en entornos educativos, ya que puede requerir ajustes y adaptaciones según el contexto.

---

## Auditoría
| Nombre | Correo electrónico |
| --- | --- |
| Jerónimo Ledesma Patiño | [jledesmap@unal.edu.co](mailto:jledesmap@unal.edu.co) |
| Juan Esteban Cadavid Arango | [jucadavida@unal.edu.co](mailto:jucadavida@unal.edu.co) |

--- 
¡Disfruta generando contenido educativo con tu Agente Educativo Inteligente! 🚀