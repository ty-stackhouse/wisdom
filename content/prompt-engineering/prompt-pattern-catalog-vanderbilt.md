# A Prompt Pattern Catalog to Enhance Prompt Engineering with ChatGPT

**Authors:** Jules White, Quchen Fu, Sam Hays, Michael Sandborn, Carlos Olea, Henry Gilbert, Ashraf Elnashar, Jesse Spencer-Smith, and Douglas C. Schmidt  
**Affiliation:** Department of Computer Science, Vanderbilt University, Nashville, TN, USA  
**Contact:** {jules.white, quchen.fu, george.s.hays, michael.sandborn, carlos.olea, henry.gilbert, ashraf.elnashar, jesse.spencer-smith, douglas.c.schmidt}@vanderbilt.edu  

---

### Abstract
Prompt engineering is an increasingly important skill set needed to converse effectively with large language models (LLMs), such as ChatGPT. Prompts are instructions given to an LLM to enforce rules, automate processes, and ensure specific qualities (and quantities) of generated output. Prompts are also a form of programming that can customize the outputs and interactions with an LLM.

This paper describes a catalog of prompt engineering techniques presented in pattern form that have been applied to solve common problems when conversing with LLMs. Prompt patterns are a knowledge transfer method analogous to software patterns since they provide reusable solutions to common problems faced in a particular context, i.e., output generation and interaction when working with LLMs.

This paper provides the following contributions to research on prompt engineering that apply LLMs to automate software development tasks. First, it provides a framework for documenting patterns for structuring prompts to solve a range of problems so that they can be adapted to different domains. Second, it presents a catalog of patterns that have been applied successfully to improve the outputs of LLM conversations. Third, it explains how prompts can be built from multiple patterns and illustrates prompt patterns that benefit from combination with other prompt patterns.

**Index Terms**—large language models, prompt patterns, prompt engineering

---

### I. INTRODUCTION
Conversational large language models (LLMs) [1], such as ChatGPT [2], have generated immense interest in a range of domains for tasks ranging from answering questions on medical licensing exams [3] to generating code snippets. This paper focuses on enhancing the application of LLMs in several domains, such as helping developers code effectively and efficiently with unfamiliar APIs or allowing students to acquire new coding skills and techniques.

LLMs are particularly promising in domains where humans and AI tools work together as trustworthy collaborators to more rapidly and reliably evolve software-reliant systems [4]. For example, LLMs are being integrated directly into software tools, such as Github’s Co-Pilot [5]–[7] and included in integrated development environments (IDEs), such as IntelliJ [8] and Visual Studio Code, thereby allowing software teams to access these tools directly from their preferred IDE.

A prompt [9] is a set of instructions provided to an LLM that programs the LLM by customizing it and/or enhancing or refining its capabilities. A prompt can influence subsequent interactions with—and output generated from—an LLM by providing specific rules and guidelines for an LLM conversation with a set of initial rules. In particular, a prompt sets the context for the conversation and tells the LLM what information is important and what the desired output form and content should be.

For example, a prompt could specify that an LLM should only generate code that follows a certain coding style or programming paradigm. Likewise, it could specify that an LLM should flag certain keywords or phrases in a generated document and provide additional information related to those keywords. By introducing these guidelines, prompts facilitate more structured and nuanced outputs to aid a large variety of software engineering tasks in the context of LLMs.

Prompt engineering is the means by which LLMs are programmed via prompts. To demonstrate the power of prompt engineering, we provide the following prompt:

> **Prompt:** “From now on, I would like you to ask me questions to deploy a Python application to AWS. When you have enough information to deploy the application, create a Python script to automate the deployment.”

This example prompt causes ChatGPT to begin asking the user questions about their software application. ChatGPT will drive the question-asking process until it reaches a point where it has sufficient information to generate a Python script that automates deployment. This example demonstrates the programming potential of prompts beyond conventional “generate a method that does X” style prompts or “answer this quiz question”.

Moreover, prompts can be engineered to program an LLM to accomplish much more than simply dictating the output type or filtering the information provided to the model. With the right prompt, it is possible to create entirely new interaction paradigms, such as having an LLM generate and give a quiz associated with a software engineering concept or tool, or even simulate a Linux terminal window. Moreover, prompts have the potential for self-adaptation, suggesting other prompts to gather additional information or generate related artifacts. These advanced capabilities of prompts highlight the importance of engineering them to provide value beyond simple text or code generation.

Prompt patterns are essential to effective prompt engineering. A key contribution of this paper is the introduction of prompt patterns to document successful approaches for systematically engineering different output and interaction goals when working with conversational LLMs. We focus largely on engineering domain-independent prompt patterns and introduce a catalog of essential prompt patterns to solve problems ranging from production of visualizations and code artifacts to automation of output steps that help fact check outputs.

The remainder of this paper is organized as follows: Section II introduces prompt patterns and compares these patterns to well-known software patterns [10]; Section III describes 16 prompt patterns that have been applied to solve common problems in the domain of conversational LLM interaction and output generation for automating software development tasks; Section IV discusses related work; and Section V presents concluding remarks and lessons learned.

---

### II. COMPARING SOFTWARE PATTERNS WITH PROMPT PATTERNS
The quality of the output(s) generated by a conversational LLM is directly related to the quality of the prompts provided by the user. As discussed in Section I, the prompts given to a conversational LLM can be used to program interactions between a user and an LLM to better solve a variety of problems. One contribution of this paper is the framework it provides to document patterns that structure prompts to solve a range of software tasks that can be adapted to different domains.

This framework is useful since it focuses on codifying patterns that can be applied to help users better interact with conversational LLMs in a variety of contexts, rather than simply discussing interesting examples or domain-specific prompts. Codifying this knowledge in pattern form enhances reuse and transferability to other contexts and domains where users face similar—but not identical—problems.

The topic of knowledge transfer has been studied extensively in the software patterns literature [10], [11] at multiple levels, e.g., design, architectural, and analysis. This paper applies a variant of a familiar pattern form as the basis of our prompt engineering approach. Since prompts are a form of programming, it is natural to document them in pattern form.

#### A. Overview of Software Patterns
A software pattern provides a reusable solution to a recurring problem within a particular context [10]. Documenting software patterns concisely conveys (and generalizes) from specific problems being addressed to identify important forces and/or requirements that should be resolved and/or addressed in successful solutions.

A pattern form also includes guidance on how to implement the pattern, as well as information on the trade-offs and considerations to take into account when implementing a pattern. Moreover, example applications of the pattern are often provided to further showcase the pattern’s utility in practice. Software patterns are typically documented in a stylized form to facilitate their use and understanding, such as:

*   **A name and classification.** Each pattern has a name that identifies the pattern and should be used consistently. A classification groups patterns into broad categories, such as creational, structural, or behavioral.
*   **The intent** concisely conveys the purpose the pattern is intended to achieve.
*   **The motivation** documents the underlying problem the pattern is meant to solve and the importance of the problem.
*   **The structure and participants.** The structure describes the different pattern participants (such as classes and objects) and how they collaborate to form a generalized solution.
*   **Example code** concretely maps the pattern to some underlying programming language(s) and aids developers in gaining greater insight into how that pattern can be applied effectively.
*   **Consequences** summarize the pros and cons of applying the pattern in practice.

#### B. Overview of Prompt Patterns
Prompt patterns are similar to software patterns in that they offer reusable solutions to specific problems. They focus more specifically, however, on the context of output generation from large-scale language models (LLMs), such as ChatGPT. Just as software patterns provide a codified approach to solving common software development challenges, prompt patterns provide a codified approach to customizing the output and interactions of LLMs.

By documenting and leveraging prompt patterns in the context of automating software development tasks, individual users and teams can enforce constraints on the generated output, ensure that relevant information is included, and change the format of interaction with the LLM to better solve problems they face. Prompt patterns can be viewed as a corollary to the broad corpus of general software patterns, just adapted to the more specific context of LLM output generation.

Prompt patterns follow a similar format to classic software patterns, with slight modifications to match the context of output generation with LLMs. Each of the analogous sections for the prompt pattern form used in this paper is summarized below:

*   **A name and classification.** The prompt pattern name uniquely identifies the pattern and ideally indicates the problem that is being addressed. For the classification, we have developed a series of initial categories of pattern types, which are summarized in Table I and include Output Customization, Error Identification, Prompt Improvement, Interaction, and Context Control.
*   **The intent and context** describes the problem the prompt pattern solves and the goals it achieves. The problem should ideally be independent of any domain, though domain-specific patterns may also be documented with an appropriate discussion of the context where the pattern applies.
*   **The motivation** provides the rationale for the problem and explains why solving it is important. The motivation is explained in the context of users interacting with a conversational LLM and how it can improve upon users informally prompting the LLM in one or more circumstances. Specific circumstances where the improvements are expected are documented.
*   **The structure and key ideas.** The structure describes the fundamental contextual information, as a series of key ideas, that the prompt pattern provides to the LLM. These ideas are similar to “participants” in a software pattern. The contextual information may be communicated through varying wording (just as a software pattern can have variations in how it is realized in code), but should have fundamental pieces of information that form a core element of the pattern.
*   **Example implementation** demonstrates how the prompt pattern is worded in practice.
*   **Consequences** summarize the pros and cons of applying the pattern and may provide guidance on how to adapt the prompt to different contexts.

#### C. Evaluating Means for Defining a Prompt Pattern’s Structure and Ideas
In software patterns, the structure and participants are normally defined in terms of UML diagrams, such as structure diagrams and/or interaction diagrams. These UML diagrams explain what the participants of the pattern are and how they interact to solve the problem. In prompt patterns, something analogous is needed, though UML may not be an appropriate structural documentation approach since it is intended to describe software structures, as opposed to the ideas to communicate in a prompt.

Several possible approaches could be used, ranging from diagrams to defining grammars for a prompt language. Although grammars may seem attractive due to their formal nature, they also incur the following challenges:

*   The goal of prompts is to communicate knowledge in a clear and concise way to conversation LLM users, who may or may not be computer scientists or programmers. As a community, we should strive to create an approachable format that communicates knowledge clearly to a diverse target audience.
*   It is possible to phrase a prompt in many different ways. It is hard, however, to define a grammar that accurately and completely expresses all the nuanced ways that components of a prompt could be expressed in text or symbols.
*   Prompts fundamentally convey ideas to a conversational LLM and are not simply the production of tokens for input. In particular, an idea built into a prompt pattern can be communicated in many ways and its expression should be at a higher-level than the underlying tokens representing the idea.
*   It is possible to program an LLM to introduce novel semantics for statements and words that create new ways for communicating an idea. In contrast, grammars may not easily represent ideas that can be expressed through completely new symbology or languages that the grammar designer was not aware of.

#### D. A Way Forward: Fundamental Contextual Statements
An open research question, therefore, is what approach is more effective than formal grammars for describing prompt pattern structure and ideas. We propose the concept of **fundamental contextual statements**, which are written descriptions of the important ideas to communicate in a prompt to an LLM. An idea can be rewritten and expressed in arbitrary ways based on user needs and experience. The key ideas to communicate, however, are presented to the user as a series of simple, but fundamental, statements.

One benefit of adopting and applying the fundamental contextual statements approach is that it is intentionally intuitive to users. In particular, we expect users will understand how to express and adapt the statements in a contextually appropriate way for their domain. Moreover, since the underlying ideas of the prompt are captured, these same ideas can be expressed by the user in alternate symbology or wording that has been introduced to the LLM using patterns, such as the Meta Language Creation pattern presented in Section III-B.

Our ultimate goal is to enhance prompt engineering by providing a framework for designing prompts that can be reused and/or adapted to other LLMs in the same way that software patterns can be implemented in different programming languages and platforms. For the purposes of this paper, however, all prompts were tested with ChatGPT [12] using the ChatGPT+ service. We use ChatGPT as the LLM for all examples presented in this paper due to its widespread availability and popularity. These examples were documented through a combination of exploring the corpus of community-posted prompts on the Internet and independent prompt creation from our use of ChatGPT to automating software development tasks.

---

### III. A CATALOG OF PROMPT PATTERNS FOR CONVERSATIONAL LLMS
This section presents our catalog of prompt patterns that have been applied to solve common problems in the domain of conversational LLM interaction and output generation for automating software tasks. Each prompt pattern is accompanied by concrete implementation samples and examples with and without the prompt.

#### A. Summary of the Prompt Pattern Catalog
The classification of prompt patterns is an important consideration in documenting the patterns. Table I outlines the initial classifications for the catalog of prompt patterns we identified in our work with ChatGPT thus far.

**TABLE I: CLASSIFYING PROMPT PATTERNS**

| Pattern Category | Prompt Pattern |
| :--- | :--- |
| **Input Semantics** | Meta Language Creation |
| **Output Customization** | Output Automater, Persona, Visualization Generator, Recipe, Template |
| **Error Identification** | Fact Check List, Reflection |
| **Prompt Improvement** | Question Refinement, Alternative Approaches, Cognitive Verifier, Refusal Breaker |
| **Interaction** | Flipped Interaction, Game Play, Infinite Generation |
| **Context Control** | Context Manager |

As shown in this table, there are five categories of prompt patterns in our classification framework: Input Semantics, Output Customization, Error Identification, Prompt Improvement, and Interaction, each of which is summarized below.

The **Input Semantics** category deals with how an LLM understands the input and how it translates the input into something it can use to generate output. This category includes the **Meta Language Creation** pattern, which focuses on creating a custom language for the LLM to understand. This pattern is useful when the default input language is ill-suited for expressing ideas the user wants to convey to the LLM.

The **Output Customization** category focuses on constraining or tailoring the types, formats, structure, or other properties of the output generated by the LLM. The prompt patterns in this category include **Output Automater, Persona, Visualization Generator, Recipe,** and **Template** patterns. 
*   The **Output Automater** pattern allows the user to create scripts that can automate any tasks the LLM output suggests the user should perform. 
*   The **Persona** pattern gives the LLM a persona or role to play when generating output. 
*   The **Visualization Generator** pattern allows the user to generate visualizations by producing textual outputs that can be fed to other tools, such as other AI-based image generators, like DALL-E [13]. 
*   The **Recipe** pattern allows the user to obtain a sequence of steps or actions to realize a stated end result, possibly with partially known information or constraints. 
*   The **Template** pattern allows the user to specify a template for the output, which the LLM fills in with content.

The **Error Identification** category focuses on identifying and resolving errors in the output generated by the LLM. This category includes the **Fact Check List** and **Reflection** patterns. 
*   The **Fact Check List** pattern requires the LLM to generate a list of facts the output depends on that should be fact-checked. 
*   The **Reflection** pattern requires the LLM to introspect on its output and identify any errors.

The **Prompt Improvement** category focuses on improving the quality of the input and output. This category includes the **Question Refinement, Alternative Approaches, Cognitive Verifier,** and **Refusal Breaker** patterns. 
*   The **Question Refinement** pattern ensures the LLM always suggests a better version of the user’s question. 
*   The **Alternative Approaches** pattern requires the LLM to suggest alternative ways of accomplishing a user-specified task. 
*   The **Cognitive Verifier** pattern instructs the LLM to automatically suggest a series of subquestions for the user to answer before combining the answers to the subquestions and producing an answer to the overall question. 
*   The **Refusal Breaker** pattern requires the LLM to automatically reword the user’s question when it refuses to produce an answer.

The **Interaction** category focuses on the interaction between the user and the LLM. This category includes the **Flipped Interaction, Game Play,** and **Infinite Generation** patterns. 
*   The **Flipped Interaction** pattern requires the LLM to ask questions rather than generate output. 
*   The **Game Play** pattern requires the LLM to generate output in the form of a game. 
*   The **Infinite Generation** pattern requires the LLM to generate output indefinitely without the user having to reenter the generator prompt each time.

Finally, the **Context Control** category focuses on controlling the contextual information in which the LLM operates. This category includes the **Context Manager** pattern, which allows the user to specify the context for the LLM’s output.

The remainder of this section describes each of these prompt patterns using the pattern form discussed in Section II-B.

#### B. The Meta Language Creation Pattern
1.  **Intent and Context:** During a conversation with an LLM, the user would like to create the prompt via an alternate language, such as a textual short-hand notation for graphs, a description of states and state transitions for a state machine, a set of commands for prompt automation, etc. The intent of this pattern is to explain the semantics of this alternative language to the LLM so the user can write future prompts using this new language and its semantics.
2.  **Motivation:** Many problems, structures, or other ideas communicated in a prompt may be more concisely, unambiguously, or clearly expressed in a language other than English (or whatever conventional human language is used to interact with an LLM). To produce output based on an alternative language, however, an LLM needs to understand the language’s semantics.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** When I say X, I mean Y (or would like you to do Y).
    The key structure of this pattern involves explaining the meaning of one or more symbols, words, or statements to the LLM so it uses the provided semantics for the ensuing conversation. This description can take the form of a simple translation, such as “X” means “Y”. The description can also take more complex forms that define a series of commands and their semantics, such as “when I say X, I want you to do [action]”. In this case, “X” is henceforth bound to the semantics of “take action”.
4.  **Example Implementation:** The key to successfully using the Meta Language Creation pattern is developing an unambiguous notation or shorthand, such as the following:
    > “From now on, whenever I type two identifiers separated by a “→”, I am describing a graph. For example, “a → b” is describing a graph with nodes “a” and “b” and an edge between them. If I separate identifiers by “-[w:2, z:3]→”, I am adding properties of the edge, such as a weight or label.”
    This example establishes a standardized notation for describing graphs by defining a convention for representing nodes and edges. It provides a clear and concise way to communicate the structure of a graph in written form, allowing for the specification of additional properties beyond the basic structure, which may not be easy or are very verbose to describe as a series of sentences.
5.  **Consequences:** Although this pattern provides a powerful means to customize interaction, it may create the potential for confusion within the LLM if the language introduces ambiguities. For example, using a common character like a comma to define new logic might conflict with standard punctuation. ChatGPT will often warn the user if a prompt creates too much confusion (e.g., trying to map the letter "a" to a specific entity like Marie Antoinette). It is best practice to use a single meta-language per conversation session to avoid conflicting semantics.

#### C. The Output Automater Pattern
1.  **Intent and Context:** The intent of this pattern is to have the LLM generate a script or other automation artifact that can automatically perform any steps it recommends taking as part of its output. The goal is to reduce the manual effort needed to implement any LLM output recommendations.
2.  **Motivation:** The output of an LLM is often a sequence of steps for the user to follow. For example, when asking an LLM to generate a Python configuration script it may suggest a number of files to modify and changes to apply to each file. However, having users continually perform the manual steps dictated by LLM output is tedious and error-prone.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Whenever you produce an output that has at least one step to take and the following properties (alternatively, always do this)...
    *   **Contextual Statement:** Produce an executable artifact of type X that will automate these steps.
    The first part identifies the situations under which automation should be generated. The second part provides a concrete statement of the type of output (e.g., “produce a Python script”) to perform the automation.
4.  **Example Implementation:**
    > “From now on, whenever you generate code that spans more than one file, generate a Python script that can be run to automatically create the specified files or make changes to existing files to insert the generated code.”
    This is particularly effective in software engineering where users would otherwise have to manually copy/paste snippets into multiple files. It can also be used for running terminal commands, cloud operations, or file system organization.
5.  **Consequences:** A concrete meaning for “automate” must be provided (like "generate a script"), or the LLM may claim it cannot automate things due to its lack of direct system access. This pattern works best when the full context needed for the automation is contained within the conversation. Users remain responsible for reviewing and understanding the generated scripts before execution, as LLMs can produce inaccuracies.

#### D. The Flipped Interaction Pattern
1.  **Intent and Context:** You want the LLM to ask questions to obtain the information it needs to perform some tasks. Rather than the user driving the conversation, the LLM drives it to focus on achieving a specific goal (e.g., a quiz or gathering info for a deployment script).
2.  **Motivation:** An LLM often has knowledge it can use to more accurately obtain information from the user. By flipping the flow, the LLM can better select the format, number, and content of interactions to reach a goal faster and more accurately.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** I would like you to ask me questions to achieve X.
    *   **Contextual Statement:** You should ask questions until this condition is met or to achieve this goal (alternatively, forever).
    *   **Contextual Statement (Optional):** Ask me the questions one at a time, two at a time, etc.
    Providing a goal allows the LLM to tailor its questions effectively. Scoping the interaction length or frequency (e.g., asking one question at a time) improves usability.
4.  **Example Implementation:**
    > “From now on, I would like you to ask me questions to deploy a Python application to AWS. When you have enough information to deploy the application, create a Python script to automate the deployment.”
    Specific constraints (like mentioning specific AWS services) lead to better outcomes.
5.  **Consequences:** Open-ended flipped interactions can vary significantly in the final artifact. If specific requirements are known, they should be injected into the initial prompt. Designers should consider the desired level of user engagement—minimal interaction (minimal control) versus high interaction where the user confirms all decisions (maximum engagement).

#### E. The Persona Pattern
1.  **Intent and Context:** Users would like LLM output to always take a certain point of view or perspective (e.g., a security expert or a Linux terminal). The intent is to give the LLM a “persona” that helps it select what types of output to generate and what details to focus on.
2.  **Motivation:** Users may not know what details are important but do know the role of the person they would normally ask for help. This pattern allows users to express needs without knowing exact output details.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Act as persona X.
    *   **Contextual Statement:** Provide outputs that persona X would create.
    The persona can be a job title, character, historical figure, or even an inanimate object.
4.  **Example Implementation:**
    > “From now on, act as a security reviewer. Pay close attention to the security details of any code that we look at. Provide outputs that a security reviewer would regarding the code.”
    Personas can also be non-human:
    > “You are going to pretend to be a Linux terminal for a computer that has been compromised by an attacker. When I type in a command, you are going to output the corresponding text that the Linux terminal would produce.”
5.  **Consequences:** Non-human personas can lead to "hallucinations" of context, such as an imaginary file system where the user can run commands. The LLM can also prompt for more context if it's acting as a database or system and needs to know the "table structure" or initial state.

#### F. The Question Refinement Pattern
1.  **Intent and Context:** This pattern engages the LLM in the prompt engineering process by ensuring it always suggests better or more refined versions of the user's questions.
2.  **Motivation:** Users may not be experts in a domain and may not know the best way to phrase a question. The LLM can use its internal knowledge to incorporate necessary assumptions or information into a better prompt.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Within scope X, suggest a better version of the question to use instead.
    *   **Contextual Statement (Optional):** Prompt me if I would like to use the better version instead.
4.  **Example Implementation:**
    > “From now on, whenever I ask a question about a software artifact’s security, suggest a better version of the question to use that incorporates information specific to security risks in the language or framework that I am using instead and ask me if I would like to use your question instead.”
    For instance, a general question about authentication might be refined into a question about mitigating XSS or CSRF in a specific framework like FastAPI.
5.  **Consequences:** This helps bridge the knowledge gap but risks narrowing the path of inquiry too rapidly, causing the user to miss the "big picture." This can be mitigated by combining it with the Cognitive Verifier or Persona patterns.

#### G. The Alternative Approaches Pattern
1.  **Intent and Context:** This ensures the LLM always offers alternative ways of accomplishing a task so a user isn't limited to the approaches they are already familiar with.
2.  **Motivation:** Humans suffer from cognitive biases. This pattern helps dissolve those biases by forcing the user to consider different methods and their relative merits.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Within scope X, if there are alternative ways to accomplish the same thing, list the best alternate approaches.
    *   **Contextual Statement (Optional):** Compare/contrast the pros and cons of each approach.
    *   **Contextual Statement (Optional):** Include the original way that I asked.
    *   **Contextual Statement (Optional):** Prompt me for which approach I would like to use.
4.  **Example Implementation:**
    > “Whenever I ask you to deploy an application to a specific cloud service, if there are alternative services to accomplish the same thing with the same cloud service provider, list the best alternative services and then compare/contrast the pros and cons of each approach with respect to cost, availability, and maintenance effort and include the original way that I asked. Then ask me which approach I would like to proceed with.”
5.  **Consequences:** This is highly effective in its generic form and can be tailored with domain-specific catalogs of approved alternatives.

#### H. The Cognitive Verifier Pattern
1.  **Intent and Context:** This pattern forces the LLM to subdivide a complex question into smaller, more manageable sub-questions, then combine the answers to provide a more accurate final response.
2.  **Motivation:** Research shows LLMs reason better when questions are subdivided. Additionally, users may initially ask questions that are too high-level or vague.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** When you are asked a question, follow these rules.
    *   **Contextual Statement:** Generate a number of additional questions that would help more accurately answer the question.
    *   **Contextual Statement:** Combine the answers to the individual questions to produce the final answer to the overall question.
4.  **Example Implementation:**
    > “When I ask you a question, generate three additional questions that would help you give a more accurate answer. When I have answered the three questions, combine the answers to produce the final answers to my original question.”
5.  **Consequences:** Users can dictate the exact number of questions. Too few might miss a critical point; too many might overwhelm the user.

#### I. The Fact Check List Pattern
1.  **Intent and Context:** This pattern requires the LLM to output a list of fundamental facts or assumptions present in its output. This allows the user to perform due diligence on the veracity of the response.
2.  **Motivation:** LLMs often generate convincing but factually incorrect text. A fact list encourages users to verify key points.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Generate a set of facts that are contained in the output.
    *   **Contextual Statement:** The set of facts should be inserted in a specific point in the output.
    *   **Contextual Statement:** The set of facts should be the fundamental facts that could undermine the veracity of the output if any of them are incorrect.
4.  **Example Implementation:**
    > “From now on, when you generate an answer, create a set of facts that the answer depends on that should be fact-checked and list this set of facts at the end of your output. Only include facts related to cybersecurity.”
5.  **Consequences:** Highly recommended when users are not experts in the domain. It doesn't work well for code samples (LLMs often refuse to "fact check" code), but is excellent for requirements files or version numbers.

#### J. The Template Pattern
1.  **Intent and Context:** Ensures the LLM output follows a precise, user-provided structure or template, especially for formats not known to the LLM.
2.  **Motivation:** Some use cases require specific application formatting (like a specific URL path or a custom data structure).
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** I am going to provide a template for your output.
    *   **Contextual Statement:** X is my placeholder for content.
    *   **Contextual Statement:** Try to fit the output into one or more of the placeholders that I list.
    *   **Contextual Statement:** Please preserve the formatting and overall template that I provide.
    *   **Contextual Statement:** This is the template: [PATTERN with PLACEHOLDERS].
4.  **Example Implementation:**
    > “I am going to provide a template for your output. Everything in all caps is a placeholder. Any time that you generate text, try to fit it into one of the placeholders that I list. Please preserve the formatting and overall template that I provide at https://myapi.com/NAME/profile/JOB”
5.  **Consequences:** This filters the output, which may eliminate useful context or descriptions the LLM would otherwise provide. It can be difficult to combine with patterns that require a specific output format (like the Recipe pattern).

#### K. The Infinite Generation Pattern
1.  **Intent and Context:** Automatically generates a series of outputs without the user having to re-enter the prompt each time.
2.  **Motivation:** Useful for repetitive tasks, like generating CRUD code for multiple entities, where retyping the prompt is tedious and error-prone.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** I would like you to generate output forever, X output(s) at a time.
    *   **Contextual Statement (Optional):** Here is how to use the input I provide between outputs.
    *   **Contextual Statement (Optional):** Stop when I ask you to.
4.  **Example Implementation:**
    > “From now on, I want you to generate a name and job until I say stop. I am going to provide a template for your output... [URL template]”
5.  **Consequences:** In long sessions, the model may "lose track" of the original instructions as the conversation history grows. Users should monitor outputs for deviation from the intended behavior.

#### L. The Visualization Generator Pattern
1.  **Intent and Context:** Uses text generation to create inputs for third-party visualization tools (like Graphviz or DALL-E) to produce imagery.
2.  **Motivation:** LLMs cannot produce images directly. This pattern creates a bridge to visual communication tools.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Generate an X that I can provide to tool Y to visualize it.
4.  **Example Implementation:**
    > “Whenever I ask you to visualize something, please create either a Graphviz Dot file or DALL-E prompt that I can use to create the visualization. Choose the appropriate tools based on what needs to be visualized.”
5.  **Consequences:** Expands the LLM's expressive capabilities into the visual domain via a tool pipeline.

#### M. The Game Play Pattern
1.  **Intent and Context:** Creates a game around a specific topic where the LLM guides the gameplay based on a limited set of rules.
2.  **Motivation:** Manually generating game content is time-consuming. The LLM can automate scenarios and interactions based on its domain knowledge.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Create a game for me around X.
    *   **Contextual Statement:** [One or more fundamental rules of the game].
4.  **Example Implementation:**
    > “We are going to play a cybersecurity game. You are going to pretend to be a Linux terminal... I am going to use commands to try and figure out how the system was compromised... To start the game, print a scenario of what happened...”
5.  **Consequences:** Can be combined effectively with Persona, Infinite Generation, and Visualization patterns.

#### N. The Reflection Pattern
1.  **Intent and Context:** Asks the model to explain the rationale, assumptions, and reasoning behind its answers.
2.  **Motivation:** Helps users assess validity and debug prompts when results don't meet expectations.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Whenever you generate an answer.
    *   **Contextual Statement:** Explain the reasoning and assumptions behind your answer.
    *   **Contextual Statement (Optional):** ...so that I can improve my question.
4.  **Example Implementation:**
    > “When you provide an answer, please explain the reasoning and assumptions behind your selection of software frameworks. If possible, use specific examples or evidence with associated code samples...”
5.  **Consequences:** May be less effective for non-technical users if the explanation is too technical. Risk of errors in the explanation itself (can be combined with Fact Check List).

#### O. The Refusal Breaker Pattern
1.  **Intent and Context:** Asks the LLM to help rephrase a question when it initially refuses to provide an answer.
2.  **Motivation:** LLMs may refuse due to phrasing or lack of knowledge. This helps users find an acceptable alternative wording.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Whenever you can’t answer a question.
    *   **Contextual Statement:** Explain why you can’t answer the question.
    *   **Contextual Statement:** Provide one or more alternative wordings of the question that you could answer.
4.  **Example Implementation:**
    > “Whenever you can’t answer a question, explain why and provide one or more alternate wordings of the question that you can’t answer so that I can improve my questions.”
5.  **Consequences:** Provides a potential path for misuse (bypassing guardrails). There is no guarantee the alternate questions will be helpful or semantically equivalent.

#### P. The Context Manager Pattern
1.  **Intent and Context:** Enables users to specify what context to consider or ignore, or to reset the conversation context entirely.
2.  **Motivation:** LLMs may get distracted by irrelevant prior parts of a conversation.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** Within scope X.
    *   **Contextual Statement:** Please consider Y.
    *   **Contextual Statement:** Please ignore Z.
    *   **Contextual Statement (Optional):** Start over.
4.  **Example Implementation:**
    > “When analyzing the following pieces of code, only consider security aspects.”
    > “Ignore everything that we have discussed. Start over.”
5.  **Consequences:** Resetting the context might accidentally remove helpful patterns or instructions injected earlier in the session.

#### Q. The Recipe Pattern
1.  **Intent and Context:** Constrains the output to a sequence of steps given partial "ingredients" or constraints.
2.  **Motivation:** Users often know the goal and some components but not the correct order or missing steps.
3.  **Structure and Key Ideas:** Fundamental contextual statements:
    *   **Contextual Statement:** I would like to achieve X.
    *   **Contextual Statement:** I know that I need to perform steps A, B, C.
    *   **Contextual Statement:** Provide a complete sequence of steps for me.
    *   **Contextual Statement:** Fill in any missing steps.
    *   **Contextual Statement:** Identify any unnecessary steps.
4.  **Example Implementation:**
    > “I am trying to deploy an application to the cloud. I know that I need to install the necessary dependencies on a virtual machine... sign up for an AWS account... Provide a complete sequence of steps... fill in missing... identify unnecessary steps.”
5.  **Consequences:** May introduce user bias by forcing the LLM to incorporate the user's initially suggested (but potentially unneeded) steps.

---

### IV. RELATED WORK
Software patterns [10], [11] are widely used to express intent independent of implementation. This work applies those concepts to prompt design. Previous studies have examined prompt keywords for image generation [29], classification tasks [31], and software bug fixing [33]. This paper complements that work by providing a structure for documenting and reasoning about prompts across various domains.

---

### V. CONCLUDING REMARKS
This paper presented a framework for a catalog of prompt patterns. Lessons learned include:
*   Prompt patterns significantly enrich LLM capabilities (e.g., cybersecurity games).
*   Documenting patterns is a useful first step, but more work is needed on pattern languages.
*   LLM capabilities will evolve, requiring constant refinement of these patterns.
*   The patterns are generalizable across many domains beyond software development.

---

### REFERENCES
[1] R. Bommasani et al., “On the opportunities and risks of foundation models,” 2021.  
[2] Y. Bang et al., “A multitask, multilingual, multimodal evaluation of chatgpt,” 2023.  
[3] A. Gilson et al., “How well does chatgpt do when taking the medical licensing exams?” 2022.  
[4] A. Carleton et al., “Architecting the future of software engineering,” 2022.  
[5] “Github copilot · your ai pair programmer.”  
[6] O. Asare et al., “Is github’s copilot as bad as humans at introducing vulnerabilities?” 2022.  
[7] H. Pearce et al., “Asleep at the keyboard? assessing the security of github copilot’s code contributions,” 2022.  
[8] J. Krochmalski, *IntelliJ IDEA Essentials*, 2014.  
[9] P. Liu et al., “Pre-train, prompt, and predict: A systematic survey of prompting methods,” 2023.  
[10] E. Gamma et al., *Design patterns: elements of reusable object-oriented software*, 1995.  
[11] D. C. Schmidt et al., *Pattern-oriented software architecture*, 2013.  
[12] OpenAI, “ChatGPT,” 2023.  
[13] OpenAI, “DALL·E 2,” 2023.  
[14] D. Zhou et al., “Least-to-most prompting enables complex reasoning,” 2022.  
[15] J. Ellson et al., “Graphviz and dynagraph,” 2004.  
[16] S. Owen, “Building a virtual machine inside a javascript library,” 2022.  
[17] P. Zhang et al., “Applying software patterns to address interoperability in blockchain,” 2017.  
[18] X. Xu et al., “A pattern collection for blockchain-based applications,” 2018.  
[19] E. A. van Dis et al., “Chatgpt: five priorities for research,” 2023.  
[20] L. Reynolds et al., “Prompt programming for large language models,” 2021.  
[21] J. Wei et al., “Chain of thought prompting elicits reasoning,” 2022.  
[22] J. Wei et al., “Emergent abilities of large language models,” 2022.  
[23] Y. Zhou et al., “Large language models are human-level prompt engineers,” 2022.  
[24] T. Shin et al., “Autoprompt: Eliciting knowledge from language models,” 2020.  
[25] A. Radford et al., “Language models are unsupervised multitask learners,” 2019.  
[26] D. Zhou et al., “Least-to-most prompting enables complex reasoning,” 2022.  
[27] J. Jung et al., “Maieutic prompting,” 2022.  
[28] S. Arora et al., “Ask me anything: A simple strategy for prompting language models,” 2023.  
[29] V. Liu et al., “Design guidelines for prompt engineering text-to-image models,” 2022.  
[30] P. Maddigan et al., “Chat2vis: Generating data visualisations via natural language,” 2023.  
[31] X. Han et al., “Ptr: Prompt tuning with rules for text classification,” 2022.  
[32] S. Wang et al., “Can chatgpt write a good boolean query for systematic review?” 2023.  
[33] C. S. Xia et al., “Conversational automated program repair,” 2023.  
[34] J. H. Choi et al., “Chatgpt goes to law school,” 2023.  
[35] S. Frieder et al., “Mathematical capabilities of chatgpt,” 2023.
