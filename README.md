main.py — the API server. This is what answers requests like "save this interaction" or "chat with the assistant."
agent.py — the AI brain. Uses LangGraph + Groq to understand what you typed and decide which action to take (log a visit, edit one, search, etc.)
database.py — defines how interactions are stored (like a spreadsheet structure, but in a real database)
schemas.py — defines what data is allowed in/out (e.g. an interaction must have an HCP name and date)
requirements.txt — list of Python libraries needed to run it
.env.example — where your Groq API key goes
frontend/ (what you see on screen)
src/App.jsx — the main screen, with the toggle between "form" and "chat"
src/components/StructuredForm.jsx — the fill-in-the-blanks form
src/components/ChatPanel.jsx — the chat box that talks to the AI
src/components/InteractionList.jsx — shows past logged visits
src/redux/ — where the app's data is stored while you use it (what's typed in the form, chat history)
src/api/client.js — connects the frontend to the backend
