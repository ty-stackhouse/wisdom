# Using LLMs for Tabletop Exercises within the Security Domain

**Sam Hays, Dr. Jules White**  
Department of Computer Science, Vanderbilt University, Nashville, TN, USA  
{george.s.hays, jules.white}@vanderbilt.edu

## I. ABSTRACT
Tabletop exercises are a crucial component of many company’s strategy to test and evaluate its preparedness for security incidents in a realistic way. Traditionally led by external firms specializing in cybersecurity, these exercises can be costly, time-consuming, and may not always align precisely with the client’s specific needs. Large Language Models (LLMs) like ChatGPT offer a compelling alternative. They enable faster iteration, provide rich and adaptable simulations, and offer infinite patience in handling feedback and recommendations. This approach can enhances the efficiency and relevance of security preparedness exercises.

## II. INTRODUCTION
Tabletop exercises are common practice for many security teams in industry, serving as role-playing simulations where an attack is described and the team or teams involved respond in ways appropriate to the described scenario with the objective of identifying strengths and weaknesses as input to a continuous improvement process.

For example, a tabletop exercise might begin by setting the scene of an ongoing ransomware attack. During this phase it is common for the facilitator (or moderator) to alert the participants to what data is available immediately (e.g., stating that “all machines in the accounting department are unable to login and a message is displayed demanding payment in the form of Bitcoin”).

After the scene is set, team roles may be noted and/or assigned (e.g., Incident Commander) to the players. These roles can be specific to an organization but typically include:

- **Facilitator** - the person or team presenting the scenario and leading the discussion, as well as disclosing information as it becomes available
- **Incident Commander** - This person is assigned to lead the incident response
- **Security Team Members** - various security and infrastructure professionals who will provide input during the scenario. These may include Security Engineers, Network Administrators/Engineers, Analysts, etc.
- **Communications Officer** - Handles internal and external communications of the incident
- **Marketing/PR** - Potentially in partnership with Communications Officer, represents the voice of public relations and keeps company image in mind and may issue public statements, etc.
- **Legal Advisor** - Provides advice on legal impact as well regulatory or compliance obligations (e.g., disclosure requirements)
- **Human Resources** - An individual who represents the voice from Human Resources and would handle personnel related issues
- **Senior Leadership** - A senior leader who can make high-stakes or high-level decisions. Typically CEO, CIO, CTO, or CISO
- **Leadership** - Managers/Directors from departments participating in the tabletop
- **Helpdesk** - Typically a senior person from the customer support or helpdesk department who would coordinate necessary response actions to that group
- **External teams** - This may include vendors of security products or services, forensic teams, external legal council, or anyone else that can participate to the scenario (where appropriate) and potentially provide insights and value

After roles are established and understood by everyone, the team will begin discussing the situation and working towards a resolution, ideally with the guidance of existing and current Incident Response Playbooks (IRPs). The person or team running the simulation (the facilitator(s)) will describe the results of the decisions made. They may also keep time to track the duration of some or all steps taken, whether or not an appropriate incident response plan is in place, if incident response communications were using a compromised channel, etc. These data are collected and analyzed after the event for use in the retrospective meeting and subsequent improvement plan.

While these types of exercises can be valuable for a security team, they can also be quite costly to run (often in excess of $50,000 ). They may also require significant planning efforts; the Cybersecurity & Infrastructure Security Agency (CISA)’s CISA Tabletop Exercise Package (CTEP) suite of documentation suggests at least three months of planning  due to factors such as team engagement, objective planning, various necessary meetings, size and complexity of scenario, size and complexity of participating team, etc. Furthermore, The quality of these exercises can vary depending on if it was planned by internal personnel, external companies specializing in running tabletop exercises, or a hybrid approach.

This is where Large Language Models (LLMs) come into play. Integrating LLMs can reduce costs, shorten planning time, increase exercise frequency, and provide a dynamic feedback loop for continuous improvement.

This paper explores how LLMs can be tailored to organizational needs, enhancing the relevance and impact of tabletop exercises, and effectively streamlining the security preparation process.

*(Figure 1: Tabletop Exercise: Common Workflow - Flowchart showing: Tabletop Exercise Starts -> Scenario Presentation -> Team Role Assignments -> Initial Response Actions -> Incident Analysis and Decision Making -> Incident Resolved? (No/Yes) -> Time Remaining in Exercise? (No/Yes) -> Debrief and Lessons Learned -> Update Policies and Procedures -> Exercise Ends)*

## III. BACKGROUND
As covered in Section II, tabletop exercises are role-playing simulations of a security-based scenario where people assume various roles (e.g., Incident Commander, Data Analyst) and make decisions based on the emerging information from the person running the scenario.

These types of exercises are excellent in helping ensure the participants are exposed to (ideally) unexpected events and that the needed tools, techniques, and response plans are in place to deal with them. In in either failure or success modes, the exercises should be considered “successful” insofar as a success validates the appropriate tools, skills, etc. are in-place and validated. In a failure case (e.g., the “damage” was total, critical data exfiltration was successful, etc.) then an opportunity is identified to add tools, controls, detections, or whatever else is needed to ensure such events are able to be handled in future real or simulated scenarios.

### A. Traditional Approach
A traditional tabletop exercise is often started as an engagement with an external security firm who includes such services in their portfolios or following guidelines like those offered by CISA. In both cases, the next step is to determine who will plan the exercise (described as the Exercise Planning Team [EPT] by CISA ).

After the planning team is established, a meeting or series of meetings which isolates the primary objectives of the exercise including scope, type, etc. Within the CISA framework this is referred to as the “Concept and Objectives” (C&O) meeting. Within the various frameworks of security firms, they may have different names but are similar in purpose.

With the C&O established, the meetings to layout the specific exercise scenario can begin. Once again, within the CISA framework this is called the “Initial Planning Meeting” (IPM). This meeting is intended for the purposes of defining objectives, capability alignment, the tabletop format, level of effort analysis, and so on.

If an external firm is retained for the project, this may be a point in which they go and develop the scenario in isolation or with minimal discussion to the EPT. If the scenario is following CISA, then another series of steps over several weeks is still recommend (i.e., Exercise Development phase, Midterm Planning Meeting, Invitation to players, Continued Development, and Final Planning Meeting) .

After the months of planning, the exercise can be conducted. Depending on the facilitator and framework, there will be differences in the execution but all cases a post-mortem or retrospective (or both), gap analysis, and final review will occur (though they may be merged into a smaller number of meetings with potentially different labels).

During the exercise itself, the facilitators(s) will reveal new temporal data as it would become available (e.g., “the CISO just received an email with a demand for payment which reads [...]”). It is also common for a user to describe an action they would take (e.g., “I’d look at the firewall logs for excessive egress traffic over the last 48 hours using Splunk.”) and if the scenario would include indicators of compromise in this data set, then they would be revealed at that moment.

Additionally, the client may not be collecting some (or even any) data which would be helpful in either detection or resolution, and those missing items would be discussed in a postmortem and retrospective meetings afterward. In practice, this means that certain planned discussion paths within the exercise may go unexplored because the team did not take the right action or ask the right question at the right time (e.g., a network sweep is not executed and thus does not reveal a secondary persistence strategy of the attacker). This is a learning opportunity and a typical outcome of these exercises is the identification of gaps or weaknesses and a plan to add compensating controls, detections, investigate new tooling, etc.

### B. Challenges With The Traditional Approach
Despite the obvious benefits of tabletop exercises (assuming the results are appropriately acted upon), it is common for many companies to hold these types of events semi-annually, annually, or even less frequently. We discuss some of the key reasons for this and suggest ways in which LLMs can increase frequency and reduce cost.

**1) Cost:** Tabletop exercises have a financial impact typically in the range of $30,000 to $50,000  when engaging with external security firms. Except for the largest companies, these costs are not trivial and may prove hard to justify. This is can be especially true when cybersecurity budgets can fluctuate year over year  . There is the addition time-complexity cost which will be covered in the next section.

From a budgetary perspective, leveraging LLMs offers a number of possible cost savings by reducing the frequency, or even potentially eliminating engagement with external firms. If, however, those engagements are desirable or even required for compliance or regulatory reasons, LLMs can still improve the value by improving security posture continuously and thereby ensuring the tabletop is more sophisticated and requires more sophisticated tactics.

**2) Complexity of Planning:** Planning a tabletop exercise can be a taxing administrative workload. The CISA framework suggests months of work during the planning phase prior to the execution of the tabletop. This is partly due to time requirements of selecting the EPT, engaging with multiple stakeholders, scenario design and iteration, availability of participating teams, etc. It is common to want a broad cross section of key teams (e.g., Legal, Security, IT, Helpdesk, Marketing/Communications) as well as at least one C-Suite represented for key decisions. Coordinating a team as diverse and large as this can be challenging for even mid-sized companies and holding the time such that everyone attends can, in some organizations, be nearly impossible.

In this paper we introduce the notion of micro-tabletops and describe their characteristics which should obviate or at least reduce the need for such broad engagement in every scenario. It will also demonstrate how tabletops can be undertaken by an individual, by a small team, across teams, and broadly.

**3) Team Preparedness:** We define team preparedness as a score-based measurement of expected efficiency of a team’s ability to execute on the tasks during an incident. We define this measurement in Fig. 2 where:

$$P = \frac{S + K + R + C + A + E}{P_{max}}$$
*(Fig. 2. Preparedness Equation)*

- **S** represents the average or cumulative measure of the team members’ skills relative to the responsibility domain. This can be quantified with professional certifications, years of experience, or skill assessments.
- **K** denotes the depth of knowledge in the domain, quantifiable through tests, certifications, and the completion of relevant training and continued education programs.
- **R** symbolizes resource availability, including tools, software, and other necessary resources to successfully perform job duties.
- **C** reflects team cohesion, a crucial indicator of preparedness, measurable via performance reviews, peer reviews, or similar systems.
- **A** indicates an adaptability score, showing a team’s ability to rapidly adapt to new technologies or handle issues promptly, determinable through adaptability assessments.
- **E** represents direct experience in performing their duties, quantifiable by the number of successful projects completed or time managing the system(s) for which they are responsible.

The result of the equation will be a value in the range of  with a value of 1 indicated perfect preparedness. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/120577586/c618318d-3e4d-49c9-9ec7-81502fd43cec/2403.01626v1.pdf)

With Preparedness Equation defined, we now define the preparedness delta as the difference in mastery over the responsibility domain between different teams. This will provide values between [-1, 1] where values near zero represent balanced preparedness scores, positive values indicating the P1 is more prepared and negative values indicating P2 is more prepared.

$$\Delta P = P_1 - P_2$$
*(Fig. 3. Preparedness Delta Equation)*

By way of example: if we consider a team from the IT department who is responsible for the Microsoft Azure platform who have been working together for years and built a deep knowledge of the system and all integration points and compare it to another team who may have just purchased a new CRM like Salesforce and have yet to come up to speed, then the preparedness delta would be high.

If we assume a 1-10 scale for values and plug in simulated but reasonable values given the scenario, we can see the following value for our hypothetical Azure and Salesforce teams:

$$\Delta P = \left(\frac{9 + 9 + 7 + 8 + 8 + 9}{60}\right) - \left(\frac{5 + 3 + 7 + 6 + 5 + 2}{60}\right) = \frac{50 - 28}{60} = 0.367$$

This positive value indicates that team A is likely more capable of handling the vicissitudes of a serious security incident. Ideally, all teams would have high preparedness values and cross-team comparisons will have a delta near zero.

Finally, we define the Unified Preparedness and Balance Score (Fig. 6) where:
- $\alpha$ is a weighting factor for preparedness over balance ($\alpha + \beta = 1$)
- $\beta$ is a weighting factor for balance over preparedness ($\alpha + \beta = 1$)
- $P_{avg}$ is the average preparedness score across all teams
- $\bar{|\Delta P|}$ is the average of all $\Delta P$ for all possible pairs of teams

$$UPBS = \alpha \cdot P_{avg} + \beta \cdot (1 - |\bar{\Delta P}|)$$
*(Fig. 6. Unified Preparedness and Balance Score Equation)*

The UPBS score is maximized (close to 1) when preparedness is maximized and teams are generally balanced (near 0).

### C. Benefits & Importance of Tabletop Exercises
Just like with any muscle, the path to strength and facility is with training. But, just as one does not build strength in a muscle by training it once a year, neither does a security team build strength (represented as: preparedness, efficiency, ingrained protocols and procedures, shared common language) by practicing infrequently. Operational Effectiveness involves repetition, and this is something LLMs can greatly facilitate.

For each tabletop exercise completed, a company will nearly always learn of a gap in their plan, a detection that could be written, a procedure or policy that is not codified in a way made obvious for consumption during an incident. As each of these are identified, they are shored up and then reinforced in subsequent events.

## IV. LARGE LANGUAGE MODELS OVERVIEW
While this work is not intended as technical paper for the implementation details of Large Language Models (LLMs), we provide here a high-level overview to help contextualize LLMs for the unfamiliar reader.

### A. A Brief Introduction to LLMs
Large Language Models are a type of artificial intelligence system that focuses on interacting with (reading, writing) human languages. They are trained on enormous data sets with the goal of generating text which should be indistinguishable from that written by a human - ideally a human-expert.

LLMs have come into prominence over the last several years primarily due to the work of OpenAI and its Generative Pre-Trained Transformer (GPT) set of tools and APIs.

### B. Capabilities of LLMs for Tabletop Exercises
It is clear that LLMs can produce results that are contextually appropriate and evocative in the cybersecurity domain. In this section, we will explore how specifically this technology can be leveraged to improve tabletop exercises.

**1) Scenario Generation:** Generating a tabletop exercise scenario can take time and effort for a human but with relatively simple instructions and context-setting, an LLM can assist with this easily.

**C. Retrospective and Recommendation**
The key deliverable of a tabletop exercise is the retrospective . This allows the team to review its performance during the exercise and identify areas for improvement.

Having acted as either the facilitator or an auditor, the LLM can make suggestions which may include tasks which are measurable. With a very small-scale tabletop, based on answers given, the LLM was able to generate measurable, actionable improvements to the security posture of the organization.

**D. Micro-Tabletop**
Tabletop exercises, due in part to their cost and complexity, are often larger-scale infrequent events. With the availability of LLMs, we can introduce the idea of a “micro-tabletop” where as little as a single person has frequent interactions with the LLM to continuously improve their own responsibility domain.

Alice may invoke small tabletop exercises for herself or her team on a weekly cadence. This allows a targeted tabletop prompt focused on the technology stack of the most interest to Alice and her team and reduces the noise associated with cross-team collaboration. The objective of these micro-tabletops would be to continuously impose new attack strategies on a team so that their individual sphere of responsibility is iteratively hardened over time.

## V. FUTURE IMPLICATIONS
With the introduction of LLMs to the marketplace and its general introduction to “AI-ification” , we can expect tabletop exercises to become more common and supported by these generative AI systems. Additionally, with the rapid increase of token limits, we may expect the amount of context-awareness to rapidly surpass what a human might reasonably deal with in short time intervals between exercises. [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/120577586/c618318d-3e4d-49c9-9ec7-81502fd43cec/2403.01626v1.pdf)

In less than one year, the ChatGPT 4 family has increased from 8,192 tokens to 128,000 tokens which represents an increase of 1462.5%. We can speculate that within a year, the LLM might be able to keep 1,500,000 words in its context for analysis.

## VI. CONCLUSION
Large Language Models such as ChatGPT and generative AI in general have already shown to be a breakthrough technology which is rapidly impacting nearly all global markets and industries. Security companies are already integrating with these technologies. In the cases of designing, executing, and reviewing security tabletop exercises, these systems are able to provide guidance and recommendations with little input.

## REFERENCES
 What are tokens and how to count them? [ppl-ai-file-upload.s3.amazonaws](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/120577586/c618318d-3e4d-49c9-9ec7-81502fd43cec/2403.01626v1.pdf)
 05, K. D. S. . S. How to deal with cybersecurity budget cuts, Nov 2023.  
 CISA. Cisa tabletop exercise package, 2023.  
 COOK, J. Ai-ification: Welcome to the next business revolution, Oct 2023.  
 NAHUM, D. Are tabletop exercises still relevant for modern cybersecurity?, Oct 2023.  
 SHARMA, S. Cisos are struggling to get cybersecurity budgets: Report, Sep 2023.
