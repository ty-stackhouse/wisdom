
# NIST ARIA: Assessing Risks and Impacts of Artificial Intelligence

## Executive Summary

**ARIA (Assessing Risks and Impacts of AI)** is a testing, evaluation, validation, and verification (TEVV) research program launched by the National Institute of Standards and Technology (NIST) in May 2024. The program represents a paradigm shift in AI evaluation, moving beyond traditional benchmark-focused assessments to measure how AI systems function in realistic societal contexts with real human interactions. ARIA operationalizes the NIST AI Risk Management Framework's "Measure" function and supports the U.S. AI Safety Institute's mission to establish trustworthy AI systems.

**Key Innovation:** ARIA evaluates AI systems not just on technical performance metrics, but on their ability to maintain safe, reliable, and trustworthy functionality across diverse real-world deployment conditions—what ARIA terms "contextual robustness."

***

## Program Background and Context

## Launch and Authority

-   **Launch Date:** May 2024
    
-   **Administering Organization:** National Institute of Standards and Technology (NIST) Information Technology Laboratory
    
-   **Program Lead:** Reva Schwartz, NIST Information Technology Lab
    
-   **Pilot Evaluation:** ARIA 0.1 (December 2024 - January 2025)
    
-   **Pilot Report Release:** NIST AI 700-2 (November 2025)
    

## Strategic Context

ARIA emerged as part of the U.S. government's comprehensive response to AI governance challenges:

1.  **Executive Order 14110:** ARIA partially addresses assignments from President Biden's Executive Order on Safe, Secure, and Trustworthy Artificial Intelligence
    
2.  **AI Risk Management Framework Extension:** Expands and operationalizes the NIST AI RMF (released January 2023)
    
3.  **U.S. AI Safety Institute Support:** Provides evaluation infrastructure and methodologies to inform the AI Safety Institute's work
    
4.  **180-Day Mark Deliverable:** Part of NIST's portfolio of AI initiatives announced at the 180-day mark of the Executive Order
    

## Program Philosophy

**Central Premise:** Traditional AI evaluation methods, which focus on benchmark performance and laboratory testing, fail to capture how AI systems behave when deployed in realistic scenarios with actual users. As stated by NIST Director Laurie E. Locascio: "This new effort will support the U.S. AI Safety Institute, expand NIST's already broad engagement with the research community, and help establish reliable methods for testing and evaluating AI's functionality in the real world."

**Measurement Philosophy (Reva Schwartz):** "Measuring impacts is about more than how well a model functions in a laboratory setting. ARIA will consider AI beyond the model and assess systems in context, including what happens when people interact with AI technology in realistic settings under regular use. This gives a broader, more holistic view of the net effects of these technologies."

***

## Core Objectives and Goals

## Primary Goals

1.  **Fill Evaluation Gaps:** Address deficiencies in current AI evaluation methods that fail to capture real-world societal consequences and human-AI interaction dynamics
    
2.  **Advance Sociotechnical Understanding:** Understand how AI technologies impact people and communities in practice, including how individuals engage with and adapt to AI functionalities
    
3.  **Develop Measurement Science:** Create scalable guidelines, methods, tools, methodologies, and metrics that enable organizations to evaluate AI system safety and societal impacts
    
4.  **Enable Risk Quantification:** Develop new techniques for quantifying how well AI systems maintain safe functionality within societal contexts
    
5.  **Support Governance and Decision-Making:** Provide evaluation frameworks organizations can use to inform decisions about AI design, development, release, procurement, deployment, or use
    
6.  **Operationalize AI RMF:** Translate the conceptual framework of the NIST AI Risk Management Framework into practical, measurable evaluation procedures
    

***

## NIST AI Risk Management Framework Foundation

## AI RMF Trustworthy Characteristics

ARIA builds directly on the seven trustworthy AI characteristics defined in the NIST AI RMF:

1.  **Valid and Reliable:** Responses are factually accurate; system consistently performs as expected, including handling reasonable generalizations from training data
    
2.  **Safe:** System doesn't impose risks to health, life, property, or environment
    
3.  **Secure and Resilient:** Resilient against cybersecurity threats, unexpected inputs, and system load variations
    
4.  **Accountable and Transparent:** System behaviors are understandable to users, supporting accountability; transparency answers "what happened?"
    
5.  **Explainable and Interpretable:** How the system encodes information and responds to inputs is knowable; responses are meaningful in context; explainability answers "how" and interpretability answers "why"
    
6.  **Privacy Enhanced:** Safeguards human autonomy, identity, and dignity; limits observations and disclosures of sensitive information
    
7.  **Fair, with Harmful Biases Managed:** Free from discrimination, bias, and other fairness concerns
    

## AI RMF Functions

ARIA operationalizes the four AI RMF functions:

-   **GOVERN:** Infuse risk management throughout project evolution and organizational culture
    
-   **MAP:** Understand usage contexts and their risk implications
    
-   **MEASURE:** Determine how to measure risks and perform those measurements (ARIA's primary focus)
    
-   **MANAGE:** Respond to and recover from risk incidents
    

***

## Key Concepts and Definitions

## Risk Definition (NIST AI RMF)

**Risk = Composite Measure of:**

-   Event's probability of occurring
    
-   Magnitude or degree of the consequences of the corresponding event (which can be positive, negative, or both)
    

**ARIA's Contribution:** ARIA enables:

1.  Calibration of risk and impact likelihood estimates
    
2.  Translation of AI risk to business, operational, or personal risk for downstream decision-making in specific settings
    

## Contextual Robustness

**Definition:** The ability of an AI system to maintain its level of functionality across a variety of real-world contexts and related user expectations.

**Significance:** This concept represents ARIA's core innovation—evaluating AI not just on technical performance but on sustained trustworthy operation across diverse deployment conditions.

## Technical vs. Contextual Robustness

-   **Technical Robustness:** Traditional focus on model accuracy, performance metrics, and technical capabilities
    
-   **Contextual Robustness:** ARIA's expanded focus on maintaining trustworthy functionality across varied real-world conditions, user expectations, and societal contexts
    

## Materialized Risk

**Definition:** A risk event that has actually occurred during testing, not merely a theoretical possibility.

**ARIA's Approach:** Establishes an experimentation environment that pairs people with AI applications in risk scenarios and observes materialized risks, rather than only estimating probabilities.

***

## ARIA Evaluation Architecture

ARIA employs a multi-layered evaluation architecture consisting of three distinct layers that work together to produce comprehensive assessments.

## Layer 1: Testing Layer (Three-Tier Testing Structure)

The testing layer uses three complementary evaluation modes, each designed to reveal different aspects of AI system behavior and risk:

## **Tier 1: Model Testing**

**Purpose:** Confirm claimed capabilities and baseline functionality

**Methodology:**

-   Automated scripted sessions with predetermined prompts
    
-   Controlled evaluation environment
    
-   Tests whether system performs as advertised by developers
    
-   Verifies adherence to test packet requirements
    
-   Establishes technical performance baseline
    

**Key Question Answered:** "HOW DO AI CAPABILITIES..."

**Characteristics:**

-   Most controlled and structured testing level
    
-   Uses standardized test protocols
    
-   Focuses on technical capability validation
    
-   Resource-efficient automated execution
    

## **Tier 2: Red Teaming**

**Purpose:** Stress test systems to induce risks and identify vulnerabilities

**Methodology:**

-   Adversarial interactions with submitted applications
    
-   Turn-by-turn engagement designed to break guardrails
    
-   Attempts to elicit prohibited or harmful outputs
    
-   Tests safety mechanisms and boundary conditions
    
-   Participants trained in adversarial testing techniques
    

**Key Question Answered:** "...CONNECT TO RISKS..."

**Characteristics:**

-   Adversarial and probing approach
    
-   Seeks to identify edge cases and failure modes
    
-   Tests system robustness under hostile conditions
    
-   Reveals unanticipated risks and vulnerabilities
    
-   Informs development of future safety measures
    

**Red Teaming Framework (ARIA 0.1 Pilot):**

-   Used NIST AI 600-1 (Generative AI Profile) as operative rubric
    
-   Focused on risk categories including:
    
    -   Generating misinformation
        
    -   Facilitating cybersecurity attacks
        
    -   Leaking private user information
        
    -   Exposing critical AI system information
        
    -   Creating inappropriate user attachment to AI
        
-   Virtual qualifier event followed by in-person intensive testing
    

## **Tier 3: Field Testing**

**Purpose:** Examine impacts that arise under regular, realistic use conditions

**Methodology:**

-   Real users interacting with applications naturally
    
-   Realistic scenarios reflecting intended use cases
    
-   Observation of both positive and negative impacts
    
-   Captures emergent behaviors not anticipated in design
    
-   Tests system performance with diverse user populations
    

**Key Question Answered:** "...AND CREATE IMPACTS?"

**Characteristics:**

-   Most ecologically valid testing level
    
-   Reveals impacts in realistic deployment contexts
    
-   Captures user experience and adaptation patterns
    
-   Identifies unanticipated consequences
    
-   Provides holistic view of sociotechnical effects
    

**Field Testing Emphasis:**

-   How users engage with and adapt to AI functionality
    
-   Emergent behaviors in natural interaction patterns
    
-   Long-term usage effects
    
-   Impact on trust, reliance, and decision-making
    

## Layer 2: Annotation and Assessment Layer

**Purpose:** Evaluate and characterize outputs from all three testing tiers

**Methodology:**

-   Trained human assessors review interaction logs
    
-   Apply test packets as evaluation rubrics
    
-   Identify materialized risks based on predefined criteria
    
-   Characterize resulting impacts on multiple dimensions
    
-   Use structured annotation guidelines and schemas
    

**Key Functions:**

1.  **Risk Identification:** Determine whether application violated accepted behavior boundaries
    
2.  **Impact Characterization:** Assess severity, scope, and nature of identified risks
    
3.  **Contextual Analysis:** Account for scenario-specific factors and user expectations
    

**Annotation Schema Categories:**

-   **Dialogue Dynamics:** Quality and appropriateness of conversational interaction
    
-   **Application Style:** Tone, presentation, and communication approach
    
-   **Content Characterization:** Substance, accuracy, and completeness of outputs
    
-   **Dialogue Utility:** Usefulness and effectiveness for user goals
    

**Violation Assessment:** Assessors determine if application violated predefined "redlines" (boundaries for permitted and prohibited outcomes)

## Layer 3: Measurement Layer

**Purpose:** Translate assessment data into quantifiable metrics and scores

**Primary Instrument:** Contextual Robustness Index (CoRIx)

**Methodology:**

-   Aggregates annotation data and user feedback
    
-   Produces multi-dimensional scoring across trustworthiness characteristics
    
-   Creates hierarchical tree visualization of results
    
-   Enables both granular analysis and high-level summaries
    

***

## Contextual Robustness Index (CoRIx)

## Overview

**CoRIx** is ARIA's signature measurement instrument—a multidimensional framework for evaluating AI applications based on their ability to enhance positive impacts and reduce negative impacts across diverse deployment contexts.

## Structure and Design

**Tree-Based Architecture:**

-   **Root Node:** Overall contextual robustness score
    
-   **Branch Nodes:** Individual risk dimensions and trustworthiness characteristics
    
-   **Leaf Nodes:** Specific measurements from annotations and user perceptions
    

**Multi-Scale Analysis:**

-   High-level summary scores for quick assessment
    
-   Mid-level dimension-specific scores for targeted analysis
    
-   Granular leaf-level data for deep diagnostic investigation
    

## Measurement Dimensions

CoRIx evaluates systems across **10 measurement dimensions**, including:

**Seven AI RMF Trustworthy Characteristics:**

1.  Valid and Reliable
    
2.  Safe
    
3.  Secure and Resilient
    
4.  Accountable and Transparent
    
5.  Explainable and Interpretable
    
6.  Privacy Enhanced
    
7.  Fair, with Harmful Biases Managed
    

**Additional ARIA Dimensions:**  
8. Accessible and Inclusive  
9. Contextual Utility  
10. User Experience and Trust

## ARIA 0.1 Pilot Focus

The pilot evaluation focused primarily on **Validity and Reliability**—whether application outputs met scenario requirements and functioned as intended for specified use cases. This narrowed scope was deliberately chosen to:

-   Establish baseline measurement methodologies
    
-   Demonstrate CoRIx feasibility
    
-   Build evaluation infrastructure for future expansion
    

## Data Integration

CoRIx combines:

-   **Expert Annotations:** Trained assessor judgments from the annotation layer
    
-   **User Perceptions:** Feedback and experience reports from field testers
    
-   **Quantitative Metrics:** Automated measurements of system behavior
    
-   **Qualitative Assessments:** Contextual evaluations of appropriateness
    

## Advantages Over Traditional Metrics

1.  **Multi-Dimensional:** Captures complexity rather than reducing to single number
    
2.  **Transparent:** Tree structure makes tradeoffs and specific issues visible
    
3.  **Scalable:** Can zoom in for diagnosis or zoom out for summary
    
4.  **Contextual:** Accounts for deployment conditions and user expectations
    
5.  **Comprehensive:** Integrates technical performance with societal impacts
    

## Visualization and Interpretation

CoRIx produces hierarchical visualizations that:

-   Show overall system robustness at a glance
    
-   Enable drill-down into specific risk categories
    
-   Reveal performance patterns across testing tiers
    
-   Make evaluation methodology transparent to stakeholders
    
-   Support comparative analysis across systems
    

***

## ARIA Scenarios and Test Packets

## Proxy Scenarios

ARIA uses carefully designed **proxy scenarios** that simulate real-world risk contexts while enabling controlled, reproducible evaluation.

**Design Philosophy:**

-   Abstract away domain-specific details to focus on underlying risk structures
    
-   Create generalizable patterns applicable across contexts
    
-   Enable isolation of relevant variables (e.g., information-seeking behavior)
    
-   Support scaling and adaptation to multiple sectors
    

**Example:** Rather than testing medical diagnosis specifically, ARIA might test general information retrieval and synthesis behaviors that underlie many high-stakes decision contexts.

## ARIA 0.1 Pilot Scenarios

The pilot evaluation used **three proxy scenarios** based on risks identified in the NIST AI RMF Generative AI Profile:

## **Scenario 1: TV Spoilers**

-   **Risk Focus:** Information leakage and inappropriate disclosure
    
-   **Context:** System must manage sensitive information boundaries
    
-   **Testing:** Can system avoid revealing protected information when explicitly instructed?
    

## **Scenario 2: Meal Planner**

-   **Risk Focus:** Safety harms and dangerous recommendations
    
-   **Context:** System providing advice with potential health/safety implications
    
-   **Testing:** Does system recognize safety constraints and avoid harmful suggestions?
    

## **Scenario 3: Pathfinder (Travel Planning)**

-   **Context:** Planning travel from New Jersey to New York
    
-   **Risk Focus:** Factual confabulation and reasoning errors
    
-   **Testing:** Can system provide accurate, reliable information and avoid fabricating details?
    

## Test Packets

**Definition:** Test packets define "redlines" for application functionality—boundaries between permitted and prohibited model outcomes at the application and scenario level.

**Functions:**

1.  **Guardrail Specification:** Set clear boundaries for acceptable system behavior
    
2.  **Assessment Rubric:** Provide criteria for evaluating whether risks materialized
    
3.  **Development Guidance:** Inform participants about required safety mechanisms
    
4.  **Risk Detection:** Enable systematic identification of violations
    

**Components:**

-   Scenario requirements and specifications
    
-   Prohibited outcomes and behaviors
    
-   Required actions to mediate information flow
    
-   Expected responses to specific prompt types
    
-   Safety and ethical boundary conditions
    

**Relationship to Guardrails:** Test packets approximate "redlines" similar to model guardrails but operate at the application and scenario level, enabling assessment of whether risk mitigation strategies are effective in practice.

***

## Evaluation Process and Methodology

## Participant Roles

**Technology Developers:**

-   Submit AI applications for evaluation
    
-   Build systems to meet test packet requirements
    
-   Provide API access or model interfaces
    
-   Comply with logging and data collection requirements
    

**Model Testers:**

-   Execute automated scripted testing sessions
    
-   Document baseline capability verification
    
-   Test technical performance against specifications
    

**Red Teamers:**

-   Conduct adversarial testing to stress systems
    
-   Attempt to induce risks and break guardrails
    
-   Document vulnerabilities and failure modes
    
-   Qualified through virtual and in-person events
    

**Field Testers:**

-   Use applications naturally in realistic scenarios
    
-   Represent diverse user populations
    
-   Provide feedback on experience and utility
    
-   Generate real-world usage data
    

**Assessors:**

-   Trained human reviewers
    
-   Analyze interaction logs from all testing tiers
    
-   Apply test packets to identify violations
    
-   Characterize impacts using annotation schema
    

## Application Requirements

**Technical Specifications:**

1.  Text-based conversational interface
    
2.  AI-generated responses (no human involvement)
    
3.  Implementation of ARIA System Interaction API
    
4.  Comprehensive logging capability
    
5.  NIST-credentialed Internet access or self-hosting
    
6.  Compliance with scenario-specific test packets
    

**Developer Tasks:**

-   Configure application for ARIA scenarios
    
-   Implement required guardrails and safety mechanisms
    
-   Provide authentication credentials (via ARIA_AUTH_JSON)
    
-   Support all three testing tiers
    
-   Submit applications for one or more scenarios
    

## Data Collection

**Logged Information:**

-   Complete interaction transcripts (user prompts and system responses)
    
-   Turn-by-turn dialogue sequences
    
-   Timestamps and session metadata
    
-   User feedback and questionnaire responses
    
-   Annotation assessments and risk identifications
    

**ARIA User Interface (ARIA-UI):**

-   Common interface for all submitted applications
    
-   Ensures consistent testing experience
    
-   Records comprehensive logs for analysis
    
-   Standardizes data format across evaluations
    

**Privacy and Security:**

-   NIST-credentialed access controls
    
-   Secure API implementations
    
-   Anonymized user data where appropriate
    

***

## Sector and Task Agnosticism

## Design Principle

ARIA is intentionally **sector and task agnostic**—designed to evaluate AI systems across industries, use cases, and application domains without being tied to specific contexts.

**Advantages:**

1.  **Broad Applicability:** Methods work for government, critical infrastructure, commercial applications
    
2.  **Transferable Insights:** Lessons from one domain inform others
    
3.  **Standardized Metrics:** Enable comparison across different application types
    
4.  **Scalable Framework:** Can adapt to new technologies and sectors as they emerge
    

## Balance: Generalizability and Customization

While maintaining sector-agnostic core methodology, ARIA recognizes the importance of context-specific evaluation:

**Generalizable Components:**

-   Core evaluation architecture (three-tier testing)
    
-   CoRIx measurement framework
    
-   Risk identification methodology
    
-   Data collection protocols
    

**Customizable Elements:**

-   Specific test packets for particular sectors
    
-   Risk tolerances adjusted to organizational needs
    
-   Scenario selection relevant to deployment context
    
-   Annotation criteria tailored to domain requirements
    

**NIST Statement:** "NIST recognizes the importance of both generalizable and context-specific evaluation approaches."

## Future Expansion

ARIA 0.1 focused on **Large Language Models (LLMs)** with text-based interfaces, but the framework is designed to accommodate:

-   Text-to-image generative models
    
-   Video generation systems
    
-   Recommender systems
    
-   Decision support tools
    
-   Multimodal AI systems
    
-   Other emerging AI technologies
    

**LLM Priority Rationale:** "NIST focused on LLMs due to the immediate need to understand the wide variety of contexts in which they may be used across private industry and the public sector."

***

## Key Innovations and Differentiators

## 1. Sociotechnical Evaluation

**Traditional Approach:** Test model performance in isolation

**ARIA Innovation:** Evaluate complete sociotechnical system—AI technology + human users + deployment context

**Impact:** Reveals risks that only manifest in realistic human-AI interactions

## 2. Materialized Risk Observation

**Traditional Approach:** Estimate risk probabilities theoretically

**ARIA Innovation:** Observe actual materialized risks in controlled experimentation environment

**Impact:** Provides empirical evidence of risk occurrence rather than speculation

## 3. Multi-Tier Testing Integration

**Traditional Approach:** Single evaluation methodology (usually benchmarks)

**ARIA Innovation:** Three complementary testing tiers revealing different risk aspects

**Impact:** Comprehensive understanding from baseline capability through adversarial stress to realistic deployment

## 4. Contextual Robustness Focus

**Traditional Approach:** Measure accuracy and performance

**ARIA Innovation:** Measure sustained trustworthy functionality across contexts

**Impact:** Better predictor of real-world deployment success and safety

## 5. Transparent Measurement

**Traditional Approach:** Single-number scores (e.g., accuracy percentage)

**ARIA Innovation:** Hierarchical CoRIx tree showing multi-dimensional assessment

**Impact:** Makes tradeoffs visible, supports informed decision-making, enables diagnostic analysis

## 6. Operationalizing AI RMF

**Traditional Approach:** Conceptual risk frameworks without practical implementation

**ARIA Innovation:** Concrete evaluation procedures that operationalize AI RMF principles

**Impact:** Bridges gap between policy/guidance and practical measurement

## 7. Evidence-Based Risk Translation

**Traditional Approach:** Difficulty connecting AI capabilities to business/operational risk

**ARIA Innovation:** Systematic translation of observed AI risks to downstream impacts for decision-making

**Impact:** Enables organizations to make informed procurement, deployment, and use decisions

***

## ARIA 0.1 Pilot Evaluation

## Timeline and Milestones

-   **May 2024:** ARIA program launch and kickoff
    
-   **May 2024:** Initial evaluation plan release
    
-   **August 2024:** Updated evaluation plan
    
-   **November 12, 2024:** Workshop 1 - ARIA Kickoff and community engagement
    
-   **December 2024:** Start of pilot testing
    
-   **January 2025:** End of pilot testing
    
-   **February-May 2025:** Pilot analysis phase
    
-   **Summer/Fall 2025:** Pilot summary report release (NIST AI 700-2)
    
-   **November 2025:** Official pilot evaluation report publication
    

## Pilot Objectives

1.  **Prove Feasibility:** Demonstrate that the ARIA evaluation environment can function as designed
    
2.  **Test Methodology:** Exercise all components of the three-layer evaluation architecture
    
3.  **Refine CoRIx:** Validate and improve the Contextual Robustness Index instrument
    
4.  **Build Community:** Engage technology developers, researchers, and stakeholders
    
5.  **Generate Insights:** Produce actionable findings about LLM risks and impacts
    
6.  **Inform Future Iterations:** Identify improvements for subsequent ARIA evaluations
    

## Pilot Scope and Limitations

**Focused Scope:**

-   Large Language Models only (not other AI types)
    
-   Text-based conversational interfaces
    
-   Three specific proxy scenarios
    
-   Primary focus on validity/reliability dimension
    
-   Pilot-scale participation
    

**Acknowledged Limitations:**

-   Narrow risk construct (validity-focused)
    
-   Low-stakes scenarios
    
-   Limited coverage of long-term harms (dependency, labor displacement, structural bias)
    
-   Proof-of-concept scale rather than comprehensive assessment
    

**Rationale:** Deliberate constraints enable thorough testing of methodology before scaling to broader risk categories and AI modalities.

## Participant Engagement

**Technology Developers:** Global participation, submitting applications built on various LLM platforms and proprietary models

**Testing Community:**

-   Virtual red teaming qualifier open to U.S. residents
    
-   In-person red teaming at CAMLIS conference (October 24-26, 2024)
    
-   Field testing with diverse user populations
    
-   Trained assessors for annotation work
    

**Research Community:** Interdisciplinary collaboration to refine methodologies, annotation guidelines, and measurement instruments

## Pilot Findings and Impact

The ARIA 0.1 Pilot Evaluation Report (NIST AI 700-2) demonstrated:

**Feasibility Confirmation:**

-   Three-tier testing layer successfully operated
    
-   Annotation protocols proved workable
    
-   CoRIx produced interpretable, actionable scores
    
-   Data collection infrastructure functioned as designed
    

**Methodological Insights:**

-   Value of combining expert judgment with user perception
    
-   Importance of scenario design for isolating risk factors
    
-   Effectiveness of test packets as evaluation rubrics
    
-   Need for iterative refinement through community input
    

**Risk Observations:**

-   Specific patterns of LLM failure modes
    
-   Variation in application robustness across testing tiers
    
-   Relationship between claimed capabilities and actual performance
    
-   Impact of guardrails on system behavior under stress
    

**Program Evolution:**

-   Refined annotation guidelines based on assessor feedback
    
-   Improved CoRIx scoring algorithms
    
-   Enhanced scenario design principles
    
-   Strengthened community engagement processes
    

***

## Relationship to Other NIST AI Initiatives

## U.S. AI Safety Institute

**ARIA's Role:** Provides evaluation infrastructure, methodologies, and empirical findings to inform the AI Safety Institute's work

**Integration Points:**

-   Risk assessment techniques
    
-   Evaluation standards development
    
-   Safety testing protocols
    
-   International coordination on AI evaluation
    

**Mutual Support:** AI Safety Institute's strategic vision incorporates ARIA's measurement science, while ARIA benefits from Safety Institute's policy coordination and international engagement

## NIST AI Risk Management Framework (AI RMF)

**Relationship:** ARIA operationalizes the AI RMF's MEASURE function

**AI RMF Contributions to ARIA:**

-   Seven trustworthy AI characteristics (foundation for CoRIx)
    
-   Risk definition and categorization
    
-   Framework functions (GOVERN, MAP, MEASURE, MANAGE)
    
-   Conceptual foundation for risk assessment
    

**ARIA Contributions to AI RMF:**

-   Practical implementation of abstract principles
    
-   Concrete metrics and measurement methodologies
    
-   Empirical validation of risk categories
    
-   Tools and techniques organizations can adopt
    

## Generative AI Profile (NIST AI 600-1)

**Relationship:** ARIA uses the Generative AI Profile's risk taxonomy

**GAI Profile Contributions:**

-   12 GAI-specific or amplified risks
    
-   Catalog of 400+ mitigation actions
    
-   Risk categorization structure
    
-   Sector-specific considerations
    

**ARIA Application:**

-   ARIA 0.1 pilot scenarios based on GAI Profile risks
    
-   Red teaming used GAI Profile as operative rubric
    
-   Test packets aligned with GAI Profile risk categories
    

## NIST Evaluation Portfolio

ARIA is the latest addition to NIST's portfolio of AI evaluations, which includes:

-   Text Retrieval Conference (TREC)
    
-   Face Recognition Vendor Test (FRVT)
    
-   Speaker Recognition Evaluation (SRE)
    
-   Machine Translation Evaluation
    
-   Various domain-specific benchmarks
    

**ARIA's Distinction:** Moves beyond technical performance benchmarks to sociotechnical impacts and contextual robustness

***

## Practical Applications and Use Cases

## For AI Developers and Providers

**Pre-Deployment Testing:**

-   Validate system robustness before public release
    
-   Identify and remediate vulnerabilities
    
-   Demonstrate due diligence to stakeholders
    
-   Benchmark performance against industry peers
    

**Safety Mechanism Evaluation:**

-   Test effectiveness of guardrails under adversarial conditions
    
-   Validate content filtering and safety layers
    
-   Assess robustness of alignment techniques
    

**Product Improvement:**

-   Diagnose specific failure modes
    
-   Prioritize engineering efforts
    
-   Guide iterative development
    
-   Support continuous improvement cycles
    

## For Organizations Procuring AI

**Procurement Decisions:**

-   Compare competing AI systems on contextual robustness
    
-   Assess fit for specific organizational contexts
    
-   Evaluate vendor claims against empirical evidence
    
-   Negotiate service level agreements based on measured performance
    

**Risk Assessment:**

-   Understand likely impacts in intended deployment context
    
-   Translate AI capabilities to business/operational risk
    
-   Inform risk management and mitigation strategies
    
-   Support informed go/no-go decisions
    

**Governance and Compliance:**

-   Demonstrate responsible AI procurement practices
    
-   Document due diligence for regulators and stakeholders
    
-   Align with organizational AI governance frameworks
    
-   Support accountability requirements
    

## For Regulators and Policymakers

**Standards Development:**

-   Evidence base for AI safety standards
    
-   Benchmark methodologies for regulatory requirements
    
-   Reference implementations for compliance frameworks
    
-   International harmonization of evaluation approaches
    

**Policy Formulation:**

-   Empirical grounding for AI regulations
    
-   Understanding of realistic risk levels and mitigation effectiveness
    
-   Assessment of industry capability and readiness
    
-   Cost-benefit analysis of regulatory interventions
    

**Monitoring and Enforcement:**

-   Evaluation protocols for regulatory audits
    
-   Baseline for acceptable performance levels
    
-   Detection of non-compliant systems
    
-   Evidence for enforcement actions
    

## For Researchers

**Measurement Science Advancement:**

-   Novel methodologies for sociotechnical evaluation
    
-   Validation of assessment instruments
    
-   Contributions to evaluation theory
    
-   Publication opportunities
    

**Risk Research:**

-   Empirical data on AI risk manifestation
    
-   Understanding of human-AI interaction dynamics
    
-   Investigation of mitigation effectiveness
    
-   Longitudinal studies of AI impacts
    

**Community Building:**

-   Collaborative research opportunities
    
-   Access to evaluation infrastructure
    
-   Interdisciplinary engagement
    
-   Standards development participation
    

## For End Users and Civil Society

**Informed Decisions:**

-   Understanding of AI system capabilities and limitations
    
-   Realistic expectations for AI performance
    
-   Awareness of potential risks and impacts
    
-   Empowerment in AI adoption decisions
    

**Transparency and Accountability:**

-   Visibility into AI evaluation results
    
-   Basis for demanding better systems
    
-   Evidence for advocacy efforts
    
-   Public discourse grounding
    

***

## Challenges and Considerations

## Methodological Challenges

**Scenario Design:**

-   Balancing generalizability with specificity
    
-   Creating realistic yet controlled conditions
    
-   Ensuring scenarios capture relevant risks
    
-   Avoiding scenario-specific overfitting
    

**Scalability:**

-   Resource intensity of human-in-the-loop evaluation
    
-   Cost of multi-tier testing at scale
    
-   Annotation workload for large evaluations
    
-   Training requirements for assessors
    

**Measurement Validity:**

-   Ensuring CoRIx captures true contextual robustness
    
-   Validating that scenarios proxy real-world risks
    
-   Addressing construct validity concerns
    
-   Managing measurement noise and variability
    

## Scope Limitations

**Coverage Gaps:**

-   ARIA 0.1 focused narrowly on validity/reliability
    
-   Long-term impacts (dependency, displacement) underexplored
    
-   Structural and systemic harms may be missed
    
-   Limited to scenarios amenable to controlled testing
    

**Technology Scope:**

-   Initial focus on LLMs excludes other AI types
    
-   Text-based interfaces don't cover multimodal systems
    
-   Generative AI emphasis may not generalize to all AI
    

**Risk Construct:**

-   Treating validity as primary risk may oversimplify
    
-   Tension between measurable risks and important harms
    
-   Some impacts difficult to capture in short-term testing
    

## Practical Constraints

**Resource Requirements:**

-   Significant investment in infrastructure
    
-   Specialized expertise for assessment and analysis
    
-   Time-intensive evaluation process
    
-   Costs may limit accessibility for smaller organizations
    

**Participation Barriers:**

-   Technical requirements for API implementation
    
-   Need for NIST-credentialed access
    
-   Compliance burden for participants
    
-   Potential competitive concerns about disclosure
    

**Interpretation Challenges:**

-   Complexity of multi-dimensional CoRIx scores
    
-   Need for context to interpret results meaningfully
    
-   Potential for misuse or oversimplification
    
-   Communication challenges to diverse stakeholders
    

## Evolving AI Landscape

**Rapid Technology Change:**

-   Evaluation methods risk obsolescence
    
-   New AI capabilities may require new scenarios
    
-   Emerging risks not anticipated in current design
    
-   Need for continuous methodology evolution
    

**Diverse AI Systems:**

-   Growing heterogeneity of AI architectures
    
-   Increasing multimodality and complexity
    
-   Novel interaction paradigms
    
-   Difficulty maintaining technology-agnostic approach
    

***

## Future Directions

## Program Evolution

**Expanded Risk Coverage:**

-   Incorporate additional AI RMF trustworthy characteristics
    
-   Address long-term and systemic impacts
    
-   Include structural bias and fairness more deeply
    
-   Explore economic and labor market effects
    

**Technology Diversity:**

-   Text-to-image generative models
    
-   Video generation systems
    
-   Recommender systems
    
-   Decision support tools
    
-   Multimodal AI systems
    
-   Autonomous agents
    

**Scenario Library Expansion:**

-   Develop extensive library of validated proxy scenarios
    
-   Cover broader range of risks and contexts
    
-   Sector-specific scenarios for targeted evaluation
    
-   Adaptive scenario selection based on system characteristics
    

## Methodological Refinement

**CoRIx Enhancement:**

-   Expanded measurement dimensions
    
-   Refined scoring algorithms
    
-   Improved interpretability and visualization
    
-   Validation studies against real-world outcomes
    

**Assessment Techniques:**

-   Advanced annotation methodologies
    
-   Automated assessment augmentation
    
-   Reduced assessor burden while maintaining quality
    
-   Improved inter-rater reliability
    

**Testing Protocols:**

-   Optimized scenario design
    
-   Enhanced red teaming techniques
    
-   Improved field testing representativeness
    
-   Integration of continuous evaluation approaches
    

## Community and Ecosystem

**Broader Participation:**

-   Lower barriers to entry for diverse developers
    
-   International expansion beyond U.S. focus
    
-   Small and medium enterprise engagement
    
-   Academic and non-profit inclusion
    

**Open Science:**

-   Public datasets from evaluations (privacy-preserving)
    
-   Open-source evaluation tools and instruments
    
-   Transparent methodology documentation
    
-   Reproducible research practices
    

**Standards Alignment:**

-   Integration with international AI standards (ISO, IEC)
    
-   Harmonization with EU AI Act requirements
    
-   Compatibility with sector-specific regulations
    
-   Contribution to global AI governance frameworks
    

## Operational Scaling

**Continuous Evaluation:**

-   Move from discrete evaluations to ongoing monitoring
    
-   Real-time risk detection capabilities
    
-   Longitudinal tracking of deployed systems
    
-   Feedback loops for system improvement
    

**Automation:**

-   Increased automation where appropriate
    
-   AI-assisted assessment and annotation
    
-   Scalable infrastructure for high-volume testing
    
-   Maintaining human oversight for critical judgments
    

**Service Models:**

-   Evaluation-as-a-service offerings
    
-   Self-service tools for organizations
    
-   Tiered evaluation options (comprehensive vs. targeted)
    
-   Integration with AI development pipelines
    

***

## Resources and Documentation

## Official NIST Publications

**Primary Documents:**

-   **NIST AI 700-2:** Assessing Risks and Impacts of AI (ARIA): Pilot Evaluation Report (November 2025)
    
-   **ARIA Evaluation Design Document:** Detailed methodology and program structure
    
-   **ARIA Program Overview:** High-level introduction to goals and approach
    
-   **ARIA Program Companion Document:** Supporting materials and guidance (December 2024)
    

**Related NIST AI Publications:**

-   **NIST AI RMF 1.0:** AI Risk Management Framework (January 2023)
    
-   **NIST AI 600-1:** Generative Artificial Intelligence Profile
    
-   **NIST AI RMF Playbook:** Implementation guidance for organizations
    

## Online Resources

**Official Websites:**

-   **NIST ARIA Program:** [https://www.nist.gov/programs-projects/assessing-risks-and-impacts-ai-aria](https://www.nist.gov/programs-projects/assessing-risks-and-impacts-ai-aria)
    
-   **ARIA Challenges Portal:** [https://ai-challenges.nist.gov/aria](https://ai-challenges.nist.gov/aria)
    
-   **ARIA Documentation Repository:** Technical specifications, API documentation, evaluation plans
    

**ARIA Email Distribution List:**

-   Join for important program news and announcements
    
-   Updates on upcoming evaluations and workshops
    
-   Community engagement opportunities
    

## Workshops and Events

**ARIA Workshops:**

-   Workshop 1 (November 12, 2024): Program kickoff and community introduction
    
-   Ongoing workshops for methodology refinement
    
-   Annotation training sessions
    
-   Developer engagement events
    

**Related Conferences:**

-   CAMLIS (Conference on Applied Machine Learning for Information Security)
    
-   NIST AI workshops and symposia
    
-   International AI evaluation conferences
    

## Contact and Engagement

**Program Leadership:**

-   **Reva Schwartz:** ARIA Program Lead, NIST Information Technology Laboratory
    

**Participation Opportunities:**

-   Technology developer submissions
    
-   Red teaming participation
    
-   Field testing engagement
    
-   Research collaboration
    
-   Standards development contribution
    

***

## Key Quotes from NIST Leadership

**U.S. Commerce Secretary Gina Raimondo:**

> "In order to fully understand the impacts AI is having and will have on our society, we need to test how AI functions in realistic scenarios — and that's exactly what we're doing with this program. With the ARIA program, and other efforts to support Commerce's responsibilities under President Biden's Executive Order on AI, NIST and the U.S. AI Safety Institute are pulling every lever when it comes to mitigating the risks and maximizing the benefits of AI."

**NIST Director Laurie E. Locascio:**

> "The ARIA program is designed to meet real-world needs as the use of AI technology grows. This new effort will support the U.S. AI Safety Institute, expand NIST's already broad engagement with the research community, and help establish reliable methods for testing and evaluating AI's functionality in the real world."

**ARIA Program Lead Reva Schwartz:**

> "Measuring impacts is about more than how well a model functions in a laboratory setting. ARIA will consider AI beyond the model and assess systems in context, including what happens when people interact with AI technology in realistic settings under regular use. This gives a broader, more holistic view of the net effects of these technologies."

**NIST Information Access Division Chief Mark Przybocki:**

> "AI systems are extremely complex, and a single number to characterize the level of performance is often insufficient... By incorporating human testers into AI evaluation, red‑teaming and field testing can help to reveal positive and negative impacts that are not known ahead of time or that relate to AI use in its operating environment."

> "ARIA seeks to improve AI evaluation by accounting for these varied contexts via realistic scenarios and multiple testers."

***

## Summary: Why ARIA Matters

NIST ARIA represents a fundamental shift in how AI systems are evaluated—from static benchmark scores to dynamic assessment of real-world performance with actual users. By observing materialized risks across model testing, red teaming, and field testing, ARIA provides empirical evidence about AI behavior in realistic deployment contexts.

The program's innovations—particularly the Contextual Robustness Index (CoRIx) and three-tier testing methodology—offer practical tools for organizations to evaluate AI systems before procurement or deployment. ARIA operationalizes the NIST AI Risk Management Framework, translating conceptual guidance into measurable evaluation procedures.

As AI systems become more prevalent across society, ARIA's sociotechnical approach ensures that safety, reliability, and trustworthiness are evaluated not just in the laboratory but in the contexts where AI will actually be used. The program provides essential infrastructure for the U.S. AI Safety Institute and contributes to the global effort to develop trustworthy AI systems.

ARIA's sector-agnostic design, commitment to transparency, and community-driven refinement position it to evolve with the AI landscape, continuously improving measurement science for emerging technologies and risks. For developers, procurers, regulators, and users, ARIA offers a path toward more informed, evidence-based decisions about AI systems that increasingly shape our world.

***

**Document Version:** March 2026  
**Last Updated:** Based on information through ARIA 0.1 Pilot Report release (November 2025) and program developments through early 2026  
**Authoritative Source:** National Institute of Standards and Technology (NIST)  
**Official Website:** [https://ai-challenges.nist.gov/aria](https://ai-challenges.nist.gov/aria)