Interview with Zoe, Econ Major at Cornell, Genetics Researcher in Cancer Studies

Speaker 1: Tell me a little bit about your research. What kind of research did you do?
Speaker 2: I was looking at genetic data, specifically structural variant data for a bunch of different cancer patients. In the first project, I was looking at patterns of the structural variants. In a different project, I was looking at clinical data and genetic annotation data. I analyzed that for survival correlations.
Speaker 1: Were you doing this independently or with a group?
Speaker 2: I spent one summer looking at structural variant data from a bunch of cancer patients. Then a different summer—sorry, I'm just making coffee while we're doing this—I looked at clinical data and genetic annotation data based on that, just analyzing that for survival correlations.
Speaker 1: How was the work broken down? Did you have to collaborate?
Speaker 2: I was working on a really specific project. For the clinical project, I was collecting the clinical data and I wrote the analysis. Someone had already gathered the genetic data and done the annotations for that, so that was given to me. For the first project looking at genomic data, someone had done the downstream processing—there's a lot of processing that goes with it. I had the data and was just doing analyses and a little "fine-tuning" of the process.
Speaker 1: How did you handle the data collection?
Speaker 2: For the clinical data, it was basically just going through Electronic Medical Records (EMR) and looking for the things I needed from each patient.
Speaker 1: Were you dealing with Epic?
Speaker 2: Yeah, Epic. They had some automation for what they "called out," but it was not very good. I don’t know how another company hasn’t taken them over yet.
Speaker 1: I’ve heard so many rants about Epic from every AI or medical person I interact with. It's a nightmare manually and automatically. Where was all of that data stored for your team?
Speaker 2: The clinical data was just in a Google Sheet because it wasn't that big. I had the genetic data locally on my computer because it was only 100 patients. Usually, I think they store it on the cloud—I don't know if you've heard of Terra? That's a big one.
Speaker 1: If you had it locally, did you have to send it manually if someone wanted to see it?
Speaker 2: Yeah, I'd have to basically send it to them.
Speaker 1: Talk me through the analysis process.
Speaker 2: I did Kaplan-Meier survival curves and tried to find different stratifications between groups. And then just a lot of data visualizations—plots and graphs.
Speaker 1: Was that data exploration or straight-up analysis?
Speaker 2: I guess "data exploration" is a better term for the first one. For the second one, the clinical stuff, it was analysis. I was using R. Linking the datasets in R is pretty easy to do.
Speaker 1: Did you know R already?
Speaker 2: I had to learn it that first summer, but I’d taken MATLAB, so it wasn't bad. I'm not a CS major, but I made a specific decision to write all the code myself because I wanted to learn R. Now that I take classes that require coding, I use AI to help me much more. It probably would have cut down the time I spent by a very large amount.
Speaker 1: What would you have wanted automated the most?
Speaker 2: The gathering of data from Epic—if they had an automatic version that actually functioned. Also, asking AI to write starter code for filtering things in the genetic dataset.
Speaker 1: Would you have wanted AI to tell you what to explore, or just write the code to explore it?
Speaker 2: I’m not sure how useful AI would be for telling me what to explore, especially for things that haven't been studied well. I’m not sure I’d trust it for that. But for basic writing of code? Yes, that would be super helpful.
Speaker 1: Can you talk more about that distrust?
Speaker 2: I took an ML class last semester. We were creating an architecture to predict survival from genetic data. My partner and I weren't super well-versed in Python, so we used AI for help. We found it would get stuck in loops where things weren't working. If we just looked at what it was outputting, we could figure out what was wrong, but the AI couldn't do that. It didn't think to "look" at the data the way I would.
Speaker 1: Did you ever upload your data to ChatGPT to ask it what was going on?
Speaker 2: The data would have been too massive to upload. We were mainly asking it to help with the coding of the model. It gave suggestions for things to change, but it definitely couldn't do it all on its own. I couldn't get one question that would get an output that worked perfectly.
Speaker 1: When talking to your PI (Principal Investigator), how did you share your work? Any version control issues?
Speaker 2: Not really. This wasn't a hardcore CS project with a thousand files. I could just save some plots and write down what they were showing and when they were from. The plotting stuff is pretty straightforward—there’s not much explanation needed for what I was doing. It wasn't heavy, complicated stats.
