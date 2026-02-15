# Enhancing Cybersecurity Tabletop Exercises with Advanced Prompt Engineering

## I. Foundations of Cybersecurity Tabletop Exercises (TTX)
Cybersecurity tabletop exercises are structured, discussion-based practice sessions designed to prepare organizations for high-impact security incidents. Unlike routine incident response, a TTX focuses on the "ocean of things" that span across technical, legal, and communication silos.

### A. The Critical Role of Practice
- **Skill Refinement**: Individual technical skills must be supplemented by team-wide coordination.
- **Coordination Dynamics**: Learning to manage unexpected scenarios and logistics across diverse departments (Legal, PR, IT).
- **Stress-Free Exploration**: Providing a safe space to identify gaps in preparation without the pressure of a live breach.

### B. Core Frameworks and Definitions
- **NIST SP 800-84**: Defines TTXs as classroom or breakout sessions where personnel discuss roles and responses to IT emergencies.
- **CISA Framework**: Describes TTXs as facilitated discussions of scripted scenarios based on current policies and procedures.
- **The Role-Playing Metaphor**: A TTX functions similarly to a tabletop RPG, where participants (players) navigate a story (scenario) managed by a "game master" (facilitator).

---

## II. Strategic Application of Generative AI in TTX
Generative AI addresses traditional resource barriers—cost, time, and "internal blind spots"—by automating scenario creation and simulating interactive roles.

### A. Narrative and Simulation Capabilities
- **Simulated Realism**: AI can "dream up" consistent technical environments, such as a compromised Linux terminal, generating realistic command outputs and ransom notes.
- **Hallucinated Consistency**: The AI maintains internal logic, ensuring that scenario clues (like a web server breach) align with simulated file systems and process lists.

### B. Accelerating the Planning Timeline
- **Traditional Timeline**: Standard CISA guidance can require up to 5.5 months of planning, from initial concept meetings to post-exercise reports.
- **AI Compression**: Generative models can compress these phases by instantly generating situation manuals, facilitator handbooks, and injects.

---

## III. Prompt Engineering Patterns for Exercise Design
Leveraging specific "patterns" allows facilitators to program Large Language Models (LLMs) to act as sophisticated partners in the exercise lifecycle.

### A. The Flipped Interaction Pattern
- **Intent**: Reverses the interaction dynamic so the LLM asks the questions to achieve a specific goal.
- **Structure**:
  1. **Instruction**: "Ask me questions about [topic]."
  2. **Condition**: "Until you have enough information to [goal]."
  3. **Cadence**: "Ask the questions one at a time."
- **Application**: Allows the AI to gather organizational context (e.g., specific departments involved) before generating a customized, high-fidelity scenario.

### B. The Persona Pattern
- **Intent**: Instructs the LLM to adopt a specific role to influence output perspective and detail.
- **Simulation Examples**:
  - **Linux Terminal**: Simulates a hacked environment responding to bash commands.
  - **The Plumber/Consultant**: Acts as an external entity during a phone-call inject.
  - **Security Reviewer**: Provides critical technical feedback on incident response choices.

### C. The Outline Expansion Pattern
- **Intent**: Overcomes LLM token limits (typically ~1,000 tokens per response) to build complex, multi-page exercises.
- **Process**:
  1. **Initial Outline**: Generate a high-level 5-phase scenario.
  2. **Sub-item Selection**: Choose a single phase or decision point.
  3. **Iterative Deepening**: Ask the AI to expand that specific point with "pros/cons," "specific constraints," and "probing questions."
- **Result**: Transforms a one-page summary into a comprehensive workbook with specific institutional nuances.

---

## IV. Practical Scenarios and Risk Mitigation
Exercises should focus on the "High Impact, High Likelihood" quadrant of the risk matrix.

### A. Technical and Administrative Injects
- **Identity Hijack**: A Google Workspace account takeover that tests downstream service availability and contact lists.
- **Data Center Exfiltration**: Zero-day malware scenarios that force decisions on internet isolation vs. evidence preservation.
- **Vendor "Friendly Fire"**: A catastrophic update from an EDR/XDR vendor that bricks the Windows fleet, testing business continuity and BitLocker recovery plans.

### B. Post-Exercise Evaluation
- **After-Action Reports (AAR)**: Identifying process deficiencies and assigning remediation tasks within 3-4 weeks.
- **The Cognitive Verifier**: Using AI to suggest sub-questions during evaluation to determine if decision thresholds were actually documented and understood.
