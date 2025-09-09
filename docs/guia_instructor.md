# Guía del Instructor: Evaluación de IA Generativa

## Sección 1: ¡Hola, Facilitador!

¡Bienvenido a esta aventura de aprendizaje! Esta guía está diseñada para ayudarte a facilitar una sesión súper interesante sobre cómo evaluar sistemas de inteligencia artificial generativa (*Generative AI*).

¿Por qué usamos este enfoque? Porque creemos que aprender debe ser como armar un rompecabezas: primero entiendes para qué sirve cada pieza (la teoría), luego practicas armándolo (el taller), y al final puedes ver la imagen completa (la comprensión profunda).

Tu papel es ser el guía que ayuda a los estudiantes a conectar los puntos entre lo que aprenden en la presentación y lo que experimentan en el código. ¡No te preocupes si no eres un experto absoluto! Esta guía te dará todo lo que necesitas.

---

## Sección 2: ¿Qué es todo esto?

### IA Generativa (*Generative AI*)
Imagínate que tienes un robot muy inteligente que puede escribir historias, traducir idiomas, o resumir textos largos. Ese robot usa IA generativa. Pero aquí viene el problema: **¿cómo sabemos si el robot está haciendo un buen trabajo?**

Es como cuando un niño te cuenta una historia que inventó. Tú puedes decir si es buena o no, pero ¿cómo le explicas eso a una computadora? ¡Ahí es donde entran las métricas de evaluación!

### Métricas Automáticas (*Automatic Metrics*)
Son como reglas matemáticas que la computadora usa para "calificar" el trabajo de la IA. Las dos más famosas son:

**Métricas de N-gramas:**

**BLEU (*Bilingual Evaluation Understudy*)**: 
- Es como un profesor que cuenta cuántas palabras están en el lugar correcto
- Se fija mucho en la precisión: "¿Las palabras que usaste son las correctas?"
- Problema: No se preocupa si faltaron cosas importantes

**ROUGE (*Recall-Oriented Understudy for Gisting Evaluation*)**:
- Es como un profesor que se asegura de que no se te olvidó nada importante
- Se fija más en la cobertura: "¿Incluiste todo lo que debías incluir?"
- Es súper útil para evaluar resúmenes

**Métricas basadas en embeddings:**

**BERTScore**: 
- Es como tener un profesor que entiende sinónimos
- Sabe que "película" y "film" significan lo mismo
- Usa inteligencia artificial (BERT) para entender el significado

**Métricas aprendidas:**

**BLEURT**: 
- Es como un profesor entrenado específicamente para calificar como los humanos
- Ha "estudiado" millones de ejemplos de evaluaciones humanas
- Es la más sofisticada pero también la más lenta

### Evaluación Humana (*Human Evaluation*)
A veces las computadoras no pueden juzgar cosas como:
- Si un texto suena natural (*fluency*)
- Si tiene sentido lógico (*coherence*)
- Si es creativo o aburrido
- Si los hechos son correctos

Para esto necesitamos humanos reales que lean y califiquen los textos.

**Marco MQM (*Multidimensional Quality Metrics*)**:
- Es como tener una rúbrica estándar para evaluar
- MQM-lite usa tres dimensiones principales:
  - *Adequacy*: ¿Se preservó bien el contenido original?
  - *Fluency*: ¿Suena natural y es gramaticalmente correcto?
  - *Consistency*: ¿Es coherente internamente?

---

## Sección 3: El Plan de Juego (Minuto a Minuto)

### **Preparación (5 minutos antes de empezar)**
- [ ] Asegúrate de que todos puedan acceder al notebook (Google Colab)
- [ ] Ten la presentación lista
- [ ] Prepara ejemplos adicionales por si alguien pregunta

### **Introducción y Motivación (10 minutos)**
**Qué hacer:**
- Empieza con la pregunta del millón: "¿Cómo sabemos si nuestra IA es buena?"
- Usa la analogía de comparar estudiantes: imaginen que tienen que decidir cuál de dos estudiantes escribió el mejor ensayo

**Señal de que va bien:** Los estudiantes empiezan a proponer ideas como "leemos los textos" o "comparamos con un ejemplo perfecto"

**Si se pone lento:** Pregunta "¿Cómo calificarían ustedes un ensayo? ¿Y si tuvieran que calificar 1000 ensayos en una hora?"

### **Módulo 1: Métricas N-gram - BLEU y ROUGE (15 minutos)**
**Presentación (8 minutos):**
- Explica las métricas n-gram como "los contadores de palabras"
- BLEU = precisión, ROUGE = cobertura
- **Momento clave:** Muestra cómo fallan con sinónimos: "película" vs "film"
- Enfatiza: "Son rápidas y simples, pero tienen limitaciones"

**Taller (7 minutos):**
- Los estudiantes experimentan con BLEU y ROUGE
- Diles: "Prueben con sinónimos y cambios de orden - ¿qué pasa?"
- **Pregunta clave:** "¿Por qué las métricas n-gram luchan con paráfrasis?"

**Señales de éxito:** Comentarios como "¡No entiende que 'auto' y 'carro' son lo mismo!"

### **Módulo 2: BERTScore - Métricas con Embeddings (15 minutos)**
**Presentación (8 minutos):**
- Empieza con el problema de n-grams: "¿Qué pasa cuando digo 'film' en lugar de 'movie'?"
- Presenta BERTScore como "el evaluador que entiende significados"
- **Analogía clave:** Es como tener un traductor inteligente en tu cerebro
- Explica: usa BERT para entender que palabras diferentes pueden significar lo mismo

**Taller (7 minutos):**
- Comparar BERTScore vs métricas n-gram
- **Ejercicio:** Casos donde n-grams fallan pero BERTScore funciona
- **Pregunta:** "¿Cuándo vale la pena usar métricas más lentas pero más inteligentes?"

### **Módulo 3: BLEURT - Métricas Aprendidas (10 minutos)**
**Presentación (5 minutos):**
- **Evolución:** "Hemos ido de contar palabras → entender significados → aprender de humanos"
- Presenta BLEURT como "la métrica entrenada para pensar como humano"
- **Analogía:** Es como un estudiante de doctorado que ha leído millones de evaluaciones
- Explica trade-offs: más precisa pero más lenta y compleja

**Taller (5 minutos):**
- Comparación rápida de todas las métricas
- **Ejercicio:** Ver todas las métricas en un mismo ejemplo
- **Pregunta:** "¿Cuándo vale la pena la complejidad extra?"

### **Módulo 4: Evaluación Humana con MQM (15 minutos)**
**Presentación (5 minutos):**
- Introduce el marco MQM: "Una rúbrica estándar para evaluar IA"
- Explica MQM-lite: Adecuación, Fluidez, Consistencia
- **Conexión:** "Las máquinas miden palabras, los humanos miden experiencia"

**Actividad Grupal (10 minutos):**
- Forma grupos de 3-4 personas
- **Instrucciones:** "Usen el marco MQM para evaluar dos textos"
- **Proceso:** Lean → Discutan → Califiquen en las 3 dimensiones
- **Circula y escucha:** Material para la discusión final

**Truco del instructor:** Celebra los desacuerdos: "¡Perfecto! Así funciona la evaluación humana real"

### **Módulo 5: La Gran Comparación (10 minutos)**
**El momento "Aha!" (8 minutos):**
- Los estudiantes comparan sus evaluaciones MQM con TODAS las métricas automáticas
- **Visualización:** Gráficos lado a lado de humanos vs. máquinas
- **Pregunta clave:** "¿Qué métrica se parece más a su juicio humano? ¿Por qué?"

**Cierre (2 minutos):**
- Resume: "No hay métrica perfecta - cada una tiene su lugar"
- **Pregunta final:** "¿Cómo combinarían estas métricas en un proyecto real?"

### **Preguntas y Discusión (5 minutos)**

---

## Sección 4: Consejos Clave

### **Para mantener la energía alta:**
- **Usa analogías simples:** BLEU = contador de palabras, ROUGE = detector de cosas faltantes, Humanos = jueces con corazón
- **Celebra los errores:** Cuando algo sale "mal" en el código, di "¡Perfecto! Eso nos enseña algo importante"
- **Haz preguntas constantemente:** En lugar de explicar todo, pregunta "¿Qué creen que va a pasar si...?"

### **Problemas técnicos comunes:**
- **El notebook no carga:** Ten un Plan B con los resultados pre-calculados
- **Error de instalación:** Google Colab usualmente funciona, pero ten screenshots de los resultados esperados
- **Estudiantes perdidos:** Asígna "compañeros de laboratorio" - que trabajen en pares

### **Dudas frecuentes y cómo responderlas:**
**"¿Por qué las métricas automáticas dan resultados raros?"**
- Respuesta: "Cada métrica 've' algo diferente: BLEU cuenta palabras exactas, BERTScore entiende significados, BLEURT imita humanos. Es como tener diferentes tipos de doctores para diferentes síntomas"

**"¿Cuál métrica es la mejor?"**
- Respuesta: "Depende de tu 'receta': ¿Necesitas velocidad? → n-grams. ¿Precisión semántica? → BERTScore. ¿Correlación humana? → BLEURT. ¿Evaluación completa? → Combinar todas"

**"¿Por qué no usar solo BLEURT si es la más avanzada?"**
- Respuesta: "Es como preguntar por qué no usar siempre un Ferrari. A veces necesitas algo más simple, barato y rápido para hacer el mandado"

**"¿Cómo saber si mis métricas automáticas son confiables?"**
- Respuesta: "Compáralas con evaluación humana en una muestra pequeña. Si coinciden, puedes confiar. Si no, ajusta tu estrategia"

### **Señales de que todo va bien:**
- Los estudiantes hacen preguntas espontáneas
- Escuchas "¡Ah, ya entendí!" durante los ejercicios
- Hay debate durante la evaluación humana
- Al final, pueden explicar cuándo usarían cada métrica

### **Señales de alarma:**
- Silencio total durante las actividades
- Nadie hace preguntas
- Los estudiantes no participan en la evaluación grupal

**¿Qué hacer si algo no funciona?**
- **Reenfócate en lo conceptual:** Si la tecnología falla, usa ejemplos en la pizarra
- **Usa la analogía de calificar exámenes:** Todos entienden la diferencia entre contar errores ortográficos vs. evaluar la creatividad
- **Haz más interactivo:** Convierte la sesión en un debate sobre "¿Cómo calificarían ustedes a ChatGPT?"

### **Mensaje final para ti, facilitador:**
Recuerda que no tienes que ser un experto perfecto. Tu trabajo es guiar la curiosidad de los estudiantes y ayudarles a descubrir estos conceptos por sí mismos. ¡Los mejores maestros son los que aprenden junto con sus estudiantes!

**¡Tú puedes hacer esto! 🚀**
