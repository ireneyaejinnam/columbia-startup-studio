Interview with Christopher, CS Major at Columbia, Researcher at USC Brain and Music Lab

Speaker 1: Hello, Christopher. Do you do any kind of data analysis?
Speaker 2: Uh, yeah, I do. I’m involved in a lab at USC—the Brain and Music Lab. It’s about emotion stuff; the studies are on nostalgia. I’m actually the only person who does the coding and statistics.
Speaker 1: What kind of analysis are you doing?
Speaker 2: I work on XY pixel data. People submit bodily sensation maps—they basically draw where they feel things. The main analysis I’ve done includes pixel-wise T-tests to get thresholds and P-values, some regressions, and some LDA (Linear Discriminant Analysis) training. There’s also masking and filtering to get the "junk" data out.
Speaker 1: As the only person doing this, would you find it helpful if there was software where you didn’t have to "coach it up" all the time? You could upload a CSV, it would suggest ways to clean the data without ruining the original file, and it could run general statistical analyses for you—T-tests, correlations—without you having to code them?
Speaker 2: I’d say tentatively yes. For example, excluding users who are three standard deviations away from the average—like people who wrote nothing or scribbled everywhere—is straightforward. But a big part of my stress is explaining the analysis to my bosses. I’d be nervous telling them, "I just let AI handle it," because they’d ask why I did it that way.
Speaker 1: Would it help if you had a history of every analysis you did, including what it means and an explanation for your specific data?
Speaker 2: Yeah, I could see that being helpful—suggesting what type of analysis to do to get started. But for rigorous research, I’d still prefer something like MATLAB where I can see the code and exactly what it’s doing.
Speaker 1: What if the platform used a "drag and drop" format, almost like Scratch, but performed MATLAB-style functions? Would that be more intuitive?
Speaker 2: Intuitive, probably not. But the current workflow sucks because the projects are about to be wrapped up and it’s so unwieldy. I’m the only person on earth who knows what to do just because I’ve done it. Being able to visualize the workflow would probably help.
Speaker 1: What makes it unwieldy?
Speaker 2: Mostly because I’m lazy! [Laughs]. If we have a meeting in two hours, I’ll put a temporary "Band-Aid" fix on the code. It works, but I don’t go back and make it better. Right now, to process a new set of data, I have to run it four times because the first time it renames one group, the second time it re-evaluates... I should have just written a for-loop. Having a centralized thing would help.
Speaker 1: If you could upload data, see the cleaning steps in a stepwise manner, and have it be reproducible because it’s in plain language, would that be helpful for your partner in the lab?
Speaker 2: Absolutely. I often have to explain the analysis to my partner, and sometimes he doesn't get it quite right. For instance, explaining PCA (Principal Component Analysis)—I don’t think he’s taken Linear Algebra, so he doesn't necessarily know what Eigenvectors are.
Speaker 1: Besides explainability, what are your other pain points?
Speaker 2: At the beginning, there was confusion about the type of T-test. I thought it was population vs. population, but it was supposed to be a pixel-wise T-test—one against zero and one pairwise. That was a communication issue. Once I understood it, I could have coded it or used ChatGPT, but the communication was the biggest hurdle.
Speaker 1: How would a shared online space help with that?
Speaker 2: Visualizing the flow would be nice, but being able to look at the CSVs together would be huge. Right now, there are a lot of CSVs being thrown around and it’s a pain in the ass. Half my workflow is in MATLAB, half is in Python. Every time there’s a new batch of data, I have to download it from Qualtrics, move it to the right folder, run code, get output, move it again... integration would have been very helpful.
Speaker 1: What do you usually ask ChatGPT to do?
Speaker 2: At the start, "What is the difference between a pairwise T-test and a T-test against zero?" Later on, it’s "This code isn’t working, help me." Also, fixing indices is annoying. We divided data by country, and moving from the entire group to a per-country thing is tedious. I’ll just ask ChatGPT to write a helper function for that.
Speaker 1: If ChatGPT is already streamlined, what would a separate platform need to offer?
Speaker 2: I don't know. The only reason I use MATLAB is because the guy before me used it. If a new platform was integrated with GitHub, MATLAB, and Python so it knew what had already been done to the data, that might be worth it.
