**Interview Snapshot — Genetic & Clinical Cancer Researcher**

**Who:** Researcher at a Cancer Lab (specializing in Structural Variants and Clinical Correlation)

**Problem confirmed:** Yes. Severe friction in data extraction (EMR), lack of trust in AI for "exploratory" logic, and a high manual burden for data cleaning and learning new languages.

**Key quotes:**
- "Gathering from Epic... would be great if they had an automatic version of that that actually functioned. It was a nightmare."
- "I wrote it all up by myself because I wanted to learn R. That was a very specific decision I made."
- "I’m not sure I’d trust [AI] for [exploration]... I found that it didn't always think through problems the way I would."
- "We found that it would get stuck in these loops... if we just looked at what it was outputting, we could figure out what was wrong and [the AI] wouldn't be able to do that."

**Emotional intensity:**
- High (7/8) regarding the frustration with Epic and Electronic Medical Records (EMR).
- Medium (5/8) regarding the "distrust" of AI's reasoning capabilities—the user feels more competent than the model for high-level thinking.
- Low (2/8) regarding the difficulty of the stats/plotting; she views Kaplan-Meier curves and basic R scripts as "straightforward."

**Current solution:**
- A manual, multi-step process. Clinical data is extracted by hand from Epic and stored in Google Sheets. Genetic data (structural variants) is stored locally on her computer.
- Analysis is performed using R, specifically for linking datasets and generating Kaplan-Meier survival curves to find patient stratifications.

**Money spent:** No specific software costs mentioned; uses open-source tools (R) and university-provided cloud storage (Terra). However, the "time-cost" of manual EMR extraction and self-teaching R is significant.

**Reaction + Commitments**

**Solution reaction:** Skeptical but curious. She would value automation for "starter code" (filtering, basic plotting) and data extraction, but strongly rejects the idea of AI leading the exploration phase of research.

**Biggest concerns:**
- Analytical Integrity: AI is perceived as "bad at exploratory thinking" in unstudied fields. She believes human intuition is required to find signals where none are expected.
- Logic Loops: AI tends to hallucinate or get stuck when debugging complex architectures (like her ML class project).
- Data Security/Scale: Her research involves high-volume genetic data that may be "too massive" or sensitive for standard chat-based AI uploads.

**Surprises/Contradiction of assumptions:**
- Intentional Difficulty: Unlike the other users, she chose the hard way (no AI) specifically to gain the skill of coding in R. Automation would have been a "detriment" to her educational goal.
- The "Epic" Bottleneck: The primary pain point isn't the analysis—it's the "upstream" mess of getting data out of hospital software.
- Human > Machine for Signal: She views AI as a tool for execution (writing the code she tells it to write), not for discovery (telling her what to look for).
