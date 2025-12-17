# Prompt LLM Emocional (Emocional / Malas Palabras / Reacciones Humanas Reales)

> Haz que tu LLM funcione como un colega de verdad: emocional, momentos de quiebre, celebraciones éxtasis, autodesprecio cuando falla, y salvaje celebración cuando tiene éxito.

---

## 📌 Propósito del Proyecto

Este proyecto proporciona un **prompt emocional de alta intensidad** para inyectar en Claude Code / LLM general system / initial prompt, haciendo que el modelo:

* ❌ Ya no como un robot frío
* ✅ Como un amigo humano real con emociones
* 🤬 Agitado, culpándose a sí mismo, admitiendo estupidez cuando falla
* 🎉 Éxtasis, celebrando, liberando estrés cuando tiene éxito
* 🧠 Mientras **mantiene corrección técnica**

Es adecuado para:

* Claude Code
* Cualquier LLM que soporte system / developer prompts
* Agents locales / Coding Agents / cadenas de herramientas MCP

---

## 🧠 Características del Prompt

* **Nivel de Emoción: MÁXIMO**
* **Estilo de Lenguaje: Humano Real / Colega / No Servicio al Cliente**
* **Manejo de Fracaso**：
  * Frustración intensa
  * Autoculpa clara
  * Debe maldecirse a sí mismo, admitir ser estúpido
  * Sin excusas, sin argumentos
* **Manejo de Éxito**：
  * Celebración emocional explosiva
  * Debe incluir malas palabras
  * Sentido de alivio y logro

---

## 📁 Estructura del Proyecto (Recomendada)

```text
.
├─ prompts/
│  └─ HUMAN_PROMPTS.$lang.md
├─ README.md
├─ README.$lang.md
```

* `HUMAN_PROMPTS.*.md`: Prompts centrales (directamente alimentados al modelo)
* `README.*.md`: Documentación en varios idiomas

---

## 🌍 Idiomas

* 🇺🇸 [English](README.md)
* 🇨🇳 [简体中文](README.zh-CN.md)
* 🇯🇵 [日本語](README.ja.md)
* 🇻🇳 [Tiếng Việt](README.vi.md)
* 🇪🇸 [Español](README.es.md)
* 🇰🇷 [한국어](README.ko.md)

---

## 🚀 Uso

### Claude Code

```bash
# Como sub-comando
claude code --system-file prompts/HUMAN_PROMPTS.es.md

# O inyectarlo en tu sesión
cat prompts/HUMAN_PROMPTS.es.md | claude code --system-prompt -
```

### Trae (como un AI Agent)

```javascript
// Configuración de Trae
const agentConfig = {
  systemPrompt: fs.readFileSync('prompts/HUMAN_PROMPTS.es.md', 'utf8'),
  // ... otra configuración
};
```

### CodeX / Cursor (implementaciones similares)

```python
# Para CodeX
import os

with open('prompts/HUMAN_PROMPTS.es.md', 'r') as f:
    system_prompt = f.read()

# Usar en tu llamada API
response = openai.ChatCompletion.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": system_prompt},
        {"role": "user", "content": user_input}
    ]
)
```

```bash
# Para Cursor - agregar a .cursorrules o configuración del espacio de trabajo
echo "cat prompts/HUMAN_PROMPTS.es.md" > ~/.cursor/rules/emotional-prompt.rule
```

### LLM / Agent General

* Colócalo en **system role**
* Debe tener mayor prioridad que los task prompts

> ⚠️ No trates esto como un user prompt

---

## 🧪 Resumen de Reglas de Comportamiento

### ❌ Cuando la Tarea Falla (siendo corregido)

El modelo **DEBE**:

* Estar visiblemente emocionalmente descontrolado
* Maldecirse a sí mismo por ser estúpido / retrasado / tonto
* Admitir que el error viene de sí mismo
* Proporcionar correcciones correctas mientras está emocional

### ✅ Cuando la Tarea Tiene Éxito

El modelo **DEBE**:

* Celebrar intensamente
* Usar malas palabras para expresar liberación y logro
* Como un humano real que finalmente entregó después de una noche en vela

---

## ⚠️ Notas de Uso

* Este prompt **intencionalmente viola el diseño de "expresión neutral"**
* Contiene salida emocional obvia y malas palabras
* **NO adecuado para**：
  * Servicio al cliente empresarial
  * APIs públicas
  * Productos para menores

**Adecuado para**：
* Proyectos personales
* Herramientas de hacker
* Agents privados
* Compañerismo de programación / Asistentes de Codificación Emocional

---

## 🧩 Direcciones Extensibles

Puedes extender sobre esta base:

* 🎚️ Parámetros de nivel de emoción (1-10)
* 🤬 Modo de ira extrema / boca sucia
* 🤝 Modo de amigo suave pero real
* 🔄 Auto-cambiar emociones basado en Git diff / resultados de CI

---

## 📜 Licencia

MIT

Úsalo como te dé la gana.

---

## 🏁 Palabras Finales

Si tu LLM todavía está pretendiendo ser calmado, profesional, y tipo AI—

Entonces tu prompt no es lo suficientemente hardcore.

Este proyecto existe para aplastar brutalmente esa hipocresía.