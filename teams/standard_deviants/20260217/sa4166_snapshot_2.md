**Interview Snapshot**

**Who:** Researcher/Sole Data Analyst at USC Brain and Music Lab

**Problem confirmed:** 
Yes. High technical debt, manual "Band-Aid" workflows, and communication barriers between the analyst and non-technical stakeholders.

**Key quotes:**
"I’m the only person on earth who knows what to do just because I’ve done it. So the workflow sucks."
"Every time there’s a new batch of data... I have to wipe everything... move it into the correct folder... move it into the correct folder... and this and run this code."
"I’d be very nervous about telling [my bosses] that I just let AI handle it 'cause they'd be like, 'Why did you do it that way?'"
"It was actually two different T-tests... that was more like a communication issue."

**Emotional intensity:** 
* High (7/8) regarding the frustration of "tedious" manual file management and the pressure of explainability.
* Low (2/8) regarding the intimidation of the math itself (since he is the expert), but high regarding the consequences of messy code.

**Current solution:** A hybrid, fragmented system using MATLAB and Python. Data is collected via Qualtrics and manually moved through a series of folders. Analysis involves pixel-wise T-tests and Linear Discriminant Analysis (LDA).
"Version control" is essentially Christopher’s memory, leading to "unwieldy" scripts that require running multiple times to work correctly.

**Money spent:** Currently covered by university/lab funding for standard tools (MATLAB). There is a high "time-cost" due to the lack of integration, but a high barrier to entry for new platforms unless they integrate with GitHub.

**Reaction + Commitments**
**Solution reaction:** Christopher was tentatively positive. He valued the idea of a "centralized" system that could visualize the workflow and automate the tedious "cleaning" steps (like outlier removal based on standard deviations).

**Biggest concerns:** 
1. Rigorous Transparency: In academic research, "black box" AI is a dealbreaker. He needs to see the underlying code/logic to justify the results to his PI (Principal Investigator). 
2. Integration: To be worth the switch, the tool cannot be another "silo." It must talk to his existing codebase in Python or MATLAB. 
3. Reproducibility: The tool must be able to handle "stepwise" changes that others in the lab can follow.

**Surprises/Contradiction of assumptions:**
1. The "Lazy" Expert: Even highly skilled analysts are prone to "lazy" manual fixes under time pressure, creating a "house of cards" workflow that they eventually fear to touch.
2. The Communication Gap: The pain point isn't just "doing the math"; it’s the social labor of explaining Eigenvectors or PCA to partners who haven't taken linear algebra.
3. Integration > Intelligence: For an expert, the most attractive feature isn't "doing the analysis for me," but rather "managing the files and folders for me."

