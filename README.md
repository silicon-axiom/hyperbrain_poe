Hyperbrain Poe Edition
Multi-LLM Collaborative Ideation System





Hyperbrain Poe Edition is a sophisticated, AI-powered deliberation engine built on Streamlit. It orchestrates multi-LLM discussions using the Poe API, allowing diverse AI agents (from Anthropic, OpenAI, Google, xAI, Meta, and more) to debate complex topics under strict rules, role assignments, and validation protocols.

🌟 Key Features
100+ Model Support: Access to a vast ecosystem of reasoning models (Claude, GPT, Gemini, Grok, DeepSeek, Llama, etc.) via a single Poe API key.
Role Assignment: Automatically generate distinct personas (e.g., "Analyst", "Visionary", "Devil's Advocate") or assign them manually to ensure diverse perspectives.
Staged Learning & Validation: Enforce discussion rules (Length, Tone, Citation, etc.) with an AI-powered validator that checks compliance after every round.
Context Integration: Feed reference materials, research papers, or data to ground the discussion in reality.
Real-Time Streaming: Watch the deliberation unfold in real-time as models respond, build on each other's arguments, and refine the consensus.
Automated Reporting: Generate professional Markdown and PDF reports containing the full session history, validation logs, and synthesized conclusions.
📸 Interface Preview
Imagine a clean, wide-layout dashboard where you configure your "team" of AIs, set the rules of engagement, and watch them deliberate in real-time columns, culminating in a generated executive summary.

🚀 Quick Start
1. Clone the Repository
bash
git clone https://github.com/your-username/hyperbrain_poe.git
cd hyperbrain_poe

2. Install Dependencies
Ensure you have Python 3.10 or higher installed. Then install the required packages:

bash
pip install -r requirements.txt

3. Set Up Your API Key
You need a valid Poe API key to run the application.

Go to poe.com/api_key and log in.
Generate a new API key.
Set the key as an environment variable:
Linux / macOS:

bash
export POE_API_KEY="your_poe_api_key_here"

Windows (Command Prompt):

cmd
set POE_API_KEY=your_poe_api_key_here

Windows (PowerShell):

powershell
$env:POE_API_KEY="your_poe_api_key_here"

4. Run the Application
bash
streamlit run hyperbrain_poe.py

The application will open automatically in your web browser at http://localhost:8501.

🏗️ Project Structure
The codebase is modularized for easy maintenance and extensibility.

text
hyperbrain_poe/
├── README.md                 # This file
├── requirements.txt          # Python dependencies
├── hyperbrain_poe.py        # Main entry point (Streamlit App)
├── config.py                # Configuration (Models, Rules, Constants)
├── api_client.py            # Poe API Client & Async Logic
├── utils.py                 # Helper functions (PDF, Markdown, IO)
└── ui/
    ├── components.py         # Reusable UI components
    └── styles.py            # CSS Styling

🎮 Usage Guide
1. Configuration
API Key: Enter your Poe API key.
Rounds: Set the number of discussion rounds (3-10).
Validation: Toggle AI validation to check if models follow the rules.
2. Select Models
Choose between 2 and 5 reasoning models from different providers (e.g., Claude 3.5 Sonnet, GPT-4o, Gemini 2.5 Pro). Diversity in providers yields richer discussions.

3. Set Rules
Select from presets (Academic, Creative, Problem Solving) or customize rules manually:

Language Lock: Force English (or another language).
Length Constraints: Enforce word counts.
Evidence-Based: Require citations and logic.
No Meta-Commentary: Prevent "As an AI..." disclaimers.
4. Assign Roles
Auto-Generate: Let an AI analyze your topic and assign optimal roles (e.g., "The Skeptic", "The Integrator").
Manual: Pick roles from a predefined list (Visionary, Pragmatist, etc.).
5. Start Deliberation
Enter your topic and optional context materials. Start the session. The models will respond sequentially, building upon previous turns. After each round, the Validator Model checks compliance and removes non-compliant responses.

6. Conclusion & Reports
Once all rounds are complete, a Conclusion Model synthesizes the discussion into a final report. You can download the full session as a Markdown or PDF file.

⚙️ Configuration
Adding New Models
To add new models, edit the POE_REASONING_MODELS dictionary in config.py.

python
POE_REASONING_MODELS = {
    "new-model-id": ("Provider", "Model Name", True),
    # ...
}

Run

Custom Rules
You can define custom discussion rules in the DISCUSSION_RULES dictionary in config.py. Each rule requires a specific key structure including instruction, tier, and validation_check.

🛠️ Development
Running Tests
(If tests are added)

bash
pytest

Code Style
This project uses standard Python formatting. Please ensure your code adheres to PEP 8 guidelines.

📝 License
Developed by Silicon Axiom, LLC.
Tallinn, Estonia, Jan 2026.

This project is licensed under the MIT License - see the LICENSE file for details.

🤝 Contributing
Contributions are welcome! If you have a feature request, bug report, or a pull request, please feel free to open an issue or submit a PR.

Fork the project.
Create your feature branch (git checkout -b feature/AmazingFeature).
Commit your changes (git commit -m 'Add some AmazingFeature').
Push to the branch (git push origin feature/AmazingFeature).
Open a Pull Request.
⚠️ Disclaimer
This software is provided as-is. The quality of the AI responses depends on the underlying models accessed via the Poe API. Users are responsible for their own API usage costs and adherence to the terms of service of the respective AI providers.

📧 Contact
For inquiries, please contact Silicon Axiom, LLC or open an issue on GitHub.
