# TripMate AI

A sleek AI-powered travel planner that turns a simple natural-language request into a structured trip experience. TripMate AI combines live flight data, hotel research, and LLM-generated itineraries into one polished web experience built with FastAPI and LangGraph.

![TripMate AI](https://img.shields.io/badge/Python-3.10%2B-blue) ![FastAPI](https://img.shields.io/badge/FastAPI-0.136.3-009688) ![LangGraph](https://img.shields.io/badge/LangGraph-1.2.2-6A5ACD)

## ✨ What TripMate AI Does

TripMate AI helps users plan trips by:

- understanding a travel request in plain English
- fetching live flight information from AviationStack
- searching hotel and travel suggestions using Tavily
- generating a practical day-by-day itinerary with Groq LLMs
- presenting everything through a clean web interface

## 🚀 Features

- Natural-language travel planning
- Multi-agent workflow powered by LangGraph
- Live flight data lookup
- Hotel discovery through web search
- Beautiful AI-generated travel summaries
- Persistent conversation/thread support
- FastAPI-powered REST API and frontend

## 🧠 Architecture Overview

The project follows a simple multi-agent design:

1. Flight agent fetches flight-related data
2. Hotel agent gathers hotel and destination insights
3. Itinerary agent builds a travel plan
4. Final agent formats everything into a polished response

This orchestration is handled by LangGraph and exposed through a FastAPI application.

## 🛠️ Tech Stack

- Python 3.10+
- FastAPI for the web API
- Jinja2 templates for the frontend UI
- LangGraph for the multi-agent workflow
- LangChain + Groq for intelligent itinerary generation
- Tavily API for hotel and travel search
- AviationStack API for live flight data
- PostgreSQL with LangGraph checkpointing

## 📁 Project Structure

- app.py — FastAPI application entry point
- backend.py — LangGraph travel planning workflow and agent orchestration
- tools/flight_tool.py — flight parsing and AviationStack integration
- tools/tavily_tool.py — Tavily-based hotel/travel search
- templates/ — HTML frontend templates
- static/ — CSS and JavaScript assets
- requirements.txt — Python dependencies

## ⚙️ Environment Variables

Create a .env file in the project root with the following values:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
AVIATIONSTACK_API_KEY=your_aviationstack_api_key
DATABASE_URL=your_postgresql_connection_string
DEFAULT_ORIGIN_IATA=HYD
```

## ▶️ Getting Started

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run the application

```bash
python app.py
```

Then open:

```text
http://127.0.0.1:8000
```

## 🧪 Example Usage

Try prompts such as:

- Plan a 5-day trip to Japan from Bangladesh
- Find flights to Singapore for a weekend getaway
- Create a budget-friendly itinerary for Dubai
- Suggest hotels and activities for a 7-day Europe trip

## 🔗 API Endpoint

The app exposes a travel planning endpoint:

- POST /api/travel

Example request body:

```json
{
  "message": "Plan a 4-day trip to Paris",
  "thread_id": null
}
```

## ✅ Notes

- Flight pricing is not guaranteed to be available through the current live-flight integration.
- The application is designed for travel planning assistance rather than direct booking.
- Make sure your API keys and database connection are correctly configured before running the app.

## 📌 Future Improvements

- add user authentication
- support hotel booking integration
- add itinerary export to PDF or calendar
- improve multi-destination trip planning
- enhance frontend experience with richer visuals

## 👤 Author

Built as an AI travel assistant project focused on intelligent trip planning and modern web experiences.
