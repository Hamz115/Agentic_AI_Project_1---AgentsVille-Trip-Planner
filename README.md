# AgentsVille Trip Planner

**Course:** Udacity Agentic AI / Generative AI  
**Project:** Agentic AI Project 1 — AgentsVille Trip Planner  
**Submission:** June 2026

An AI-powered travel planning notebook that uses agentic prompting techniques to build, evaluate, and revise a personalized itinerary for a fictional trip to **AgentsVille**.

---

## Project Overview

This project implements a travel-planning agent that creates a structured vacation itinerary from traveler preferences, budget, dates, weather data, and available activities.

The project demonstrates several core agentic AI patterns:

- **Role-based prompting** — the itinerary agent acts as a specialized travel planner
- **Chain-of-thought style planning** — the agent reasons through traveler preferences, weather, budget, and scheduling constraints
- **Structured outputs** — generated plans are parsed into Pydantic models
- **Evaluation functions** — itinerary quality is checked against budget, date, activity, interest, and weather constraints
- **Tool use** — helper tools retrieve activities, run calculations, and evaluate generated plans
- **ReAct prompting** — the revision agent iteratively reasons, acts, observes, and improves the itinerary
- **Feedback loops** — the plan is revised after evaluation and traveler feedback

---

## Status

Project implementation is complete and was submitted to Udacity.

Completed items:

- Vacation information model and sample traveler data
- Mock weather and activities API usage
- Itinerary data models with Pydantic
- Initial itinerary generation agent
- Evaluation functions for itinerary validity
- Budget and schedule checks
- Weather compatibility checks
- Tool definitions for ReAct workflow
- Itinerary revision agent
- Final readable travel plan output
- Notebook executed successfully with saved outputs

---

## Project Structure

```text
.
├── project_starter.ipynb   # Main completed notebook
├── project_lib.py          # Helper classes, mock APIs, and shared utility code
├── requirements.in         # Direct Python dependencies
├── requirements.txt        # Locked/resolved dependency list
├── README.md               # Project overview and usage guide
└── .gitignore              # Excludes local secrets, logs, venv, and generated artifacts
```

Local-only files intentionally not committed:

```text
.env
.venv/
Logs/
udacity_project1_submission/
*.zip
__pycache__/
```

---

## Main Notebook Sections

The notebook is organized around the full itinerary-planning workflow:

1. **Initial Setup** — dependencies, OpenAI/Vocareum client, and model selection
2. **Define Vacation Details** — traveler preferences, destination, dates, and budget
3. **Review Weather and Activity Schedules** — mock external API data for AgentsVille
4. **The ItineraryAgent** — structured travel-plan generation
5. **Evaluating the Itinerary** — validation and quality checks
6. **Defining the Tools** — calculator, activity lookup, evaluation, and final output tools
7. **The ItineraryRevisionAgent** — ReAct-based itinerary revision loop
8. **Final Output** — readable final trip plan and narration

---

## Setup

### Requirements

- Python 3.12+
- OpenAI-compatible API access through Udacity/Vocareum or OpenAI
- Jupyter Notebook or VS Code notebook support

### Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

On Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Variables

Create a local `.env` file. This file is ignored by git.

For the Udacity/Vocareum endpoint:

```text
OPENAI_API_KEY=your_vocareum_key
OPENAI_BASE_URL=https://openai.vocareum.com/v1
```

For the regular OpenAI endpoint, use your OpenAI key and remove or adjust `OPENAI_BASE_URL` as needed.

---

## Running the Project

Open the notebook:

```text
project_starter.ipynb
```

Then run the cells from top to bottom.

The main success checkpoint is the itinerary generation cell printing:

```text
✅ Initial itinerary generated successfully. Congratulations!
```

The later cells evaluate and revise the plan until a final itinerary is produced.

---

## Key Files Explained

| File | Purpose |
|---|---|
| `project_starter.ipynb` | Main Udacity notebook containing the completed project workflow |
| `project_lib.py` | Shared helper code, mocked APIs, chat-agent utilities, and display helpers |
| `requirements.in` | Minimal direct dependency list |
| `requirements.txt` | Full dependency lock/output used for reproducible setup |
| `.gitignore` | Keeps secrets, logs, virtual environments, and generated submission files out of git |

---

## Notes

- The city, weather, and activities are fictional/mock data from the Udacity project.
- API credentials are intentionally not included in this repository.
- Notebook outputs are included because this is a notebook-based Udacity submission project.
- Generated submission zip files and internal review logs are intentionally excluded from version control.
