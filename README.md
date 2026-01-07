# Hyperbrain Poe Edition - Multi-LLM Collaborative Ideation System

A Streamlit-based web interface for orchestrating multi-LLM deliberations via the Poe API.

## Features

- **Multi-Provider Support:** Access to 100+ AI models (Anthropic, OpenAI, Google, xAI, Meta, etc.).
- **Role Assignment:** AI-generated or manual role assignment for diverse perspectives.
- **Context Support:** Integration of background materials and references.
- **Configurable Rules:** Tiered discussion rules with presets (Academic, Creative, etc.).
- **Compliance Validation:** Automated validation of responses against rules using AI.
- **Reporting:** Automatic generation of Markdown and PDF reports.

## Setup

1. **Clone the repository**
   git clone <your-repo-url>
   cd hyperbrain_poe

2. **Install dependencies**
   pip install -r requirements.txt

3. **Set API Key**
   export POE_API_KEY="your_key_from_poe.com/api_key"

4. **Run the app**
   streamlit run hyperbrain_poe.py

## Configuration
Edit config.py to add new models, rules, or role templates.

## License
Developed by Silicon Axiom, LLC. Tallinn, Estonia, Jan 2026.
