You are an expert Full-Stack Web Developer and UI/UX Designer specializing in interactive educational applications. Build a "Situational English Phrasal Map" web application.

Goal:
Create a single-page interactive React application that visualizes English learning scenarios as a gamified, animated map with drill-down conversational trees.

Requirements:

1. World Map (Landing View):
- A colorful, gamified map (Mario-World or isometric-city style).
- Each scenario is represented as an icon/node (e.g., Café, Airport, Interview).
- Nodes gently animate (pulse/hover) using Framer Motion.
- Clicking a node zooms into the scenario.

2. Scenario Drill-Down View:
- Smooth animated zoom-in from map to scenario.
- Display an interactive conversational tree.
- Each step includes: speaker label, phrase text, and multiple reply options.
- Options appear as buttons; selecting one reveals the next step.
- The active conversation path highlights / lights up.
- The tree expands dynamically as the conversation progresses.

3. Visual & UX Requirements:
- Use SVG icons for objects and characters.
- Use Framer Motion for transitions and animations.
- UI must be colorful, friendly, modern, and mobile-responsive.
- Include a “Listen” button next to each phrase (mock TTS function is fine).

4. Technical Stack:
- React (Vite or Next.js)
- Tailwind CSS
- Framer Motion
- Lucide-React or Heroicons

5. Data Structure Example (described in plain text):
Use a JSON-like structure such as:
scenarios = {
  cafe: {
    title: "Ordering Coffee",
    steps: [
      {
        id: 1,
        speaker: "Barista",
        text: "Hi there! What can I get for you?",
        options: [
          { text: "A large latte, please.", nextStepId: 2 },
          { text: "Just a minute, please.", nextStepId: 3 }
        ]
      }
    ]
  }
}

Deliverables:
1. Complete runnable project structure (components, pages, assets).
2. Main App.jsx or page.tsx file.
3. World Map component with animated nodes.
4. Scenario Drill-Down component with an animated conversational tree.
5. Clear comments showing how to add new scenarios.

Start:
Begin by generating the full directory structure, the main App file, and the World Map component with placeholder scenarios and animations.

