# FundindFlow_Automatización-n8n
Sistema Inteligente de Monitorización y Gestión de Convocatorias de Financiación para ONG de Cooperación Internacional
# FundingFlow: Sistema Inteligente de Monitorización y Gestión de Convocatorias 🌍🤖

[cite_start]**Autor:** Jesús Ignacio Briceño Alarcón [cite: 8]  
[cite_start]**Contexto:** Proyecto Final - Máster en Automation & AI (Nuclio Digital School) [cite: 1-2]  
[cite_start]**Sector:** Cooperación Internacional al Desarrollo / Tercer Sector [cite: 6, 153]

---

## 📌 Visión General
[cite_start]FundingFlow es una solución de **automatización inteligente (Low-code + AI)** diseñada para resolver la ineficiencia estructural en la captación de fondos de las ONG de cooperación internacional [cite: 3-6, 15, 202]. [cite_start]Actualmente, el personal técnico dedica entre 5 y 8 horas semanales a la búsqueda manual de fondos en portales dispersos, un proceso fragmentado que genera una pérdida de oportunidades de entre el 20% y el 35% [cite: 13-14, 168, 185].

[cite_start]Este sistema transforma un proceso reactivo en un **flujo proactivo, centralizado y escalable**, logrando una reducción del tiempo de búsqueda manual del **85%**[cite: 21, 203, 393].

## 🏗️ Arquitectura del Sistema
[cite_start]El sistema se compone de **5 flujos especializados** orquestados en **n8n Cloud (v2.9.3)**[cite: 22, 525, 839]:

1. [cite_start]**Módulo de Captura Multicanal:** Monitorización continua (cada 6h) de fuentes RSS (Grant4EU, TerraViva Grants, FundsforNGOs) y scraping ético de portales institucionales como AECID y PNUD [cite: 541-544, 580, 922].
2. [cite_start]**Módulo de Extracción con IA:** Implementación de **OpenAI GPT-4o-mini** para estructurar campos técnicos (fechas, montos, sectores, elegibilidad) a partir de texto semi-estructurado con una precisión superior al 90% [cite: 17, 548-551, 629-631, 1025].
3. [cite_start]**Módulo de Alertas Segmentadas:** Notificaciones proactivas vía Telegram, Slack y Gmail, filtradas por lógica condicional según sector temático y región geográfica [cite: 556, 743-767].
4. [cite_start]**Gestión de Pipeline:** Control integral del ciclo de vida de la propuesta (desde la detección hasta la resolución definitiva) centralizado en Google Sheets [cite: 31, 567-575, 720-721].
5. [cite_start]**Reporting Ejecutivo:** Generación semanal de informes analíticos asistidos por IA para la toma de decisiones estratégica de la dirección general [cite: 556, 772-780, 958].

## 📊 Impacto y ROI
* [cite_start]**Eficiencia:** Reducción comprobada de la carga horaria administrativa de 11-18 h/semana a solo ~2 h de supervisión técnica [cite: 393-394, 1082].
* [cite_start]**Velocidad:** Capacidad de respuesta y detección de nuevas convocatorias en <12h frente a las 48-72h del proceso manual tradicional[cite: 21, 948].
* [cite_start]**ROI Estimado:** Retorno de inversión proyectado entre **2.111% y 8.525%** basado en el ahorro de tiempos de personal y la recuperación de oportunidades de financiación perdidas [cite: 23, 860-870].

## 🛠️ Tecnologías Utilizadas
* [cite_start]**Orquestador:** n8n (Arquitectura compatible con Cloud y Self-hosted)[cite: 462, 839].
* [cite_start]**IA:** OpenAI API (Modelos GPT-4o-mini para procesamiento de lenguaje natural) [cite: 17, 629-631, 2152].
* [cite_start]**Persistencia de Datos:** Google Sheets (Diseño escalable a PostgreSQL para entornos de alta concurrencia) [cite: 18, 715-716].
* [cite_start]**Comunicación:** Telegram Bot API, Slack API y Gmail (Integración nativa vía OAuth2)[cite: 20, 827, 2124].

## 🚀 Instalación y Uso
Para replicar estos flujos en su propia instancia de n8n, siga estos pasos:

1. [cite_start]**Descarga:** Obtenga los archivos `.json` ubicados en la carpeta `/flujos-json` de este repositorio [cite: 1226-1229].
2. [cite_start]**Importación:** En el editor de n8n, cree un nuevo flujo y seleccione **"Import from File"**[cite: 1228].
3. [cite_start]**Configuración de Seguridad (Importante):** Por razones de ciberseguridad y protección de datos, los archivos JSON han sido anonimizados para eliminar credenciales estáticas [cite: 828-832, 902]. [cite_start]**Es obligatorio que cada usuario configure sus propias credenciales (API Keys, Tokens y OAuth2)** localmente para restablecer la funcionalidad de los nodos de OpenAI, Google Sheets y canales de mensajería[cite: 827].
4. [cite_start]**Despliegue:** Consulte las notas de configuración en el Anexo E para ajustar los disparadores temporales según las necesidades específicas de su organización[cite: 146, 2150].

---
[cite_start]*Este proyecto busca democratizar el acceso a la tecnología de vanguardia para organizaciones sociales, permitiendo que el talento humano se enfoque en el impacto y no en la administración de datos.* [cite: 1128]
