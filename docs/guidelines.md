# Research Paper Plan & Draft Content

**Title (working):** The Pedagogical Potential of AI-Generated Visual Explanations for Learners with Low Language Proficiency or Learning Disabilities: A Systematic Review

**Target length:** ~7,000 words
**Citation style:** APA 7th edition (in-text + reference list)
**Document type:** Systematic literature review

---

## Instructions for Claude Code (LaTeX Conversion)

1. **Document class:** Use the university template already present in the working directory. Do not create a new preamble — extend the existing one.
2. **Required packages (verify in template, add if missing):** `inputenc`, `fontenc`, `babel`, `geometry`, `setspace`, `csquotes`, `hyperref`, `apacite` *or* `biblatex` with `style=apa` (prefer `biblatex` + `biber` for cleaner APA 7).
3. **Sectioning:** Use `\section{}` for the five top-level sections; `\subsection{}` for thematic divisions inside Literature Review and Findings.
4. **Citations:** All in-text references should be `\parencite{key}` or `\textcite{key}` (biblatex) or `\cite{key}` (apacite). I supply BibTeX keys in §References; generate a `references.bib` file with the 10 entries.
5. **Abstract:** Place inside `\begin{abstract}...\end{abstract}` if the template defines it. Keyword line follows the abstract: `\textit{Keywords:} ...`.
6. **Spacing:** 1.5 line spacing for body text (`\onehalfspacing`), single for abstract and references unless template specifies otherwise.
7. **Tables:** The Findings section includes one table (Table 1: Summary of Reviewed Studies). Use `booktabs` (`\toprule`, `\midrule`, `\bottomrule`). Place with `[H]` (requires `float` package) or `[htbp]`.
8. **Figures:** One PRISMA-style flow diagram is referenced in Methodology. If TikZ is available, draw it inline; otherwise leave a `\todo{insert PRISMA diagram}` marker.
9. **No bullet lists in body prose** — convert any bullet content in this plan into flowing paragraphs unless explicitly marked as a list.
10. **Word counts** below each section are targets; the prose I provide is roughly that length already, so expand rather than compress.

---

## Abstract (~250 words — single paragraph)

> **Draft:**
>
> The rapid maturation of generative artificial intelligence, and particularly of multimodal large language models capable of producing images, diagrams, and animated explanations on demand, has opened a new frontier in inclusive pedagogy. For learners with low language proficiency and for those with learning disabilities, the dependence of conventional instruction on dense text has long been a source of avoidable extraneous cognitive load. This systematic review synthesises ten recent empirical and theoretical studies, published between 2024 and 2025, that examine how AI-generated visual explanations function as a pedagogical resource for these populations. Drawing on the Cognitive Theory of Multimedia Learning and Cognitive Load Theory as analytic anchors, the review classifies the studies into four thematic clusters: AI tool typologies, theory–practice alignment, pedagogical efficacy, and implementation barriers. Findings indicate that AI-generated visual explanations are most effective when their design reflects established multimedia principles — particularly the modality, signalling, and coherence principles — and when they are embedded within scaffolded, learner-active tasks rather than offered as passive supplements. Evidence of efficacy is strongest for vocabulary learning, reading comprehension, and conceptual scaffolding in STEM, with reported gains of up to thirty per cent in some hybrid implementations. The review also identifies persistent gaps: a narrow disability focus on dyslexia and autism spectrum disorder, limited longitudinal data, and underdeveloped frameworks for managing AI hallucination and algorithmic bias in visual outputs. The paper concludes by proposing a research agenda that foregrounds adaptive load management, learner-controlled visual generation, and culturally responsive design.
>
> **Keywords:** artificial intelligence; visual explanations; multimedia learning; cognitive load theory; learning disabilities; language proficiency; inclusive education; generative AI

---

## 1. Introduction (~900 words)

**Purpose of section:** Frame the problem, situate the topic in current debates, introduce the theoretical lens, state research questions, and preview the paper.

**Structure:** Five paragraphs.

### Paragraph 1 — Hook & contemporary relevance (~180 words)

> The classroom of 2026 is multilingual, neurodiverse, and increasingly mediated by artificial intelligence. In a single lecture hall, an instructor may simultaneously address learners who are still acquiring the language of instruction, learners with diagnosed conditions such as dyslexia or attention-deficit/hyperactivity disorder, and learners whose only difficulty is the unevenness of prior schooling. For each of these students, a textbook paragraph or a verbal explanation imposes a cognitive cost that is not necessarily related to the material itself but to the linguistic packaging of that material. The pedagogical problem is therefore not what is taught, but how it is encoded for transmission. Generative artificial intelligence, and especially the recent generation of multimodal large language models capable of producing diagrams, illustrations, and short animations from natural-language prompts, offers a route around this bottleneck. Rather than asking learners to convert text into mental images on their own — a task that is itself language-dependent — the technology can supply the visual representation directly, at the right level of abstraction, and within seconds.

### Paragraph 2 — Background on AI in education (~190 words)

> The emergence of tools such as GPT-4 Vision, DALL·E 3, and Gemini has shifted the conversation about AI in education away from text-only chatbots and towards multimodal systems that read, write, see, and draw. Bewersdorff et al. (2024) characterise this as a "next step" in generative AI, in which the same model can interpret a hand-drawn student diagram and respond with both a corrected diagram and a level-appropriate textual explanation. Earlier waves of educational technology — intelligent tutoring systems, adaptive testing platforms, screen readers — addressed accessibility one channel at a time. Multimodal AI collapses these channels into a single interface and, crucially, makes visual content production cheap enough to be personalised. A teacher who would once have spent hours preparing differentiated worksheets can now generate a learner-specific diagram during the lesson itself. The pedagogical implications are significant for any student who benefits from non-verbal scaffolding, but they are particularly consequential for learners with low language proficiency and for learners with disabilities, two groups for whom the gap between cognitive capability and linguistic access is often the primary barrier to achievement.

### Paragraph 3 — The cognitive case (~160 words)

> The case for visual explanations is not new. Mayer's Cognitive Theory of Multimedia Learning (CTML) and Sweller's Cognitive Load Theory (CLT), both of which have been refined for over three decades, establish that learners process information through partially independent verbal and visual channels and that learning is optimised when extraneous load is minimised and germane load is maximised. What is new is the scale and immediacy with which AI can deliver visual material that respects these principles. Twabu and Modise (2025) argue that traditional CTML and CLT, although foundational, were articulated in an era of static multimedia and require extension to accommodate the adaptive, learner-responsive behaviour of AI systems. Their proposed AI-augmented framework is one of several recent attempts to bring multimedia learning theory up to date with the technological reality of generative models.

### Paragraph 4 — Research gap and questions (~200 words)

> Despite a rapidly expanding literature on AI in education, work that specifically interrogates the pedagogical potential of AI-*generated* visual explanations for learners with low language proficiency or learning disabilities remains scattered across systematic reviews of special education technology, theoretical papers on multimodal AI, and empirical studies of individual tools. No synthesis to date has brought these strands together under a single analytic frame. The present review addresses that gap by examining ten studies published between 2024 and 2025 in light of the following research questions:
>
> - **RQ1.** What categories of AI-generated visual explanations have been documented in recent pedagogical research relevant to learners with low language proficiency or learning disabilities?
> - **RQ2.** How do these tools and approaches align with the principles of CTML and CLT?
> - **RQ3.** What evidence exists for their pedagogical efficacy with the target learner populations?
> - **RQ4.** What limitations and unresolved questions does the current literature reveal, and what should future research prioritise?

### Paragraph 5 — Significance and structure (~170 words)

> The significance of this review is threefold. First, it consolidates a fragmented evidence base at a moment when generative AI is being adopted in classrooms faster than the research can evaluate. Second, it offers educators, instructional designers, and policymakers a theoretically grounded basis for decisions about which AI tools to introduce, for whom, and under what conditions. Third, by foregrounding learners with low language proficiency alongside learners with disabilities, it resists the tendency of the field to treat these populations as separate, when in practice they share the same underlying need for non-verbal scaffolding. The remainder of the paper is organised as follows. Section 2 reviews the relevant literature on multimedia learning theory, AI applications for diverse learners, and visual generation in educational contexts. Section 3 sets out the systematic review methodology. Section 4 presents the thematic findings. Section 5 discusses theoretical and practical implications, acknowledges limitations, and proposes directions for future inquiry.

---

## 2. Literature Review (~2,000 words)

**Purpose of section:** Establish the conceptual and empirical context. Organise thematically (not chronologically). Conclude by identifying the gap that motivates the systematic review.

**Subsections:**

### 2.1 Theoretical Foundations: CTML and CLT (~450 words)

> The Cognitive Theory of Multimedia Learning, developed by Richard Mayer over three decades, posits that meaningful learning occurs when learners actively integrate verbal and visual representations of the same content into coherent mental models. The theory rests on three assumptions inherited from cognitive psychology: the dual-channel assumption, that humans process auditory-verbal and visual-pictorial information through distinct channels; the limited-capacity assumption, that each channel can hold only a small number of elements at once; and the active-processing assumption, that learning requires deliberate cognitive effort to select, organise, and integrate information. From these assumptions Mayer derives a set of design principles — the modality, redundancy, signalling, contiguity, coherence, and personalisation principles, among others — that have been replicated across hundreds of experimental studies.
>
> Cognitive Load Theory, articulated by John Sweller and colleagues, offers a complementary lens. CLT distinguishes intrinsic load (the inherent complexity of the material), extraneous load (the load imposed by the manner of presentation), and germane load (the load associated with the construction of schemas in long-term memory). Effective instruction minimises extraneous load and channels working-memory resources towards germane load. For learners with low language proficiency or with disabilities such as dyslexia, the linguistic surface of textual material constitutes a significant source of extraneous load: the cognitive cost of decoding language competes with the cognitive resources available for understanding the content itself.
>
> The intersection of CTML and CLT yields a clear prediction: substituting or supplementing textual explanations with well-designed visual explanations should reduce extraneous load and free working memory for schema construction. Lawson and Mayer (2024) provide recent experimental support for the active-processing component of this prediction, finding that summarising during multimedia animations improved learning outcomes while passive viewing did not, suggesting that the visual channel alone is insufficient unless paired with cognitive engagement.
>
> Twabu and Modise (2025) propose an extension of these frameworks for the AI era. Their model introduces three additions: AI-mediated schema creation, in which a generative system scaffolds the learner's transition from novice to expert representations; adaptive cognitive load management, in which AI dynamically calibrates the complexity of the visual representation to the learner's measured load; and human–AI collaborative learning, in which the learner and the system iteratively refine a representation. The framework remains conceptual rather than empirically validated, but it offers a vocabulary for analysing AI-generated visual explanations as theoretically motivated rather than merely technologically convenient.

### 2.2 AI Applications for Learners with Disabilities (~500 words)

> Panjwani-Charani and Zhai (2024) provide the most comprehensive recent map of AI applications for students with learning disabilities, identifying seven categories across sixteen empirical studies: adaptive learning systems, facial expression recognition, chat robots, communication assistants, mastery learning environments, intelligent tutors, and interactive robots. Their analysis reveals two patterns of immediate relevance to the present review. First, adaptive learning systems dominate the empirical literature, while AI tools that produce or manipulate visual representations are relatively scarce. Second, the disability focus is heavily skewed: ten of the sixteen studies addressed dyslexia, with autism spectrum disorder a distant second and dyscalculia represented by only a single study. The authors classify the level of integration using the SAMR-LD model — Substitution, Augmentation, Modification, Redefinition for learning disabilities — and find that AI applications occupy all four levels, although the highest level (Redefinition, in which AI enables tasks otherwise impossible) remains rare.
>
> Drosos et al. (2025) extend this picture by reviewing 139 studies on AI, virtual reality, and large language models in special education. Their thematic analysis surfaces several application clusters of direct relevance: multimodal conversational systems for non-verbal communication, AI-generated images for augmentative and alternative communication, individualised educational support for children with developmental disorders, and VR-based social skills training. The authors document a clear historical shift from earlier assistive technologies, which substituted for impaired functions (text-to-speech, screen reading), towards generative AI tools, which produce new representational content tailored to the learner. This shift is consequential because it changes the question from "how can the learner access the existing material?" to "what material best fits this learner?"
>
> A particularly important strand of this literature concerns autism spectrum disorder. Urrea et al. (2024) systematically review thirteen studies of technology-assisted vocabulary learning for children with ASD, including tablet applications, video modelling, computer-assisted instruction, and augmented reality. They report that visual systems such as the Picture Exchange Communication System remain a strong baseline, and that technology adds value primarily when it integrates structured visual scaffolding with explicit instruction. Khoirunnisa et al. (2024) describe a complementary AR system for reading skills in ASD learners, in which visual overlays adapt to individual learner profiles. While neither study uses generative AI as such, both establish the population-level evidence base on which AI-generated visual explanations can build.
>
> Bühler et al. (2024) approach the same population from a different angle, conducting semi-structured interviews with students with disabilities in higher education about their use of generative AI. The participants — many with ADHD, dyslexia, dyspraxia, or autism — reported that ChatGPT and similar tools helped them structure ideas, overcome writer's block, and convert dense academic content into more accessible formats. Concerns centred on AI inaccuracy, academic integrity, and the cost of subscription tiers. The study is notable because it documents that learners themselves perceive generative AI as an assistive technology, validating the premise of the present review from the user side.

### 2.3 Multimodal AI and Visual Generation in Education (~500 words)

> The technical capability that distinguishes the current moment from earlier waves of educational AI is multimodality. Bewersdorff et al. (2024) develop the most explicit theoretical treatment of multimodal large language models in education, arguing that MLLMs change three things at once: they can interpret learner inputs in any modality, they can produce explanations in any modality, and they can move between modalities within a single interaction. The authors illustrate this with several scenarios drawn from science education: a diagram of a chemical reaction is augmented with a textual explanation calibrated to the student's reading level; a student's hand-drawn sketch of cellular respiration is corrected and re-rendered as a clean diagram; a multimodal assessment combines a generated image with a written prompt. Crucially, Bewersdorff et al. ground each scenario in CTML, showing that the design choices follow directly from established multimedia principles rather than from technological novelty.
>
> Osman et al. (2024) operationalise a similar approach in the form of an AI educational video assistant for higher education. Their tool comprises three modules: a Transcription Module that converts lecture audio to text using OpenAI Whisper, an Engagement Module that uses a large language model to support interactive question-and-answer, and a Reinforcement Module for spaced review. Each module is mapped explicitly to specific CTML principles. The Transcription Module supports the modality principle by allowing learners to switch between auditory and textual representations. The Engagement Module supports the personalisation principle by responding in conversational language. The Reinforcement Module supports the spaced-practice principle. Both human evaluators and automated metrics confirmed gains in learning outcomes, although the study did not specifically isolate effects for learners with disabilities or low language proficiency.
>
> A complementary line of work examines the conditions under which visual content actually produces learning. Lawson and Mayer (2024) conducted an experimental study in which students viewed annotated animations about greenhouse gases and were asked to summarise, draw, or simply watch. Summarising produced significant learning gains; drawing did not. The result is a useful corrective to a naive enthusiasm for visual content: a generated diagram, however accurate, does not produce learning if the learner is a passive consumer of it. The pedagogical value of AI-generated visual explanations therefore depends on the activity structure that surrounds them.
>
> Ahmad et al. (2025) bring these strands together in a review that explicitly addresses the dual challenge of disability support and language barriers. They document AI-driven adaptive learning systems, intelligent tutoring platforms such as ALEKS and Q-interactive, NLP-based text simplification, bilingual glossary generation, and assistive technologies including text-to-speech, closed captioning, and image recognition. Their headline empirical finding — that AI-enabled hybrid learning models have produced improvements of up to twenty-five per cent in vocabulary learning and thirty per cent in reading comprehension in certain contexts — provides the strongest available evidence for the population of interest, although the authors caution that effects are highly context-dependent and that ethical concerns about bias and privacy remain unresolved.

### 2.4 Identified Gap (~250 words)

> Three observations emerge from this body of work. First, the theoretical apparatus exists: CTML and CLT, with the recent extensions proposed by Twabu and Modise, provide a coherent vocabulary for analysing AI-generated visual explanations. Second, the empirical literature on AI in special education and on multimodal AI in mainstream education is growing rapidly, but the two literatures rarely meet. Studies of AI for learners with disabilities tend to describe assistive applications without engaging multimedia learning theory; studies of multimodal AI in education tend to describe theoretically grounded applications without examining differential effects for learners with low language proficiency or disabilities. Third, where the two literatures do meet — for example in Ahmad et al. (2025) and Drosos et al. (2025) — the treatment is broad rather than focused, surveying many tools without close examination of how visual generation specifically supports the populations of interest.
>
> The gap is therefore not an absence of research but a lack of integration. A systematic review oriented specifically to AI-generated visual explanations, framed by CTML and CLT, and focused on learners with low language proficiency or learning disabilities, would synthesise what is currently known, expose the conditions under which the technology supports learning, and identify which questions remain open. The methodology adopted to address this gap is set out in the next section.

### 2.5 [Optional] Brief positioning paragraph (~100 words, only if word count tight)

> This review positions itself at the intersection of three established literatures rather than within any one of them. It treats CTML and CLT as the analytic frame, AI-generated visual explanations as the technological object, and learners with low language proficiency or learning disabilities as the population of interest. The contribution is integrative: each of the three components has been studied separately, and partial intersections exist, but no recent synthesis has held all three in view simultaneously.

---

## 3. Methodology (~1,100 words)

**Purpose of section:** Make the review reproducible. Use a PRISMA-inspired structure. Be explicit about decisions.

### 3.1 Research Design (~150 words)

> This study employs a systematic literature review methodology to synthesise current knowledge on AI-generated visual explanations as a pedagogical tool for learners with low language proficiency or learning disabilities. A systematic review is appropriate because the field is fragmented across multiple sub-disciplines — educational technology, special education, cognitive psychology, and human–computer interaction — and because the rapid pace of development in generative AI requires periodic consolidation of evidence. The review follows the principles of the Preferred Reporting Items for Systematic Reviews and Meta-Analyses (PRISMA) statement, with adaptations appropriate to a primarily qualitative thematic synthesis. Specifically, the review uses PRISMA's four-phase approach (identification, screening, eligibility, inclusion) for source selection, but uses thematic analysis rather than meta-analytic statistical pooling for synthesis, given the heterogeneity of the included studies in design, population, and outcome measures.

### 3.2 Search Strategy (~200 words)

> The search was conducted between September and December 2025 across five academic databases selected for their coverage of education, psychology, and information science: Scopus, Web of Science, ERIC, IEEE Xplore, and Google Scholar. The search strategy combined three concept blocks using Boolean operators. Block A targeted the technology: "generative AI" OR "large language model" OR "multimodal AI" OR "AI-generated image" OR "visual generation". Block B targeted the pedagogical context: "education" OR "learning" OR "instruction" OR "pedagogy" OR "multimedia learning". Block C targeted the population: "learning disabilit*" OR "language proficiency" OR "English language learner" OR "special education" OR "dyslexia" OR "autism" OR "ADHD". The three blocks were combined as A AND B AND C, with database-specific syntax adjustments. The search was limited to peer-reviewed journal articles, edited book chapters from academic publishers, and conference proceedings from established venues. Date limits were 2023–2025, reflecting the post-GPT-4 era of multimodal generative AI. The search was conducted in English, which constitutes a limitation acknowledged in §5.

### 3.3 Inclusion and Exclusion Criteria (~200 words)

> Studies were included if they met all of the following criteria. First, the study addressed AI tools capable of generating, manipulating, or contextualising visual content, defined broadly to include diagrams, illustrations, animations, augmented reality overlays, and image-based augmentative communication. Second, the study addressed an educational context, including formal schooling, higher education, and structured non-formal learning. Third, the study either explicitly addressed learners with low language proficiency or learning disabilities, or its findings were directly transferable to those populations as evidenced by the use of relevant theoretical frameworks (CTML, CLT, universal design for learning). Fourth, the study reported either empirical findings, a systematic synthesis of empirical findings, or a theoretically grounded framework with explicit pedagogical implications.
>
> Studies were excluded if they: addressed AI in education without any visual or multimodal component (for example, text-only chatbot studies); addressed visual technology in education without an AI component (for example, conventional video learning); were limited to technical descriptions of AI systems without pedagogical analysis; were published in non-peer-reviewed venues; or were not available in English. Opinion pieces, editorials, and short commentaries were also excluded.

### 3.4 Selection Process (~150 words)

> The initial database search returned approximately 340 records. After duplicate removal across databases, 287 unique records remained. Title and abstract screening reduced this to 42 records assessed for full-text eligibility. Full-text review excluded 32 records, primarily because they addressed AI in education without a visual generation component (n = 18), addressed visual learning without AI (n = 7), or were not directly relevant to the target populations (n = 7). The final corpus comprised ten studies, listed in the references and summarised in Table 1 (Findings section). The selection process is summarised in the PRISMA flow diagram presented as Figure 1.
>
> *(Claude Code: insert PRISMA-style figure here. If TikZ is available, draw the four boxes — Identification, Screening, Eligibility, Inclusion — with the numbers above; otherwise insert a placeholder `\todo{PRISMA flow diagram: 340 → 287 → 42 → 10}`.)*

### 3.5 Data Extraction (~150 words)

> A structured data extraction form was developed to ensure consistent treatment of each included study. The form captured: bibliographic information (authors, year, journal); study type (systematic review, empirical study, theoretical framework, qualitative study); target population (specific disability or language-proficiency profile, age group, educational level); AI tool or application examined; visual modality involved (static image, diagram, animation, AR, multimodal); theoretical framework cited; methodology; key findings; and reported limitations. Extraction was conducted by the author and entered into a single spreadsheet, with each row representing one study. For studies that were themselves systematic reviews, the extraction recorded summary-level findings rather than re-extracting from primary sources, in order to avoid double-counting.

### 3.6 Synthesis Approach (~150 words)

> Synthesis followed Braun and Clarke's six-phase thematic analysis procedure, adapted for documentary rather than interview data. After familiarisation with each study, initial codes were generated inductively from the extracted data, with attention both to manifest content (what the studies reported) and latent content (theoretical assumptions, recurring concerns). Codes were then collated into candidate themes, which were reviewed against the full dataset to ensure internal coherence and external distinctiveness. Four themes were finalised: (i) typology of AI-generated visual explanations; (ii) alignment with multimedia learning theory; (iii) evidence of pedagogical efficacy; and (iv) implementation barriers and ethical concerns. Each theme is presented in §4 with supporting evidence from the included studies.

### 3.7 Quality and Limitations (~100 words)

> Quality appraisal followed the criteria appropriate to each study type: systematic reviews were appraised against AMSTAR-2 criteria, empirical studies against the Mixed Methods Appraisal Tool, and theoretical papers against criteria for conceptual rigour and engagement with prior literature. All ten included studies met the threshold for inclusion. The principal limitations of the review — language restriction, narrow date range, single-author extraction — are acknowledged in §5. The methodological choices made here represent a balance between systematic rigour and feasibility within the scope of a single-author review.

---

## 4. Findings and Analysis (~2,000 words)

**Purpose of section:** Present the four thematic findings with evidence from the corpus. Lead with a summary table.

### 4.0 Overview and Table 1 (~150 words)

> This section presents the findings of the thematic synthesis organised around the four themes identified in §3.6. Table 1 provides a summary of the ten included studies, indicating their type, theoretical orientation, target population, and primary contribution. The thematic discussion that follows draws on these studies in combination, integrating their findings rather than summarising each in turn.

**Table 1 specification (use `booktabs`, columns: # | Author(s) (Year) | Type | Population focus | Primary contribution):**

| # | Authors (Year) | Type | Population | Primary contribution |
|---|---|---|---|---|
| 1 | Panjwani-Charani & Zhai (2024) | Systematic review | Learning disabilities | Typology of seven AI applications for SWLDs |
| 2 | Bewersdorff et al. (2024) | Theoretical framework | General + science ed | MLLM framework grounded in CTML |
| 3 | Osman et al. (2024) | Empirical (design + eval) | Higher ed learners | CTML-aligned video assistant tool |
| 4 | Ahmad et al. (2025) | Review | Disability + ELL | Quantified gains; ethics framework |
| 5 | Lawson & Mayer (2024) | Experimental | General learners | Generative activities + visual learning |
| 6 | Drosos et al. (2025) | Systematic review (n=139) | Special education broad | Landscape map of AI/VR/LLM in SE |
| 7 | Bühler et al. (2024) | Qualitative interview | HE students with disabilities | Learner perceptions of generative AI |
| 8 | Urrea et al. (2024) | Systematic review (n=13) | Children with ASD | Tech-assisted vocabulary evidence |
| 9 | Twabu & Modise (2025) | Theoretical | ODL/distance learners | AI-augmented CTML/CLT framework |
| 10 | Khoirunnisa et al. (2024) | Empirical (design study) | ASD reading skills | Personalised AR for reading |

### 4.1 Theme 1: A Typology of AI-Generated Visual Explanations (~450 words)

> The first thematic finding concerns the categorisation of AI-generated visual explanations as they appear in the reviewed literature. Across the ten studies, four broad categories can be distinguished. The first comprises *generated static visuals* — diagrams, illustrations, and infographics produced by text-to-image or multimodal models in response to a learner or teacher prompt. Bewersdorff et al. (2024) treat this category as central to their framework, with examples ranging from chemical reaction diagrams to anatomical illustrations. The second category comprises *augmented or annotated visuals*, in which an AI system adds textual labels, callouts, or signalling cues to existing visual content. This category aligns directly with Mayer's signalling principle and is illustrated by Bewersdorff et al.'s scenarios in which a textbook diagram is enriched with level-appropriate explanatory text on demand. The third category comprises *adaptive multimodal sequences*, in which visual content is generated as part of a multi-step, multimodal interaction. Osman et al.'s (2024) educational video assistant exemplifies this category: visuals are not produced in isolation but are embedded within a transcription-engagement-reinforcement pipeline. The fourth category comprises *AI-mediated augmented reality*, in which visual scaffolding is overlaid on the physical or printed environment. Khoirunnisa et al. (2024) provide the clearest example, with AR overlays personalised to ASD learner profiles for reading skill development.
>
> A cross-cutting observation is that the more complex categories — adaptive sequences and AI-mediated AR — are typically associated with stronger theoretical grounding. Studies that produce isolated static visuals tend to be more technologically descriptive, whereas studies that integrate visuals into multi-step pedagogical flows tend to engage more substantively with multimedia learning theory. This pattern is consistent with Drosos et al.'s (2025) observation that the field is shifting from assistive substitution towards generative production, and that the more recent generative tools support more elaborate pedagogical designs.
>
> A second observation concerns the asymmetry between supply and demand. Panjwani-Charani and Zhai (2024) document that, among empirical studies of AI for students with learning disabilities, only a minority focus on visual or non-verbal AI applications, despite the strong theoretical case for such applications with these populations. The corpus thus suggests that AI-generated visual explanations are a comparatively underdeveloped area of research relative to AI-driven adaptive learning systems and intelligent tutoring systems, even though the populations of interest in the present review would benefit most from visual modalities. This asymmetry frames much of the discussion that follows: the technological capability exists, the theoretical justification exists, but the empirical literature has not yet caught up.

### 4.2 Theme 2: Alignment with Multimedia Learning Theory (~450 words)

> The second theme concerns the degree to which AI-generated visual explanations, as documented in the corpus, align with the principles of CTML and CLT. The strongest alignments emerge in three areas. First, the *modality principle* — that learners benefit when verbal information is presented as narration alongside visuals rather than as on-screen text — is supported by both Bewersdorff et al.'s (2024) framework and Osman et al.'s (2024) implementation, which explicitly partitions verbal information across auditory and textual channels. Second, the *signalling principle* — that learning is improved when key elements are highlighted — is operationalised in MLLM-mediated diagram annotation, where the AI system can selectively emphasise the elements relevant to a learner's current question. Third, the *coherence principle* — that extraneous material should be excluded — is at least implicit in adaptive systems that prune visual content to the learner's current level.
>
> Alignment is weaker in two areas. The *redundancy principle* — that learners should not receive identical information through multiple channels simultaneously — is at risk in many generative AI applications, where the default behaviour is to produce both an image and a textual description that essentially repeats the image's content. Bewersdorff et al. (2024) acknowledge this risk and recommend that prompt design and interface design should give the learner control over which channels are activated. The *personalisation principle*, which advocates conversational rather than formal language, is well-served by LLM-based interfaces but raises questions about register and accessibility for learners whose primary language differs from the system's default.
>
> The CLT lens reinforces but also complicates the multimedia framework. Twabu and Modise (2025) argue that the standard intrinsic-extraneous-germane partition is inadequate for AI-mediated learning, because AI systems can shift between roles — substituting for the learner's effort (reducing germane load undesirably) or scaffolding the learner's effort (channelling germane load productively). They propose adaptive cognitive load management as a fourth construct, in which AI dynamically calibrates the complexity of generated visual content to the learner's measured load. This proposal remains conceptual, but it points to a productive line of inquiry: whether AI-generated visual explanations can be designed not merely to reduce extraneous load but to actively manage germane load on a per-learner basis.
>
> Lawson and Mayer's (2024) experimental finding that drawing did not produce significant learning gains, while summarising did, has direct implications for theory–practice alignment. It suggests that an AI-generated visual is most effective when it is the *output* of a guided generative activity rather than the input to passive consumption. This finding cautions against the most enthusiastic claims for generative AI in education and aligns with the active-processing assumption at the heart of CTML.

### 4.3 Theme 3: Evidence of Pedagogical Efficacy (~500 words)

> The third theme concerns whether AI-generated visual explanations demonstrably improve learning outcomes for the target populations. The evidence base is uneven. The strongest direct quantitative claims appear in Ahmad et al. (2025), who report that AI-enabled hybrid learning models have produced improvements of up to twenty-five per cent in vocabulary learning and thirty per cent in reading comprehension in certain implementations. These figures, although attractive, must be read with caution: they are drawn from heterogeneous studies, with varying populations and outcome measures, and they represent best-case rather than typical outcomes.
>
> More targeted evidence emerges for specific populations. Urrea et al. (2024) synthesise thirteen studies on technology-assisted vocabulary learning for children with ASD and find consistent benefits for technology-mediated visual instruction, particularly when structured visual systems such as PECS are integrated with explicit instruction. Although the studies they review do not all involve AI generation as such, the underlying mechanism — visual scaffolding for non-verbal learners — extends naturally to AI-generated content. Khoirunnisa et al. (2024) report on an AR system specifically designed for ASD learners, demonstrating reading skill improvements through personalised visual overlays.
>
> For learners with low language proficiency, the evidence base is thinner. Ahmad et al. (2025) discuss NLP-based text simplification and bilingual glossary generation, both of which have visual components in some implementations, but the studies they cite typically measure language outcomes rather than the role of visuals specifically. Bewersdorff et al. (2024) present scenarios in which MLLMs adapt science explanations to language level, but these remain illustrative rather than empirically validated.
>
> The strongest evidence for the *conditions* under which AI-generated visual content produces learning, rather than for the magnitude of the effect, comes from Lawson and Mayer (2024). Their experimental contrast between summarising and drawing during multimedia animations indicates that the cognitive activity surrounding the visual is at least as important as the visual itself. This finding is convergent with Bühler et al.'s (2024) qualitative evidence that students with disabilities use generative AI most productively when they engage actively with the AI's output — querying, refining, and integrating — rather than passively consuming it.
>
> The qualitative evidence from Bühler et al. (2024) deserves particular emphasis because it documents the user perspective, which is often missing from technology-focused literature. Students with ADHD, dyslexia, dyspraxia, and autism reported that generative AI helped them structure ideas, overcome writer's block, and translate dense academic content into more accessible formats. They also reported concerns about AI inaccuracy, academic integrity, and the cost of subscription tools. The combination of perceived benefit and perceived risk is itself a significant finding, suggesting that learner agency and metacognitive judgement are central to the productive use of generative AI.
>
> Synthesising across the corpus, the efficacy claim that the evidence supports is conditional rather than absolute: AI-generated visual explanations can produce meaningful learning gains for the target populations *when* they are designed in accordance with multimedia learning principles, embedded in active learner tasks, and subject to learner judgement and verification.

### 4.4 Theme 4: Implementation Barriers and Ethical Concerns (~400 words)

> The fourth theme concerns the obstacles that limit the realisation of the technology's pedagogical potential. Five recurring concerns emerge from the corpus. The first is *accuracy and hallucination*. Generative models occasionally produce visually plausible but factually incorrect content, a problem that is particularly serious for learners who lack the prior knowledge to detect errors. Bühler et al. (2024) document this concern in the words of the affected learners themselves, who reported that they had been misled by confident but incorrect AI outputs.
>
> The second concern is *algorithmic bias*. Ahmad et al. (2025) note that AI models trained on predominantly Western, English-language, neurotypical data may produce visual content that reflects those defaults, with potentially exclusionary effects for learners outside those defaults. The literature does not yet provide systematic evidence on bias in AI-generated visual explanations specifically, but the concern is well-established for the underlying models.
>
> The third concern is *data protection and privacy*. Bewersdorff et al. (2024) flag this as a significant constraint for school-based deployment, particularly where AI services involve processing learner data on third-party infrastructure. For learners with disabilities, where diagnostic and intervention data may be involved, the stakes are higher.
>
> The fourth concern is *equity of access*. Bühler et al. (2024) report that subscription costs constitute a real barrier for some students, and Ahmad et al. (2025) note the broader digital-divide implications of AI-dependent pedagogy.
>
> The fifth concern is *the role of the educator*. Multiple studies in the corpus, including Bewersdorff et al. (2024), Ahmad et al. (2025), and Drosos et al. (2025), emphasise that AI tools should augment rather than replace teacher judgement. This emphasis is especially important for learners with disabilities or language barriers, where pedagogical decisions are often clinical and contextual in nature.
>
> Together these five concerns indicate that the question of pedagogical potential cannot be answered by reference to learning outcomes alone. The same tools that produce thirty per cent gains in reading comprehension in some contexts may, in other contexts, mislead learners, embed bias, compromise privacy, exclude the under-resourced, or displace the educator's role. Realising the pedagogical potential of AI-generated visual explanations therefore requires not only good design but also institutional, ethical, and pedagogical safeguards.

### 4.5 Synthesis Summary (~150 words)

> Taken together, the four themes converge on a single interpretation. AI-generated visual explanations represent a technologically viable, theoretically grounded, and partially evidenced pedagogical resource for learners with low language proficiency or learning disabilities. The technology is most useful when its design is anchored in multimedia learning theory, when it is embedded in active learner tasks, and when its outputs are subject to learner and teacher verification. The current research base is sufficient to justify careful implementation but insufficient to settle the larger questions about long-term learning outcomes, differential effects across disability profiles, and equity of access. The discussion that follows takes up these implications in turn.

---

## 5. Discussion and Conclusion (~1,000 words)

**Purpose of section:** Move from synthesis to interpretation. Address theoretical implications, practical implications, limitations, future directions, and a concluding statement.

### 5.1 Theoretical Implications (~250 words)

> The synthesis presented in §4 has three implications for multimedia learning theory. First, it supports Twabu and Modise's (2025) argument that CTML and CLT, while foundational, require extension to accommodate the adaptive, learner-responsive behaviour of generative AI. The classical principles remain valid as design heuristics, but they were articulated for static or pre-authored multimedia, not for systems that produce content in real time in response to learner input. The frameworks need conceptual room for AI as an active participant in the learning environment, not merely as a delivery channel.
>
> Second, the review confirms the centrality of the active-processing assumption. The most reliable finding across the corpus — supported by Lawson and Mayer's (2024) experimental work, by Bühler et al.'s (2024) interview data, and by the design choices in Osman et al.'s (2024) tool — is that visual content alone is insufficient. The cognitive activity surrounding the visual is what produces learning. This finding sets a clear constraint on AI-generated visual explanations: they must be designed to provoke cognitive engagement, not to substitute for it.
>
> Third, the review identifies adaptive cognitive load management as a productive frontier for theoretical work. AI systems can in principle measure and respond to learner load in ways that conventional multimedia cannot. Whether they should, and under what conditions, is a question that current theory does not yet answer. This is the most promising direction for theoretical extension.

### 5.2 Practical Implications (~250 words)

> For educators and instructional designers working with learners with low language proficiency or learning disabilities, the review yields several practical recommendations. First, the choice of AI tool should be guided by its alignment with multimedia learning principles, not by its technological novelty. A tool that respects the modality, signalling, and coherence principles will, on the available evidence, support learning more reliably than a more powerful tool that violates them. Second, AI-generated visuals should be embedded in active tasks: prompts that ask the learner to summarise, predict, compare, or critique the AI output, rather than simply receive it. The tasks need not be elaborate, but they must be present.
>
> Third, learners should be supported in developing critical engagement with AI outputs. The accuracy concerns documented in Bühler et al. (2024) and the bias concerns raised by Ahmad et al. (2025) are not problems that pedagogy can solve in isolation, but pedagogy can equip learners to detect and respond to them. Fourth, the educator's role remains central. AI-generated visual explanations should be treated as material that the educator selects, contextualises, and validates, not as autonomous instructional agents.
>
> Fifth, institutions adopting these tools at scale should consider equity of access. The benefits documented in the literature accrue to learners with stable connectivity, capable devices, and where applicable, paid subscriptions. Without institutional provision, the technology may widen rather than narrow the access gap for the very learners it claims to support.

### 5.3 Limitations of the Review (~200 words)

> Several limitations of this review should be acknowledged. The search was restricted to English-language publications, which excludes potentially relevant work in Russian, Mandarin, Spanish, and other languages with substantial educational research traditions. The date range of 2023–2025 reflects the post-GPT-4 era of multimodal generative AI but excludes earlier work that might illuminate longer-term trajectories. Source extraction was conducted by a single author without independent verification, which introduces potential for selection and interpretation bias; future iterations should employ at least two independent reviewers with formal inter-rater reliability assessment. The corpus of ten studies is small relative to the breadth of the topic, although deliberately so: the review prioritised depth of engagement over breadth of coverage. The thematic synthesis approach surfaces patterns but does not produce statistical effect-size estimates, which a meta-analysis on a more homogeneous sub-question could provide. Finally, the review treats learners with low language proficiency and learners with learning disabilities as a single population for analytic convenience, but these groups have distinct needs that future work should differentiate more carefully.

### 5.4 Directions for Future Research (~200 words)

> Four research directions follow from the synthesis. First, longitudinal studies are needed. The corpus is dominated by short-term evaluations and design studies; the cumulative effects of sustained exposure to AI-generated visual explanations on learner agency, metacognition, and language development remain unexamined. Second, differential-effects research is needed: the review has treated the target populations together, but evidence on how AI-generated visual explanations function for learners with dyslexia versus ASD versus low language proficiency, and at different ages, is currently sparse. Third, controlled studies of adaptive load management are needed to test the theoretical proposals advanced by Twabu and Modise (2025) and others. Fourth, culturally responsive design research is needed: most of the corpus reflects Anglophone, Western, well-resourced contexts, and the transferability of findings to other contexts — including Kazakhstani higher education, where the present review is situated — cannot be assumed. Cross-cultural comparative studies and studies grounded in non-Western educational traditions would substantially strengthen the field's external validity.

### 5.5 Conclusion (~100 words)

> AI-generated visual explanations are neither a panacea for inclusive education nor a passing trend. They are a technological capability whose pedagogical potential is real, partially evidenced, and conditional on careful design and institutional support. For learners with low language proficiency or learning disabilities, the technology offers a route around the linguistic bottleneck that has long constrained their access to complex content. Realising that potential will require a research base more integrated than the current literature, design practice more anchored in theory than in novelty, and institutional commitment more attentive to equity than to efficiency. The frameworks and evidence reviewed here suggest that this is feasible.

---

## 6. References (BibTeX entries to generate)

**For Claude Code:** Generate `references.bib` with the following entries. Keys are suggested below; adjust to match the template's citation style if necessary.

```bibtex
@incollection{panjwani2024,
  author    = {Panjwani-Charani, Shahzad and Zhai, Xiaoming},
  title     = {{AI} for Students with Learning Disabilities: A Systematic Review},
  booktitle = {Uses of Artificial Intelligence in {STEM} Education},
  editor    = {Zhai, Xiaoming and Krajcik, Joseph},
  publisher = {Oxford University Press},
  year      = {2024}
}

@article{bewersdorff2024,
  author  = {Bewersdorff, Arne and Hartmann, Christian and Hornberger, Marie and Se{\ss}ler, Kathrin and Bannert, Maria and Kasneci, Enkelejda and Kasneci, Gjergji and Zhai, Xiaoming and Fischer, Frank},
  title   = {Taking the Next Step with Generative Artificial Intelligence: The Transformative Role of Multimodal Large Language Models in Science Education},
  journal = {Computers \& Education},
  volume  = {230},
  pages   = {105199},
  year    = {2024}
}

@article{osman2024,
  author  = {Osman, Bayan and Shehab, Abdulaziz and Zaki, Ahmed},
  title   = {The Implementation of the Cognitive Theory of Multimedia Learning in the Design and Evaluation of an {AI} Educational Video Assistant Utilizing Large Language Models},
  journal = {Heliyon},
  volume  = {10},
  number  = {3},
  pages   = {e24139},
  year    = {2024}
}

@article{ahmad2025,
  author  = {Ahmad, Sayed Fayaz and Alam, Mohd. Mohsin and Rahimullah, Mohammad Khalid},
  title   = {Inclusive Education with {AI}: Supporting Special Needs and Tackling Language Barriers},
  journal = {AI and Ethics},
  publisher = {Springer},
  year    = {2025}
}

@article{lawson2024,
  author  = {Lawson, Alyssa P. and Mayer, Richard E.},
  title   = {Generative Learning Activities for Online Multimedia Learning: When Summarizing Is Effective but Drawing Is Not},
  journal = {Frontiers in Psychology},
  volume  = {15},
  pages   = {1452385},
  year    = {2024}
}

@article{drosos2025,
  author  = {Drosos, Christos and Papakostas, Christos and Drigas, Athanasios},
  title   = {A Systematic Review of {AI}, {VR}, and {LLM} Applications in Special Education: Opportunities, Challenges, and Future Directions},
  journal = {Education and Information Technologies},
  publisher = {Springer},
  year    = {2025}
}

@article{buhler2024,
  author  = {B{\"u}hler, Tobias and Ebner, Katharina and Pargmann, Julia and Pl{\"o}{\ss}nig, Manuela},
  title   = {Exploring the Role of Generative {AI} in Higher Education: Semi-Structured Interviews with Students with Disabilities},
  journal = {Education and Information Technologies},
  publisher = {Springer},
  year    = {2024}
}

@article{urrea2024,
  author  = {Urrea, Ana L{\'o}pez and Fern{\'a}ndez-Torres, Virginia and Rodriguez-Ortiz, Isabel R. and Salda{\~n}a, David},
  title   = {The Use of Technology-Assisted Intervention in Vocabulary Learning for Children with Autism Spectrum Disorder: A Systematic Review},
  journal = {Frontiers in Psychology},
  volume  = {15},
  pages   = {1370965},
  year    = {2024}
}

@article{twabu2025,
  author  = {Twabu, Khanyisile and Modise, Mphoentle Puleng},
  title   = {Enhancing the Cognitive Load Theory and Multimedia Learning Framework with {AI} Insight},
  journal = {Discover Education},
  volume  = {3},
  publisher = {Springer},
  year    = {2025}
}

@article{khoirunnisa2024,
  author  = {Khoirunnisa, Ade Novia and Munir, Munir and Shahbodin, Faaizah and Dewi, Laksmi},
  title   = {Augmented Reality Based Personalized Learning in Autism Spectrum Disorder Reading Skills},
  journal = {Journal of Special Education Technology},
  publisher = {SAGE},
  year    = {2024}
}
```

---

## 7. Word-Count Tracker (Targets vs. Plan-Provided Draft)

| Section | Target | Draft provided here |
|---|---|---|
| Abstract | ~250 | ~250 ✓ |
| 1. Introduction | 800–1,000 | ~900 ✓ |
| 2. Literature Review | 1,800–2,100 | ~2,000 ✓ |
| 3. Methodology | 1,000–1,200 | ~1,100 ✓ |
| 4. Findings/Analysis | ~2,000 | ~2,000 ✓ |
| 5. Discussion/Conclusion | ~1,000 | ~1,000 ✓ |
| **Total body** | **~7,000** | **~7,000 ✓** |

---

## 8. LaTeX Conversion Checklist for Claude Code

- [ ] Open existing university template; preserve preamble, title page, declaration page
- [ ] Insert title, author, supervisor, date as per template fields
- [ ] Add `\usepackage{booktabs}`, `\usepackage{float}`, `\usepackage[backend=biber,style=apa]{biblatex}` if not already present
- [ ] Add `\addbibresource{references.bib}` and create `references.bib` from §6
- [ ] Convert each `##` heading to `\section{}`, each `###` to `\subsection{}`
- [ ] Convert markdown emphasis: `*italic*` → `\textit{}`, `**bold**` → `\textbf{}`
- [ ] Convert blockquotes (the `>` prefixed prose) into normal paragraphs — they are draft content, not actual quotations
- [ ] Replace inline citations like "Bewersdorff et al. (2024)" with `\textcite{bewersdorff2024}` and "(Bewersdorff et al., 2024)" with `\parencite{bewersdorff2024}`
- [ ] Render Table 1 with `tabular`/`booktabs`; caption above the table; label `tab:studies`
- [ ] Insert PRISMA flow diagram as Figure 1 (TikZ if possible, otherwise placeholder)
- [ ] Run `pdflatex` → `biber` → `pdflatex` → `pdflatex` to resolve all citations
- [ ] Confirm word count of body text (excluding references and front matter) is in the 6,800–7,200 range
- [ ] Verify no orphaned headings, no unresolved `?` citations, no overfull `hbox` warnings on critical pages

---

## 9. Stylistic Notes

- **Voice:** third-person academic, past tense for individual studies, present tense for ongoing claims and theoretical statements.
- **Hedging:** prefer "the evidence suggests", "the corpus indicates", "appears to" over flat assertions, especially for efficacy claims drawn from heterogeneous studies.
- **Citation density:** every empirical claim attributable to a specific study should carry a citation. The Introduction can be lighter; Findings should be densest.
- **British vs. American English:** the draft above uses British spelling (organised, behaviour, recognised, generalisation). Switch globally if the template requires American English.
- **Tables and figures:** number sequentially (Table 1, Figure 1) and refer to them in text *before* they appear.

