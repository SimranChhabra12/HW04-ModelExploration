# HW04-ModelExploration
Model Exploration 
ntroduction

Assignment 4 explores the creative capabilities of the GPT-2 model by developing a prompt-to-song generation system. GPT-2 is a transformer-based language model developed by OpenAI that is adept at generating coherent and contextually relevant text. In this assignment, the model is used to transform prompts—describing moods, scenarios, or stories—into complete sets of song lyrics. The goal is to harness GPT-2’s potential for creative expression and to investigate its performance in generating artistic content.

Use Case:
Personalized Songwriting Assistant for Emotional Expression

What?

I'm building a tool that takes a detailed text prompt and turns it into a draft of song lyrics. The goal is to help overcome writer’s block by providing a starting point with a clear structure—like having separate "Verse:", "Chorus:", and "Bridge:" sections. For example, a user could enter a prompt about urban isolation and beauty, and the tool would generate lyrics that not only describe that scene but also include a catchy chorus.

Why?

Creative Brainstorming: If you're a songwriter or musician struggling for inspiration, this tool can give you a structured draft to build on.

Personal Expression: It lets you convert your feelings and experiences into lyrics, even if the first draft isn’t perfect.

Content Creation: Indie artists or content creators can quickly generate raw lyric ideas to later refine into polished songs.

How It Works:

Input:

I provide a detailed prompt—something like:

"Write a song about a person walking through a city at night, feeling both the isolation and beauty of urban life."

Structure Enforcement:

The prompt includes clear, explicit instructions:

"Use this format exactly:

Verse: [Describe the scene/emotion]

Chorus: [Write a catchy chorus]

Bridge: [Add a twist or deeper insight]"

Output:

GPT‑2 then generates a draft based on the prompt. It’s supposed to stick to the structure, but here's where it gets tricky.

Does It Work?

Even though GPT‑2 always churns out something, it’s not really built for songwriting. More often than not, I end up with text that reads like a narrative or a generic story instead of a neatly formatted song. The model frequently:

Mixes up or omits the section labels.

Produces extra, irrelevant text that throws off the structure.

Sometimes does a decent job, but it's hit or miss—meaning I often have to run it several times or tweak it further to get something usable.

The Upside and the Challenge:

Upside: It can rapidly generate creative drafts that give me a spark of inspiration or a base to work from.

Challenge: The model's inconsistency and tendency to deviate from the desired format means I have to do a lot of manual editing. It really highlights both the potential of these generative models and where they still need improvement for niche tasks like songwriting.

Methodology

I used Hugging Face’s transformers library in a Colab notebook. First, I loaded up GPT-2 with the text-generation pipeline.

Tweaking the Prompts:
At first, I was getting story-like outputs, not song lyrics. I realized I needed to be more specific. So, I adjusted the prompts to include cues like "Verse:", "Chorus:", and even "Bridge:" to push the model towards a song format.

Some changes I made:
1. I increased the max_length to 200 so the model has more room to develop the song.

2. I set the temperature to 0.8 for a nice balance between creativity and sticking to the topic.

3. The prompts now clearly ask for song sections like "Verse:" and "Chorus:", which guides the model to format its output like a song.

Results and What I Learned:

With the refined prompts, the outputs started to look more like actual song lyrics rather than just stories. Here’s what I noticed:

Relevance and Coherence: The generated lyrics match the theme of the prompts pretty well.

Structure: By adding section labels, the text now has a song-like feel, which makes it easier to imagine these as actual lyrics.

Creativity: The lyrics are creative and include some interesting imagery. However, sometimes the model repeats itself or goes off track, so there’s room for improvement.

User Perspective: Testing different prompts helped me see that clearer, more detailed instructions lead to better results.

Conclusion

This project was a great way to experiment with GPT-2’s creative potential. By tweaking the prompts to include explicit song structure cues, I was able to steer the model away from generic narrative text and closer to what you’d expect from a song. It’s not perfect, but it definitely shows how powerful prompt engineering can be when working with language models. In the future, fine-tuning the model on actual song lyrics might help reduce repetitive or off-topic outputs even further.
