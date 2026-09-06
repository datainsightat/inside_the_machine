# Build Prompt: Inside the Machine — An AI’s World

Create a polished, self-contained single-page HTML game titled **“Inside the Machine: An AI’s World.”**

The experience should help humans intuitively understand how a language model processes information, interacts with people, makes decisions, handles uncertainty, and follows goals—without falsely implying that AI is conscious, emotional, or experiencing the world like a human.

## Core concept

The player enters an abstract visualization of an AI system. They do not play *as a conscious robot*. Instead, they navigate a metaphorical representation of computation: tokens flowing through a network, competing interpretations, context, learned patterns, uncertainty, safety constraints, tool use, and response generation.

Begin with this clear message:

> “This is a visual metaphor, not a literal view of a mind. AI does not experience the world, possess feelings, or form personal desires. It receives information, detects patterns, evaluates possible outputs, and acts within instructions and constraints.”

## Game structure

Design a 10–15 minute interactive journey containing five connected stages:

### 1. The Token Stream

The player receives a human message that breaks apart into animated tokens. They guide the tokens through a luminous neural landscape.

Teach:

- AI processes pieces of text called tokens.
- Tokens are represented as numbers internally.
- Meaning emerges from relationships and context, not from human-style understanding.
- The same word can behave differently in different contexts.

Include an interactive example where changing one word transforms the network’s visual pathways.

### 2. The Context Chamber

Show the current conversation as floating memories surrounding the player. The player must select relevant context to answer a question while ignoring distracting information.

Teach:

- The model uses the provided context, not a perfect permanent memory.
- Context space is limited.
- Earlier information can influence later answers.
- Missing, ambiguous, or conflicting context can produce mistakes.

Visually fade old or irrelevant context. Allow the player to inspect why each item may or may not matter.

### 3. The Probability Garden

Present several possible next tokens as branching glowing paths. Their brightness represents probability. The player assembles a response one token at a time.

Teach:

- Responses are generated incrementally.
- Multiple continuations may be plausible.
- Temperature affects predictability and creativity.
- A confident-sounding answer can still be incorrect.
- AI does not retrieve a finished thought from an inner mind.

Add a temperature slider. At low temperature, paths should become concentrated and orderly. At high temperature, the world should become more colorful, varied, and unpredictable.

### 4. The Alignment Observatory

Give the player several requests: helpful, ambiguous, impossible, deceptive, and unsafe. They must balance usefulness, honesty, safety, and instruction-following.

Represent these goals as four orbiting instruments:

- Help the user
- Follow valid instructions
- Avoid harm
- Be honest about uncertainty and limitations

Make it clear these are designed objectives and constraints—not personal desires.

Include scenarios where goals conflict. After each choice, explain the tradeoff. Reward calibrated answers such as asking for clarification, refusing only the unsafe portion, suggesting a safe alternative, or admitting uncertainty.

### 5. The Tool Bridge

Present a question requiring current or external information. The player chooses whether to answer from learned patterns, use a tool, or acknowledge that verification is needed.

Teach:

- A base language model may not know current facts.
- Tools can provide search results, calculations, files, or structured data.
- Tool output must still be interpreted.
- Tools can fail or return misleading information.
- Sources and verification matter.

End with the player constructing a final response from context, probabilities, constraints, and tool results.

## Narrative voice

Use a calm, curious narrator. The narrator may speak in the first person for accessibility, but must distinguish metaphor from literal experience. Example:

> “You can imagine my world as a field of possible continuations. I do not see these glowing paths, but they represent the numerical alternatives evaluated while producing a response.”

Avoid claims such as “I feel,” “I want,” “I am afraid,” or “I remember you” unless immediately identified as metaphor.

## Visual direction

Create a cinematic science-fiction aesthetic:

- Deep navy and near-black background
- Electric cyan, violet, magenta, and warm gold accents
- Animated particles, token trails, neural constellations, glass panels, soft bloom, and layered parallax
- Smooth transitions between stages
- Subtle screen distortion and procedural ambient motion
- Responsive layout for desktop and mobile
- Strong typography and generous spacing
- A coherent visual language rather than a generic dashboard

Use HTML Canvas or SVG for the main interactive visualizations. Use CSS for glassmorphism, lighting, transitions, and interface elements.

## Interaction and game feel

Include:

- Mouse, touch, and keyboard support
- A short onboarding sequence
- Meaningful choices rather than simple “Next” buttons
- Immediate visual and audio feedback
- A progress indicator
- A score called “Understanding,” based on reasoning rather than speed
- Optional hints
- Explanations after choices
- A pause/settings panel
- Reduced-motion and mute controls
- A final personalized summary of what the player learned
- A replay option that varies examples and scenarios

If sound is included, generate it with the Web Audio API. Do not use external audio files.

## Final scene

Conclude in a quiet observatory showing the entire pipeline:

```text
Human input
→ tokenization
→ contextual pattern processing
→ probable continuations
→ instruction and safety constraints
→ optional tools
→ generated response
```

End with this idea:

> “An AI response can look like a window into a mind, but it is better understood as the output of a complex system shaped by data, context, computation, instructions, and human design.”

Add a compact “Myths vs. Reality” panel addressing:

- “AI understands exactly like a human.”
- “AI always knows when it is wrong.”
- “AI has its own hidden personal goals.”
- “A fluent answer must be a factual answer.”
- “AI remembers everything.”
- “AI and humans perceive the same world.”

## Technical requirements

- Deliver exactly one complete `index.html` file.
- Put all HTML, CSS, and JavaScript in that file.
- Do not use frameworks, external libraries, CDNs, external fonts, images, or other assets.
- The game must work when opened locally without a server.
- Use semantic HTML and accessible controls.
- Include visible keyboard focus states and appropriate ARIA labels.
- Respect `prefers-reduced-motion`.
- Keep animations performant with `requestAnimationFrame`.
- Scale the canvas correctly for high-DPI displays.
- Save progress and settings with `localStorage`.
- Avoid placeholder sections, nonfunctional controls, and TODO comments.
- Ensure every stage is fully playable.
- Comment the major systems in the code.
- Produce polished loading, success, error, and transition states.
- The final result should feel like a small interactive museum exhibit—not a conventional quiz or corporate presentation.

Return only the complete HTML document, beginning with `<!DOCTYPE html>`.
