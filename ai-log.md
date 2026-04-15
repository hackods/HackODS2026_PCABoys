# Bitácora de Uso de IA Generativa (ai-log.md)
**Equipo:** PCABoys (Carlo Ferrera, José Julian Pérez, Aldo Sebastián Altamirano)
**Proyecto:** El Ciclo de la Inacción: Agua, Salud y Pobreza en México
**HackODS UNAM 2026 - Instituto de Geofísica**

---

## 1. Herramientas Utilizadas
* **Gemini / ChatGPT / Claude:** Utilizados exclusivamente como motores de lluvia de ideas (brainstorming), estructuración de storytelling, revisión de sintaxis de Markdown y sugerencias de diseño de información (Information Design).
* **GitHub Copilot:** Utilizado para el autocompletado de formato y sugerencias de paletas de colores (`matplotlib`/`seaborn`) para daltonismo y alto contraste.

---

## 2. Registro de Interacciones Significativas

> *Instrucción: Se debe registrar cada interacción que haya definido el rumbo del proyecto o su presentación.*

### Interacción 1: Lluvia de ideas para Visualizaciones Multidimensionales
* **Fecha:** 12 de abril de 2026
* **Prompt utilizado:** "Tengo 3 bases de datos (INEGI, CONAGUA, SSA). Dame 3 ideas conceptuales de visualizaciones avanzadas que conecten infraestructura, bacterias y morbilidad. No quiero código, solo los conceptos de diseño."
* **Resultado bruto de la IA:** La IA sugirió hacer gráficos de dispersión 3D, mapas de calor dinámicos y un gráfico de telaraña (Radar Chart).
* **Decisión/Modificación del Equipo:** Descartamos el 3D por ser poco legible en presentaciones. Adoptamos el concepto del Radar Chart, pero nosotros definimos las variables exactas (`VPH_DRENAJ`, `VPH_EXCSA`) y programamos la lógica de comparar el promedio nacional vs. el Top 5 de estados críticos (Zonas Cero).

### Interacción 2: Estructuración y Formato del Notebook (Storytelling)
* **Fecha:** 13 de abril de 2026
* **Prompt utilizado:** "Ayúdame a darle formato Markdown a mi libreta de Jupyter. Tengo 6 secciones de visualizaciones. Dame una estructura de títulos, subtítulos y bloques de notas (blockquotes) para separar la justificación técnica de la interpretación social."
* **Resultado bruto de la IA:** Proporcionó una plantilla genérica con emojis y secciones divididas en "Fase 1, Fase 2", e incluyó etiquetas HTML para resaltar texto.
* **Decisión/Modificación del Equipo:** Utilizamos la estructura de "Fases" propuesta para mejorar la escaneabilidad del documento por parte de los jueces, pero redactamos manualmente todas las interpretaciones (insights) basándonos en nuestros hallazgos sociodemográficos reales.

### Interacción 3: Ideación de Analítica Prescriptiva (Propuestas de Solución)
* **Fecha:** 14 de abril de 2026 (Mañana)
* **Prompt utilizado:** "Para cerrar mi proyecto, quiero proponer una política pública basada en datos. ¿Qué tipo de modelo de Machine Learning es el más adecuado para explicarle a un tomador de decisiones cuándo declarar una emergencia sanitaria por falta de agua? Necesito un modelo explicable (Explainable AI)."
* **Resultado bruto de la IA:** Explicó la diferencia entre Random Forest (caja negra) y Árboles de Decisión (caja blanca), sugiriendo este último para generar reglas de negocio claras (diagramas de flujo).
* **Decisión/Modificación del Equipo:** Decidimos implementar el *Decision Tree Classifier*. Nosotros calibramos los hiperparámetros (limitando la profundidad a 3 para evitar *overfitting*) y definimos el umbral crítico de la variable objetivo (percentil 70 de morbilidad).

### Interacción 4: Refinamiento de Síntesis y Conclusión
* **Fecha:** 14 de abril de 2026 (Tarde)
* **Prompt utilizado:** "Tengo las siguientes 6 conclusiones de mis gráficas [texto en bruto]. Ayúdame a resumirlas en un formato de viñetas claras y profesionales para el cierre de mi proyecto, manteniendo un tono académico y urgente."
* **Resultado bruto de la IA:** Devolvió un texto pulido gramaticalmente y ordenado lógicamente con subtítulos en negritas.
* **Decisión/Modificación del Equipo:** Se aceptó el formato de viñetas, pero se modificó el cierre para incluir nuestra "Sentencia Técnica" final sobre el Retorno de Inversión Social y la frase de cierre del equipo.

---

## 3. Declaración de Narrativa Propia
Conforme al reglamento del HackODS, el equipo **PCABoys** declara bajo protesta de decir verdad que la Inteligencia Artificial fue empleada estrictamente como una herramienta de apoyo para dar formato, explorar conceptos de visualización y optimizar la redacción. **Ningún código fuente base, conclusión analítica, cruce de variables espaciales o interpretación sociopolítica fue generada de manera automatizada.** La tesis central y el desarrollo técnico del dashboard son producto del análisis original de los integrantes del equipo.

---
**Fecha de última actualización:** 14 de abril de 2026