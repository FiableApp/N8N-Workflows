# N8N-Workflows

📊 FIAble – Copiloto Financiero Inteligente

FIAble es un agente conversacional financiero construido sobre n8n que se conecta con WhatsApp para ayudar a los usuarios a:

🎯 Crear planes de ahorro personalizados para metas específicas

📊 Hacer tracking automático de gastos a partir de correos electrónicos y transacciones almacenadas en Supabase

💡 Ofrecer insights financieros y consejos de ahorro basados en los patrones de consumo

El objetivo es que cada persona tenga un copiloto financiero cercano, empático y motivador que le permita tomar el control de sus finanzas de manera simple.

🚀 Arquitectura del flujo (n8n)

Este proyecto está orquestado en n8n con los siguientes componentes:

Webhook (WhatsApp) → recibe mensajes entrantes de los usuarios.

Edit Fields → normaliza la data entrante (ID del usuario, fecha, mensaje, etc.).

Simple Memory (LangChain) → gestiona el contexto de cada sesión de usuario.

AI Agent (OpenRouter + GPT) → motor de conversación, con reglas de personalidad y herramientas conectadas.

Supabase Tools:

📂 Usuarios → registro de usuarios nuevos y gestión de estados.

💳 Transacciones → consulta de gastos en un rango de fechas.

📬 Proveedores → correos asociados como fuentes de información.

HTTP Request → envía la respuesta procesada de vuelta al usuario en WhatsApp.

Google Docs / Google Drive Tools → generación y almacenamiento de reportes/documentos.

🧠 Identidad y reglas de FIAble

Conversacional y amigable, con tono positivo y motivador

Explica en lenguaje sencillo, sin jerga financiera innecesaria

Mantiene contexto de las conversaciones (memoria por sesión de usuario)

Opciones principales que siempre ofrece al usuario:

Crear planes de ahorro personalizados para metas específicas

Hacer tracking de gastos y dar insights

⚠️ Si el usuario pregunta por el cumplimiento de su meta, FIAble responde con un link a su Dashboard FIAble:
👉 Tu Dashboard FIAble

⚙️ Instalación y despliegue

Clona este repositorio:

git clone https://github.com/tu-usuario/fiable.git
cd fiable


Configura n8n (local o en servidor):

Instala dependencias de n8n

Levanta el editor (n8n start)

Importa el flujo (workflow.json) desde este repo en tu instancia de n8n.

Configura credenciales necesarias:

Supabase (API key y URL)

OpenRouter API (para LLMs)

Gmail API (para lectura de correos)

WhatsApp provider API (Webhook URL + API Key)

📂 Estructura del repo

README.md → este documento

workflow.json → definición del flujo de n8n

docs/ → guías adicionales (ej. set up de Supabase, Google APIs)

examples/ → conversaciones de prueba y transacciones dummy

🔮 Futuras mejoras

Integración con dashboards interactivos en tiempo real

Recomendaciones personalizadas con IA según hábitos de consumo

Notificaciones proactivas de ahorro vía WhatsApp

🤝 Contribuciones

¡Las contribuciones son bienvenidas!
Abre un issue o haz un pull request con mejoras y nuevas ideas.
