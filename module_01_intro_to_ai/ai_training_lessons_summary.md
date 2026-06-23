# AWS Foundational AI Training: Lessons 1 to 9 Brief Summary

## Lesson 1: Fundamentals of Machine Learning and AI
* **AI Core Definitions**:
  * **Artificial Intelligence (AI)**: Broad field encompassing systems capable of perception, reasoning, learning, problem-solving, and decision-making.
  * **Machine Learning (ML)**: Algorithms enabling computers to learn from data to improve task performance.
  * **Deep Learning (DL)**: Subset of ML mimicking biological brain structures (neurons and synapses).
  * **Generative AI (GenAI)**: Subset of DL adapting pre-trained foundation models to generate novel data (text, images, audio, etc.) without retraining from scratch.
* **Data Typologies**:
  * **Labeled vs. Unlabeled**: Labeled contains explicit target outputs (e.g., classification tags); unlabeled contains raw input features only.
  * **Structured vs. Unstructured**: Structured is tabular/time-series (rows and columns); unstructured lacks predefined formatting (e.g., text, images, audio, video).
* **ML Learning Paradigms**:
  * **Supervised**: Model learns mappings from labeled training data.
  * **Unsupervised**: Model identifies underlying patterns/clusters in unlabeled data.
  * **Reinforcement**: Agent learns optimal actions via trial-and-error rewards/penalties.
* **Inference Models**:
  * **Batch Inference**: Offline, high-volume processing of static data chunks (prioritizes throughput and accuracy over latency).
  * **Real-Time Inference**: Near-instantaneous, low-latency predictions on incoming data stream (e.g., chatbots, autonomous driving).
* **Deep Learning Architectures**:
  * **Neural Networks**: Node layers (input, hidden, output) adjusting connection weights to map relationships.
  * **Computer Vision (CV) & NLP**: Primary DL domains for visual processing and human language interaction.
  * **Diffusion Models**: Generate high-fidelity outputs by gradually adding noise (forward diffusion) and then iteratively removing it (reverse diffusion).
  * **Generative Adversarial Networks (GANs)**: Zero-sum competition between a *Generator* (creates synthetic data) and a *Discriminator* (detects fakes).
  * **Variational Autoencoders (VAEs)**: Encodes input into a probabilistic latent space; Decodes it to reconstruct original samples.
* **Foundation Models (FMs)**:
  * Large-scale models pre-trained on massive internet datasets via **self-supervised learning** (auto-generating labels from data structure).
  * **FM Lifecycle**: Data Selection $\to$ Pre-training (context & grammar) $\to$ Continuous Pre-training $\to$ Optimization (prompts/RAG/tuning) $\to$ Evaluation $\to$ Deployment $\to$ Continuous Feedback & Monitoring.
  * **LLM Core Concepts**:
    * **Tokens**: Basic units of text (words, characters) processed.
    * **Embeddings/Vectors**: Numerical representations mapping tokens in a multi-dimensional semantic space.
* **AWS AI/ML Services Stack**:
  * *ML Frameworks*: **Amazon SageMaker AI** (fully managed workflow to build, train, deploy custom models).
  * *Specialized AI Services*:
    * **Comprehend** (NLP & Sentiment), **Translate** (Neural translation), **Textract** (OCR & form extraction), **Lex** (Chatbots/NLU), **Polly** (Text-to-speech), **Transcribe** (Speech-to-text), **Rekognition** (Computer Vision), **Kendra** (Enterprise search), **Personalize** (Recommender engine), **DeepRacer** (Reinforcement learning).
  * *GenAI Layer*:
    * **SageMaker JumpStart** (Pre-trained open-source model hub), **Amazon Bedrock** (Managed serverless API accessing frontier models), **Amazon Q** (Work assistant), **Amazon Q Developer** (Coding buddy).
  * *Cost Trade-Offs*: Balance latency/responsiveness, Regional availability, compute type (CPU vs. GPU), token-based pricing, provisioned throughput, and custom model infrastructure.

---

## Lesson 2: Exploring AI Use Cases and Applications
* **Sector Applications**:
  * **Media & Entertainment**: Synthetic scriptwriting, immersive VR environments, automated journalism.
  * **Retail**: Product review summaries, price optimization modeling, virtual try-ons, store layout designs.
  * **Healthcare**: **AWS HealthScribe** (automated clinical notes from patient-clinician conversation logs), personalized medicine, medical imaging enhancement.
  * **Life Sciences**: Generative drug discovery (molecular structure design), protein folding prediction.
  * **Financial Services**: Fraud detection (simulating money-laundering data), scenario portfolio management, automated debt collection.
  * **Manufacturing**: Predictive maintenance scheduling, process parameter optimization, generative product design.
* **Key AI Applications**:
  * **Computer Vision**: Autonomous driving, medical diagnostics, safety facial/image search.
  * **NLP**: Redacting sensitive insurance policy details, customer sentiment analysis, educational Q&A chatbots.

---

## Lesson 3: Responsible AI Practices
* **Responsible AI Pillars**:
  * **Fairness**: Preventing discrimination and promoting inclusion.
  * **Explainability**: Clarifying *why* a model reached a decision.
  * **Privacy & Security**: Protecting user data; ensuring user control of inputs.
  * **Transparency**: Disclosing *how* the system works (capabilities, limitations, cards).
  * **Veracity & Robustness**: Resiliency to unexpected errors, adversarial inputs, or distribution shifts.
  * **Governance**: Formal corporate policies managing legal liabilities, bias, and IP rights.
  * **Safety**: Proactively avoiding unintended physical, environmental, or social harm.
  * **Controllability**: Steerability of model behavior to align with human intent.
* **Business Benefits**: Increased brand trust/reputation, compliance, risk mitigation, competitive edge, better data-driven decisions.
* **AWS Responsible AI Tools**:
  * **Bedrock Model Evaluation**: Automatic (robustness, toxicity) and human evaluations (style, brand voice).
  * **SageMaker AI Clarify**: Explains feature attributions (SHAP/LIME) and detects bias in datasets/model predictions.
  * **Guardrails for Bedrock**: Blocks restricted topics, filters harmful content, and redacts PII.
  * **SageMaker Data Wrangler**: Rebalances datasets using SMOTE, random over/undersampling.
  * **SageMaker Model Monitor & Amazon A2I**: Continuous quality monitoring and human-in-the-loop validation.
  * **SageMaker Governance**: Role Manager (least privilege), Model Cards (training metadata), Model Dashboard (production health).
  * **AWS AI Service Cards**: Transparent documentation outlining limitations, design choices, and best practices.
* **HCD (Human-Centered Design) Principles**:
  * **Design for Amplified Decision-Making**: Optimize for clarity, simplicity, usability, reflexivity, and accountability.
  * **Design for Unbiased Decisions**: Assess bias, design fair tools, and train decision-makers.
  * **Design for Human-AI Learning**: Leverage cognitive apprenticeship (mutual learning), personalization, and RLHF (via SageMaker Ground Truth data annotation).
* **Model Selection Trade-Offs**:
  * **Interpretability vs. Performance**: Simple models (linear regression) offer high transparency (exact mechanics/weights) but lower accuracy. High-performance models (deep neural nets) require model-agnostic explainability tools (surrogates, SHAP).
  * **Safety vs. Transparency**: Security constraints (differential privacy, output filtering, air-gapped training) protect data but limit model inspection/auditing.
  * **Controllability**: Steerability via data manipulation. Simpler models are more controllable.
  * **Sustainability (Environmental)**: Assessing energy consumption footprints and hardware recycling (GPUs/TPUs).

---

## Lesson 4: Developing Machine Learning Solutions
* **ML Lifecycle Phases**: Business Goals $\to$ Problem Framing $\to$ Data Processing (Collection, Cleaning, Feature Engineering) $\to$ Model Development (Train, Tune, Evaluate) $\to$ Deployment $\to$ Monitoring $\to$ Retraining.
* **Model Sourcing**:
  * *Pre-trained Models*: Lowest operational overhead (SageMaker JumpStart).
  * *Built-in Algorithms*: General purpose classification, regression, clustering, image, or text processing.
  * *Custom Docker Images*: Custom packages configured inside containers.
* **Model Fit & Evaluation**:
  * **Overfitting**: Model memorizes training data (high variance, low bias); performs poorly on unseen data.
  * **Underfitting**: Model is too simple to capture patterns (high bias, low variance); performs poorly even on training data.
  * **Split Strategy**: Dividing labeled data into Training, Validation (tuning/fit checks), and Testing subsets (typically 80/10/10).
* **Metrics**:
  * **Classification**:
    * **Confusion Matrix**: Maps True Positives (TP), True Negatives (TN), False Positives (FP), and False Negatives (FN).
    * **Accuracy**: (TP+TN)/Total. Less effective for imbalanced datasets.
    * **Precision**: TP/(TP+FP). Crucial when false positive costs are high.
    * **Recall (Sensitivity)**: TP/(TP+FN). Crucial when missing positive cases is costly (e.g., terminal illness).
    * **AUC-ROC**: Evaluation curve comparing True Positive vs. False Positive rates at various thresholds.
  * **Regression**:
    * **Mean Squared Error (MSE)**: Measures average squared difference between predictions and actual values.
    * **R-squared**: Explains the percentage of variance explained by model inputs.
* **Deployment Options**:
  * *Self-Hosted APIs* (infra control) vs. *Managed APIs* (managed by AWS, low overhead).
  * **SageMaker Inference Options**: Real-time (interactive, low latency), Batch Transform (large datasets, non-persistent endpoint), Asynchronous (large payloads up to 1GB, long run times), Serverless (idle traffic tolerances, cold start friendly).
* **MLOps (Machine Learning Operations)**:
  * Adopts DevOps principles for ML workflows: version control (data/code/model versioning), automation, and CI/CD.
  * **Continuous Touchpoints**: Integration (code/data/model validation), Delivery (model release), Training (auto-retraining), Monitoring (drift/business metrics).
  * **Pipeline Stages**: Model Build $\to$ Model Evaluation $\to$ Registry/Approval $\to$ Model Deployment $\to$ Live Feedback.

---

## Lesson 5: Developing Generative AI Solutions
* **GenAI App Lifecycle**: Use Case Formulation $\to$ Model Selection $\to$ Performance Improvement $\to$ Evaluation $\to$ Deployment.
* **Customization Approaches (Cost-Accuracy Trade-off)**:
  * *Pre-trained FMs*: Fast, lowest cost, lower task-specific accuracy.
  * *RAG (Retrieval-Augmented Generation)*: Augments prompts with external document context. High factual accuracy, lower cost, no weight adjustments.
  * *Fine-tuning*: Adjusts weights using instruction datasets or human feedback (RLHF). High specificity, moderate cost.
  * *Self-Trained (Scratch)*: Custom architecture and weights. Extreme customization, extremely high cost, compute, and time.
* **Evaluating GenAI Outputs**:
  * **GLUE/SuperGLUE**: Standard benchmarks for language understanding.
  * **SQuAD & WMT**: QA and translation benchmarks.
  * **ROUGE**: Recall-oriented overlap check for summarization completeness (ROUGE-N, ROUGE-L).
  * **BLEU**: Precision-oriented phrase matching for translation accuracy.
  * **BERTScore**: Semantic similarity comparison using contextual embeddings (avoids reliance on exact word matches).
* **Agents**: Autonomous software components breaking down complex processes into subtasks, orchestrating resources, and logging execution metrics.

---

## Lesson 6: Optimizing Foundation Models
* **RAG Architecture (Context Injection)**:
  * Raw enterprise documents are split, tokenized, and converted to high-dimensional **vector embeddings**.
  * Embeddings are stored in a **vector database** (e.g., AWS OpenSearch, Aurora/RDS PostgreSQL with pgvector, Amazon Kendra).
  * Query inputs prompt a **Similarity Search** (k-NN or Cosine Similarity) to fetch relevant context documents.
* **RAG Agents & Execution**:
  * Chatbots utilize agents to perform tasks autonomously (e.g., checking plan details, initiating a product swap) by coordinating APIs.
* **RAG Evaluation**:
  * SMEs create benchmark datasets (questions, context, reference answers).
  * **LLM-as-a-Judge**: An external LLM compares generated chatbot answers against reference answers to grade performance.
* **Fine-Tuning Approaches**:
  * **Instruction Tuning**: Retraining models on prompt-response pairs.
  * **RLHF**: Human ratings/preferences create a reward function (using SageMaker Ground Truth data annotation).
  * **Domain Adaptation**: Customizing on specialized corpus (e.g., medical journal).
  * **Continuous Pre-training**: Extending pre-training on raw domain data.
* **Fine-Tuning Curation**: Requires high-quality, relevant data. Curation stages: Data Curation $\to$ Accurate Labeling $\to$ Governance/Compliance $\to$ Representativeness/Bias check $\to$ Feedback integration.

---

## Lesson 7: Security, Compliance, and Governance
* **Pillars of Adherence**:
  * **Security**: Confidentiality, integrity, availability of infra/workloads.
  * **Governance**: Empowering business value while managing systemic risk.
  * **Compliance**: Adhering to laws, industry standards, and regulations.
* **Defense-in-Depth Strategy**:
  * **Data Protection**: Encryption at rest (KMS) and in transit (ACM, Private CA, VPC/PrivateLink).
  * **Identity/Access**: AWS IAM (least privilege, short-term credentials, Access Analyzer).
  * **Application Protection**: AWS Shield, Amazon Cognito.
  * **Network & Edge**: Amazon VPC, AWS WAF.
  * **Infrastructure**: IAM user groups, network ACLs.
  * **Threat Detection**: AWS Security Hub, Amazon GuardDuty.
  * **Incident Response**: AWS Lambda, EventBridge.
* **Compliance & AI Risks**:
  * Common certifications: NIST 800-53, ISO 27001, SOC, HIPAA, GDPR, PCI DSS.
  * **AI Compliance Differences**: Complexity/opacity (black boxes), dynamism/adaptability (models change post-deployment), emergent/unexpected capabilities, unique risks (algorithmic bias).
  * **Algorithm Accountability**: Laws (e.g., EU AI Act) requiring risk assessments, transparency, and human oversight.
  * **Regulated Workloads**: HR, safety, inspection, and regulatory environments (finance, healthcare, aerospace).
* **AWS Governance Services**:
  * **AWS Config**: Resource configurations and historical changes for auditing.
  * **Amazon Inspector**: Scanning running EC2, containers, and Lambda functions for software CVEs and network exposure.
  * **AWS Audit Manager**: Automating evidence collection to prove regulatory control effectiveness.
  * **AWS Artifact**: On-demand download of AWS-owned SOC, PCI, and ISO compliance certifications.
  * **AWS CloudTrail & Trusted Advisor**: Tracking account API operations and optimizing environment health (security, resilience, cost).
* **Data Governance in AI**:
  * Managing data quality (completeness, accuracy, timeliness, consistency) and tracking **lineage and provenance** (origins and flow history).
  * Implementing Privacy-Enhancing Technologies (PETs): masking, obfuscation, differential privacy, tokenization.
  * **AI Scoping Matrix (Security Scopes)**:
    * *Scope 1 (Consumer App)*: No data/model ownership (e.g., public chat tools).
    * *Scope 2 (Enterprise App)*: Third-party app with embedded GenAI (vendor contract controls).
    * *Scope 3 (Pre-trained Models)*: Integration with a third-party model via API (e.g., Bedrock).
    * *Scope 4 (Fine-tuned Models)*: Customizing a third-party model with private business data.
    * *Scope 5 (Self-trained Models)*: Building/training model from scratch (full ownership of data/weights).

---

## Lesson 8: Essentials of Prompt Engineering
* **Benefits**: Bolsters safety, injects domain-specific knowledge, and explores capability without altering model weights.
* **Core Elements**:
  * **Instructions**: Task description of what to do.
  * **Context**: External guiding info/guidelines.
  * **Input Data**: The raw text/values to process.
  * **Output Indicator**: Format/indicator for the output (e.g., "Fulfillment status:").
* **Best Practices**:
  * Keep prompts clear, concise, and structured.
  * Use directives for response type (length, format constraint).
  * Leverage **Negative Prompting** to steer the model away from unwanted topics/toxicity.
  * Start with questions (Who, What, How) and break complex tasks into subtasks (e.g., asking model to "Think step-by-step").
* **Inference Settings (Inference Parameters)**:
  * **Temperature**: Controls creativity/randomness (0 is deterministic, 1 is creative).
  * **Top P**: Word selection diversity limit based on cumulative probability (e.g., top 25% distribution).
  * **Top K**: Limits word pool to the *K* most probable next words.
  * **Length Parameters**: Maximum length (max generated tokens) and **Stop Sequences** (special tokens to terminate generation).
* **Prompt Engineering Techniques**:
  * **Zero-shot**: Relying on world knowledge without examples.
  * **Few-shot / One-shot**: Providing example input-output pairs inside the prompt.
  * **Chain-of-Thought (CoT)**: Guiding the model to output intermediate logical steps.
* **Prompt Vulnerabilities**:
  * **Poisoning**: Contaminating training datasets.
  * **Hijacking/Prompt Injection**: Manipulating input prompts to force malicious outputs/instructions.
  * **Exposure**: Inadvertent leakage of sensitive training data through output.
  * **Prompt Leaking**: Users tricking the model to reveal its system prompt instructions.
  * **Jailbreaking**: Circumventing ethical/safety filters by roleplay or hypothetical scenarios.

---

## Lesson 9: From Theory to Practice with PartyRock
* **PartyRock Definition**: AWS-managed sandbox application layer built on top of Amazon Bedrock that abstracts cloud deployment, API calls, and key management.
* **App Modalities**: Text generation, image creation, and data analysis.
* **Core Concepts**:
  * **Prompt Templates & Variable Injection**: Input fields (e.g., user preferences) act as variables injected dynamically into system prompt templates.
  * **App Remixing**: Creating personal copies of public apps to adjust the underlying **Dependency Graph**.
  * **Prompt Chaining**: Routing output of one widget into another to ground subsequent generations and reduce hallucinations.
  * **Model Orchestration**: Selecting different models (Haiku vs. Opus) for specific steps in a chain to balance speed, cost, and intelligence.
* **Image Playground Mechanics**:
  * **Latent Space**: Multi-dimensional concept maps where prompt keywords act as coordinate vectors.
  * **Denoising**: Model starts with random noise and removes it iteratively to reveal the conceptual image.
* **Data Analysis OLAP Loop**:
  * *The Grid Paradox*: Transformers read text linearly and struggle with 2D grids (serialization limits and probabilistic math errors).
  * *Engine-in-the-Middle*: PartyRock solves this by embedding an OLAP database engine (like **DuckDB**).
  * *Tool execution loop*: The LLM generates SQL queries based on the database schema, passes them to the engine for deterministic math execution, and translates the results back into natural language.
