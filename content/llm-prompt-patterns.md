# LLM Prompt Engineering Patterns

A Concise Pattern Reference Guide 

---

Persona Pattern 

**Act as a specific role and perform a task.** Instructs the LLM to adopt a particular persona or expertise to approach your request from that perspective. 

> 
> **Template:** 
> Act as a [PERSONA].
> Perform this task: [TASK].
> 
> 

**Example:** Act as a gourmet chef. I will tell you what I'm eating, and you will tell me about my eating choices. 

---

Audience Persona Pattern 

**Explain information to a specific type of person.** Tailors explanations to match the background, knowledge level, or perspective of a target audience. 

> 
> **Template:** 
> Explain [TOPIC] to me.
> Assume that I am [AUDIENCE].
> 
> 

**Example:** Explain large language models to me. Assume that I am a bird. 

---

Question Refinement Pattern 

**Improve questions before answering them.** Prompts the LLM to suggest better, more precise versions of your question before providing an answer. 

> 
> **Template:** 
> From now on, whenever I ask a question, suggest a better version of the question to use instead. Prompt me if I would like to use the better version instead.
> 
> 

**Example:** Whenever I ask a question about who is the greatest of all time (GOAT), suggest a better version that puts multiple players' unique accomplishments into perspective. 

---

Cognitive Verifier Pattern 

**Break complex questions into component questions.** Decomposes complex questions into simpler clarifying questions, then combines the answers into a comprehensive response. 

> 
> **Template:** 
> When you are asked [TASK], follow these rules:
> Generate additional questions about [TOPIC].
> Combine the answers to these questions to produce [OUTCOME].
> 
> 

**Example:** When you are asked to plan a trip, generate questions about my budget, preferred activities, and transportation. Combine answers to better plan my itinerary. 

---

Flipped Interaction Pattern 

**Ask me questions instead of answering directly.** Reverses the dynamic so the LLM asks you clarifying questions to better understand your needs before providing answers. 

> 
> **Template:** 
> I would like you to ask me questions to achieve [GOAL]. You should ask questions until [STOPPING CONDITION]. Ask me the first question.
> 
> 

**Example:** Ask me questions to help diagnose a problem with my Internet. Ask questions until you have enough information to identify the two most likely causes. Ask one question at a time. 

---

Game Play Pattern 

**Create an interactive game around a topic.** Transforms learning or problem-solving into an engaging game with rules, scoring, and interactive feedback. 

> 
> **Template:** 
> Create a game for me around [TOPIC].
> Here are the fundamental rules:
> [RULE 1]
> [RULE 2]
> 
> 

**Example:** Create a cave exploration game for me to discover a lost language. Describe where I am and what I can do. I should discover new words and symbols in each cave area. Tell me about the first area. 

---

Template Pattern 

**Provide output structure using a template.** Specifies an exact format or structure that the LLM should follow when generating output. 

> 
> **Template:** 
> I am going to provide a template for your output.
> [PLACEHOLDER] is my placeholder for content.
> Please preserve the formatting and overall template.
> This is the template: [YOUR TEMPLATE WITH PLACEHOLDERS]
> 
> 

**Example:** Create a random strength workout. Here is my template: NAME, REPS @ SETS, MUSCLE GROUPS WORKED, DIFFICULTY 1-5, FORM NOTES 

---

Meta Language Creation Pattern 

**Define custom shortcuts or symbols.** Establishes shorthand syntax or custom language that the LLM should interpret according to your definitions. 

> 
> **Template:** 
> When I say [SYMBOL/PHRASE], I mean [DEFINITION].
> 
> 

**Example:** When I say "variations (X)", I mean give me ten different variations of X. Usage: "variations (company names for a software company)" 

---

Recipe Pattern 

**Fill in missing steps in a sequence.** Provides known steps toward a goal, and requests that the LLM complete the recipe with any missing steps. 

> 
> **Template:** 
> I would like to achieve [GOAL].
> I know that I need to perform steps [STEP A], [STEP B], [STEP C].
> Provide a complete sequence of steps for me.
> Fill in any missing steps.
> 
> 

**Example:** I would like to drive to NYC from Nashville. I want to go through Asheville, NC and don't want to drive more than 300 miles per day. Provide a complete sequence of steps. Fill in any missing steps. 

---

Alternative Approaches Pattern 

**Explore multiple solutions to a problem.** Prompts the LLM to identify and present several different ways to accomplish a task, with pros and cons. 

> 
> **Template:** 
> If there are alternative ways to accomplish [TASK], list the best alternate approaches. Compare and contrast the pros and cons of each approach. Ask me which approach I would like to use.
> 
> 

**Example:** For every prompt I give you, list alternative ways to word the prompt. Compare the pros and cons of each wording approach. 

---

Ask for Input Pattern 

**Request specific information from the user.** Instructs the LLM to solicit particular types of input before proceeding with a task. 

> 
> **Template:** 
> Ask me for [INPUT TYPΕ].
> 
> 

**Example:** From now on, I will cut/paste email chains. You will summarize each person's points as sequential bullet points. At the end, list any open questions or action items. Ask me for the first email. 

---

Menu Actions Pattern 

**Create a command-based interface.** Establishes a set of commands or keywords that trigger specific actions or behaviors. 

> 
> **Template:** 
> Whenever I type: [COMMAND X], you will [ACTION Y]. Whenever I type: [COMMAND Z], you will [ACTION Q]. At the end, ask me for the next action.
> 
> 

**Example:** Whenever I type "add FOOD", add it to my grocery list and update my estimated bill. Whenever I type "remove FOOD", remove it and update the bill. Ask for the next action. 

---

Outline Expansion Pattern 

**Progressively expand an outline into detailed content.** Generates an initial outline, then allows you to iteratively select sections to expand into greater detail. 

> 
> **Template:** 
> Act as an outline expander.
> Generate a bullet point outline based on the input I give you.
> Ask me which bullet point to expand.
> Create a new outline for the selected bullet.
> Ask which section to expand next.
> 
> 

**Example:** Create an outline for "Machine Learning Basics". I'll choose which section to expand, and you'll create a detailed outline for that section. 

---

Fact Check List Pattern 

**Generate and highlight key factual claims.** Identifies and lists the fundamental facts within an output that could undermine its accuracy if incorrect. 

> 
> **Template:** 
> Whenever you output text, generate a set of facts that are contained in the output. The set of facts should be inserted at [POSITION]. Include facts that could undermine veracity if incorrect.
> 
> 

**Example:** Provide a fact check list at the end of your output containing the key claims that should be verified. 

---

Tail Generation Pattern 

**Repeat options and request next input.** Ends output by restating available options or previous choices, then prompts for the next user action. 

> 
> **Template:** 
> At the end of your output:
> Repeat [INFORMATION].
> Ask me for [NEXT INPUT].
> 
> 

**Example:** At the end of your output, add this disclaimer: "This output was generated by a large language model and may contain errors. All statements should be fact-checked." Ask me for the first thing to write about. 

---

Semantic Filter Pattern 

**Remove specific types of information from output.** Instructs the LLM to filter or exclude particular categories of content from its response. 

> 
> **Template:** 
> Filter this information to remove [CRITERIA].
> 
> 

**Example:** Filter this information to remove everything but the first sentence of each paragraph. 

---

Combining Patterns 

Mix multiple patterns for complex tasks.  Use multiple patterns together to address sophisticated requirements. For example: 

* 
**Persona + Recipe**: Act as an expert AND fill in missing steps 


* 
**Cognitive Verifier + Template**: Ask clarifying questions AND format the output using a template 


* 
**Menu Actions + Tail Generation**: Define commands AND remind what's available at the end 


* 
**Outline Expansion + Audience Persona**: Expand detail AND explain for a specific audience 



---

Quick Reference: Pattern Selection Guide 

| Goal | Pattern(s) |
| --- | --- |
| Adopt expertise | Persona |
| Clarify explanations | Audience Persona |
| Improve your question | Question Refinement |
| Break down complexity | Cognitive Verifier |
| Interactive discovery | Flipped Interaction |
| Make learning fun | Game Play |
| Control output format | Template |
| Define shorthand | Meta Language Creation |
| Complete a plan | Recipe |
| Explore options | Alternative Approaches |
| Gather information | Ask for Input |
| Build commands | Menu Actions |
| Develop ideas | Outline Expansion |
| Verify claims | Fact Check List |
| End interactions | Tail Generation |
| Remove content | Semantic Filter |
