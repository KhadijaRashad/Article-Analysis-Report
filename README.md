# Article-Analysis-Report
Analyzed article: Turk, S., &amp; Coskuncay, A. (2026). A systematic and evolutionary analysis of software design pattern detection and recommendation approaches (2015–2025). Information and Software Technology, 199, 108290. 


1. Introduction and Article Selection
For this assignment I selected a recent review article published in Information and Software Technology, a journal indexed in the Web of Science (SCIE). The article is a systematic literature review (SLR) of how software design patterns have been automatically detected and recommended over the last decade. I chose it for three reasons. First, design patterns are one of the most direct bridges between theory and practice in object-oriented programming (OOP): every pattern in the Gang of Four (GoF) catalogue is an idiom built from classes, interfaces, inheritance, composition and polymorphism. Second, the article covers the full arc from rule-based and graph-based techniques to deep learning and large language models (LLMs), so it shows how a classical software engineering problem has been re-framed by each new generation of tools. Third, because it is a review, it points to many primary studies that I can examine and compare, which the assignment requires.
This report follows the structure requested in the assignment: the core subject and research questions (Section 2), the methods used (Section 3), an evaluation of the findings (Section 4), the link to OOP concepts (Section 5), a summary of the field's development based on key primary references (Section 6), my own interpretation and improvement suggestions (Section 7), and the bibliography (Section 9).
2. Core Subject, Objective and Research Questions
2.1 Core subject
The article addresses the automated analysis of design patterns in two directions:
• Detection (reverse engineering): given existing artifacts such as source code or UML models, find which classes play which roles in which pattern. Detection is artifact-driven and structurally grounded.
• Recommendation (forward engineering): given a textual requirement or design problem, suggest an appropriate pattern. Recommendation is problem-driven and semantically grounded.
2.2 Objective
The authors state that their aim is to provide a systematic and evolutionary synthesis of approaches published between 2015 and 2025, to classify them into technological paradigms, and to identify open research challenges. They claim novelty in presenting the first multi-paradigm, evolutionary integration for this period, whereas earlier surveys usually focused on a single family of methods (for example only graph-based or only ML-based detection).
2.3 Research questions
RQ
Question (paraphrased)
RQ1
How did detection and recommendation approaches evolve between 2015 and 2025?
RQ2
How do the paradigms compare in performance, scalability, pattern coverage and variant detection?
RQ3
Which datasets, languages and evaluation protocols are used, and how do they affect generalizability?
RQ4
What open challenges remain and which future directions can address them?
The questions are well chosen: RQ1 is descriptive, RQ2 is comparative, RQ3 is a meta-research question about evidence quality, and RQ4 is prescriptive. Together they move from what happened to how good is the evidence to what should happen next.
3. Methods and Technological Approaches
3.1 Review method
The authors follow Kitchenham and Charters' evidence-based software engineering guidelines and PRISMA principles. A protocol was defined before screening. The process was:
1. Identification: a Web of Science query combining three keyword sets (A: design pattern, GoF; B: software, source code, UML, graph, static or dynamic analysis, refactoring; C: detection, identification, recognition, classification, recommendation, pattern role, micro-architecture), restricted to peer-reviewed English journal and conference papers from 2015–2025. This returned 212 records.
2. 1. Screening: 126 records were excluded on title and abstract (unrelated fields, keyword collisions such as GoF meaning Goodness of Fit or Gain of Function, theoretical-only papers, secondary studies, short papers).
2. Eligibility: 86 full texts were assessed, and 20 were excluded (6 not an automated method, 5 without empirical validation, 9 out of scope).
3. Inclusion: 66 primary studies were synthesized.
4. 1. Inclusion: 66 primary studies were synthesized.
Quality was assessed with five criteria (clarity of method, transparency of setup, adequacy of metrics, dataset reporting, discussion of threats), each scored Yes (1), Partly (0.5) or No (0), by two independent reviewers. Agreement was reported as Cohen's kappa = 0.82. Because the studies are heterogeneous, no statistical meta-analysis was attempted; instead a qualitative, normalized, evidence-based coding was used.
4. Evaluation of the Findings
4.1 Main findings reported
RQ1 (evolution). The field moved from structure to semantics: from exact template matching, to probabilistic classification, to learned representations, to contextual reasoning with LLMs. Detection and recommendation, previously separate, begin to converge in LLM-based work. The yearly heat map (Fig. 4) shows machine learning peaking in 2017–2019 and 2022, graph-based studies disappearing after 2019, and LLM-based studies appearing only from 2023 (2, 1 and 4 studies in 2023, 2024 and 2025).
RQ2 (comparison). No paradigm dominates. Graph-based and rule-based methods are the most explainable (mean 1.000 and 0.958) and tend to have high precision but lower recall on non-canonical implementations. Deep learning has the highest performance evidence score (0.900), hybrid approaches the most balanced profile (scalability evidence 0.833, variant detection 0.833), graph-based the highest pattern coverage (0.531), and machine learning the weakest variant detection (0.273). LLM-based studies show moderate variant detection (0.571) but weak scalability reporting (0.429) and the lowest explainability (0.500).
