# SLOTH
its a working name. the aim is to create customized SLMs for schools and universities such that the notes that the professors have collected would be used as an input to create visualizations, short videos, quizzes, flashcards etc. the Catch is that unlike the other AI, this would be customized to a particular university/school


 1: Scoping & The "One-Input" PipelineThe Goal: Define strict limits and get raw text into the AI.Action Items:Restrict the input: Decide that for the MVP, professors can only upload PDFs or TXT files. (Skip PPTs and handwritten notes for now).Set up the environment: Initialize your GitHub repository, backend, and database.Build the Parser: Write a script that extracts text from a professor's uploaded PDF and chunks it into digestible pieces.
 
 2: Core AI Engine (The "Customized" Logic)The Goal: Make the AI behave like it belongs to a specific school.Action Items:Implement RAG (Retrieval-Augmented Generation): Store the chunked notes in your vector database. When a student asks a question, the system must only pull answers from that specific professor's notes.System Prompting: Guardrail the LLM. Example: "You are an AI teaching assistant for [University Name], specifically for [Course Name]. Use only the provided context. If the answer is not in the professor's notes, politely state that it isn't covered in the curriculum.
 
 
  3: Output Generation (Flashcards & Quizzes)The Goal: Turn text into interactive study materials.Action Items:Structured JSON Outputs: Use OpenAI's structured outputs or instructor libraries to force the AI to return data in exact formats.Example: Prompt it to generate an array of flashcards: [{ "front": "Question", "back": "Answer" }].Quiz Generation: Do the same for multiple-choice questions.
  
  
 4: The "Visual Learning" EngineThe Goal: Bring in the visualizations (this is the hardest part, so keep it lean).Action Items:Diagrams via Code: Do not try to generate actual images or videos yet (AI image generation is slow, expensive, and often inaccurate for complex school topics). Instead, prompt the AI to generate Mermaid.js or Python Matplotlib code representing flowcharts, mind maps, or timelines.Frontend Render: Have your frontend render that Mermaid code into a beautiful visual diagram instantly.
 
 
 5: Frontend Integration & UIThe Goal: Connect the backend AI engine to a clean dashboard.Action Items:Professor View: A dead-simple page with a drag-and-drop file uploader and a "Generate Platform" button.Student View: A clean dashboard showing the generated study modules: a Flashcard tab, a Quiz tab, a Diagram tab, and a chat sidebar to talk to the course material.
 
 
6: Testing, Refinement & PresentationThe Goal: Squash bugs, load real university data, and prep the demo.Action Items:Get Real Data: Take a single syllabus and 3 chapters of actual notes from a professor. Dump them into the system.Polish the Demo: Fix UI quirks. Ensure the visual diagrams load correctly.The Pitch: Record a 3-minute video showing the transition from Raw PDF $\rightarrow$ Interactive School-Branded Study Suite. This is the "actual result" that locks in your extension.
