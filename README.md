# 👨‍🍳 ChefIA - Asistente Culinario con IA

## 📑 Descripción del Proyecto
ChefIA es un sistema basado en **ingeniería de prompts** que funciona como un asistente culinario inteligente. Su propósito es resolver dos problemas comunes en la vida cotidiana:

- **Fatiga por decisión culinaria**: “¿Qué cocino hoy?”
- **Desperdicio de alimentos**: ingredientes que se echan a perder por falta de planificación.

ChefIA convierte una lista de ingredientes disponibles en **recetas creativas, rápidas y saludables**, reduciendo el estrés de la planificación diaria y fomentando un estilo de vida más sostenible.

---

## 🚀 Motivación
- **Impacto en la salud**: fomenta comidas más nutritivas frente a opciones rápidas poco saludables.  
- **Reducción de desperdicio**: propone el uso de sobras y subproductos.  
- **Alivio de la carga mental**: elimina la toma de decisiones diaria sobre qué cocinar.  

---

## 🛠️ Solución Propuesta
ChefIA utiliza **modelos de lenguaje avanzados** (Gemini API) y un **mega-prompt estructurado** que:

1. Asume el rol de **chef y nutricionista experto**.
2. Recibe como entrada:
   - Ingredientes disponibles
   - Tiempo máximo de cocina
   - Restricciones o preferencias (ej: vegetariano, sin gluten)
   - Equipamiento disponible (ej: sartén, microondas)
3. Devuelve:
   - **3 recetas diferentes** con nombre creativo
   - Lista de ingredientes utilizados
   - **Instrucciones paso a paso (máx. 8 pasos)**
   - Beneficio nutricional clave
   - Idea para aprovechar sobras o subproductos

---

## ✅ Viabilidad
- **Técnica**:  
  - Basado en **Google Generative AI (Gemini)**  
  - Desarrollado en **Python** (Jupyter/Colab)  
  - Uso de fast prompting para reducir costos de tokens  

- **Temporal (MVP)**:  
  - Entrega en **7 días**  
  - Diseño y pruebas → Optimización del prompt → Exportación y documentación  

- **Escalabilidad**:  
  - Futura integración en una **web app con Flask/Django**  
  - Expansión a recomendaciones nutricionales personalizadas  

---

## 📦 Instalación y Setup del Entorno
Ejecutar en un notebook de **Google Colab**:

```bash
%pip install -qU 'google-genai>=1.0.0'
%pip install -q google-generativeai

# Configurar la API Key de Google:
from google.colab import userdata
import google.generativeai as genai

GOOGLE_API_KEY = userdata.get('GOOGLE_API_KEY')
genai.configure(api_key=GOOGLE_API_KEY)
