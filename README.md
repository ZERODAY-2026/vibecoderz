# vibecoderz

# 🌑 Dark Lands

### Understand Before You Sign.

**An AI-powered, privacy-first legal document understanding platform that helps people understand complex legal documents in simple language.**

Dark Lands aims to make legal documents easier to understand by identifying important clauses, explaining obligations, highlighting potential concerns, and helping users locate relevant information without requiring them to have a legal background.

Built for **ZeroDay OSS Hacktoberfest 2026 — AI Problem Statement 2: Private Legal Document Triage Agent.**

---

## 📌 Table of Contents

* [About the Project](#-about-the-project)
* [Problem Statement](#-problem-statement)
* [Our Solution](#-our-solution)
* [Key Features](#-key-features)
* [What Makes Dark Lands Different](#-what-makes-dark-lands-different)
* [Supported Languages](#-supported-languages)
* [Privacy and Security](#-privacy-and-security)
* [Technology Stack](#-technology-stack)
* [System Architecture](#-system-architecture)
* [Getting Started](#-getting-started)
* [Local AI Setup](#-local-ai-setup)
* [Project Structure](#-project-structure)
* [Testing](#-testing)
* [Limitations](#-limitations)
* [Roadmap](#-roadmap)
* [Contributing](#-contributing)
* [License](#-license)
* [Disclaimer](#-disclaimer)

---

## 📖 About the Project

Legal documents often contain complicated terminology, lengthy clauses, and conditions that are difficult for ordinary people to understand.

Rental agreements, employment contracts, service agreements, and legal notices may contain important obligations, payment conditions, penalties, deadlines, and termination clauses.

Dark Lands is designed to help users understand these documents through a straightforward interface and AI-powered explanations grounded in the actual document text.

Our goal is simple:

**Make legal information easier to understand while keeping private documents under the user's control.**

Dark Lands is being developed as an open-source project with a privacy-first architecture and support for local AI inference.

---

## 🚨 Problem Statement

**Private Legal Document Triage Agent**

People without legal training may struggle to identify important information in legal documents.

Common challenges include:

* Understanding complex legal language.
* Identifying payment obligations and penalties.
* Finding termination clauses and notice periods.
* Recognizing important dates and deadlines.
* Understanding ambiguous or potentially concerning clauses.
* Comparing different versions of an agreement.
* Protecting confidential documents while using AI tools.

Traditional document viewers display the text but do not explain its practical meaning.

Cloud-based AI tools may also require users to transmit confidential information to external services.

Dark Lands addresses these challenges through document-grounded explanations and a privacy-focused approach to AI processing.

---

## 💡 Our Solution

Dark Lands aims to provide a single platform where users can upload a legal document, explore its important clauses, ask questions about its contents, and understand their obligations in simple language.

The proposed workflow is:

1. Upload a PDF or TXT document.
2. Extract its text locally.
3. Analyze relevant passages using a compatible local AI model.
4. Identify important clauses and obligations.
5. Display explanations with source passages and page references where available.
6. Explore questions, potential concerns, and important dates.
7. Delete the document and its associated data when finished.

The system is designed to distinguish between what the document explicitly states, what may require further review, and what cannot be determined from the available text.

---

## ✨ Key Features

### 1. 📄 Private Document Analysis

Designed to support PDF and plain-text documents.

The analysis workflow aims to identify:

* Document type and parties.
* Payment obligations.
* Deposits and refund conditions.
* Penalties and liability provisions.
* Termination conditions.
* Notice periods.
* Renewal conditions.
* Confidentiality obligations.
* Dispute resolution clauses.
* Important dates.
* Ambiguous wording and missing information.

Findings should be linked to supporting passages from the original document.

### 2. 🧭 Clause Compass

Clause Compass is the signature feature of Dark Lands.

It organizes important clauses into five sections:

**What It Says**
A plain-language explanation of the original clause.

**What It Means for You**
An explanation of the practical obligations or conditions suggested by the wording.

**What You Should Check**
Potential ambiguities, missing details, and questions worth asking.

**Where to Find It**
The original passage, page reference where available, and a link to the relevant document section.

**What-If Explorer**
An interactive way to explore hypothetical situations using relevant clauses from the document.

The objective is to help users understand the document without inventing unsupported legal conclusions.

### 3. 🗺️ Document Transparency Map

A structured overview of important document topics.

Potential categories include:

* Payments and money.
* Rights and responsibilities.
* Deadlines.
* Termination.
* Penalties.
* Confidentiality.
* Liability.
* Ambiguous wording.
* Missing information.

Each category should connect to relevant passages in the original document.

The map is intended to improve document navigation and help users identify areas that may deserve closer attention.

### 4. 📅 Personal Obligation Timeline

Designed to identify dates and obligations explicitly stated in a document.

Examples include:

* Rent payment dates.
* Contract expiration dates.
* Renewal deadlines.
* Notice periods.
* Payment milestones.

The timeline should distinguish explicit dates from calculated dates and explain any assumptions involved.

It must not invent deadlines or automatically create external calendar events.

### 5. 💬 Ask My Document

A document-grounded question-and-answer interface.

Example questions:

* What does this paragraph mean?
* Does this agreement mention a penalty?
* What happens to the deposit according to this document?
* Which section explains my responsibilities?
* Does the document specify a notice period?
* What information is missing?

Answers are intended to include supporting quotations, page references where available, and clear explanations of uncertainty.

When the document does not answer a question, the application should say so rather than fabricate a response.

### 6. 🔍 Document Comparison

Designed to compare two documents and identify:

* Added clauses.
* Removed clauses.
* Changed wording.
* Changed dates.
* Changed monetary amounts.
* Changed obligations.
* Potentially significant differences.

Text differences should be identified using deterministic comparison techniques where possible, with local AI used to explain differences when appropriate.

### 7. 🌐 Multilingual Interface

Planned interface languages:

* English
* हिंदी (Hindi)
* ಕನ್ನಡ (Kannada)
* తెలుగు (Telugu)
* தமிழ் (Tamil)

The language selector is intended to make the application accessible to a wider range of users.

Original legal text should remain unchanged when explanations are translated.

Language support and AI-generated explanation quality must be tested for each supported language.

### 8. 🌓 Dark Mode and Light Mode

The application is designed to provide both dark and light themes.

The theme system aims to include:

* A persistent theme preference.
* System theme detection on the first visit.
* Consistent styling across pages and dialogs.
* Accessible text contrast.
* Readable document highlights.

### 9. 🔗 Legal Resource Connect

A directory of public legal resources intended to help users find official information.

Potential resources include:

* India Code.
* eCourts.
* Other verified official government legal-information resources.

Private documents must not be automatically uploaded to external legal websites or included in external searches.

The application should use direct official links when a supported public API is unavailable.

### 10. 🔐 Privacy Centre

A dedicated area intended to make data handling transparent.

Planned capabilities include:

* AI model and runtime status.
* Document storage information.
* Document deletion controls.
* Temporary-file cleanup.
* Network requirement information.
* Privacy and security documentation.
* Offline operation verification.

Privacy claims should reflect actual implementation and testing rather than assumptions.

---

## 🚀 What Makes Dark Lands Different?

Dark Lands focuses on more than summarizing a document.

| Capability                   | Purpose                                                         |
| ---------------------------- | --------------------------------------------------------------- |
| Clause Compass               | Breaks important clauses into understandable sections.          |
| Document Transparency Map    | Organizes relevant passages by topic.                           |
| Personal Obligation Timeline | Helps users review dates and obligations.                       |
| Ask My Document              | Answers questions using retrieved document passages.            |
| Document Comparison          | Identifies changes between document versions.                   |
| Local AI Architecture        | Aims to keep private document processing on the user's machine. |
| Five-Language Interface      | Makes the application accessible to more users.                 |
| Privacy Centre               | Makes storage, deletion, and network behavior transparent.      |

The emphasis is on **understandable explanations, traceable evidence, and privacy-conscious processing**.

---

## 🛠️ Technology Stack

The intended technology stack includes:

| Component            | Technology                                                        |
| -------------------- | ----------------------------------------------------------------- |
| Frontend             | Next.js                                                           |
| UI Framework         | React                                                             |
| Programming Language | TypeScript                                                        |
| Styling              | Tailwind CSS                                                      |
| AI Model             | Google Gemma 3n E2B/E4B or another hackathon-approved local model |
| AI Inference         | Compatible local inference runtime                                |
| Document Processing  | Local PDF and TXT extraction                                      |
| Local Data           | Temporary storage or an appropriate local database                |
| Testing              | Automated tests and manual verification                           |
| Version Control      | Git and GitHub                                                    |

The final implementation may vary depending on the existing repository and verified model-runtime compatibility.

Refer to the actual project configuration for installed dependency versions.

---

## 🏗️ System Architecture

Dark Lands is intended to separate the interface, document processing, AI inference, and evidence verification into distinct components.

```text
                 ┌──────────────────────────┐
                 │       Dark Lands         │
                 │      User Interface      │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │    Document Upload       │
                 │    Validation Layer      │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │    Local Extraction      │
                 │       PDF / TXT          │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │   Passage Processing     │
                 │   and Local Retrieval    │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │   Local AI Inference     │
                 │      Gemma Model         │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │   Evidence Validation    │
                 │  and Source References   │
                 └────────────┬─────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │   Analysis and Results   │
                 │  Explanations / Timeline │
                 └──────────────────────────┘
```

**Privacy principle:** Private document contents should remain within the local processing environment. External legal-resource browsing must not automatically transmit document contents.

The actual implementation must be tested to verify these properties.

---

## ⚙️ Getting Started

### Prerequisites

Before running the application, check that your system has the prerequisites required by the repository:

* Git.
* Node.js, if required by the project.
* The package manager specified by the project lockfile.
* Sufficient memory and storage for the selected local AI model.
* A compatible local inference runtime for AI-powered features.

The exact hardware requirements depend on the model variant, quantization, runtime, and operating system.

### 1. Clone the Repository

Replace the placeholder below with the actual public GitHub repository URL.

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Navigate into the cloned repository:

```bash
cd <YOUR_REPOSITORY_DIRECTORY>
```

### 2. Install Dependencies

Use the package manager corresponding to the repository's lockfile.

For an npm-based project:

```bash
npm install
```

For a project using another package manager, follow its documented installation procedure.

### 3. Configure Environment Variables

If the application requires environment variables, create a local configuration file using the provided example:

```bash
cp .env.example .env.local
```

On Windows Command Prompt, you can use:

```cmd
copy .env.example .env.local
```

Configure only the variables documented by the project.

Never commit `.env.local`, passwords, private keys, or other secrets to GitHub.

Do not add cloud AI API keys for document analysis if the application is intended to operate exclusively through local inference.

### 4. Start the Development Server

For an npm-based Next.js project:

```bash
npm run dev
```

Open the local address printed by the development server in your browser.

The default Next.js development address is commonly:

```text
http://localhost:3000
```

The actual address may differ depending on your configuration and available ports.

### 5. Configure the Local AI Model

Follow the model and inference-runtime instructions documented for the actual implementation.

The application should report whether the local model is available.

Do not consider AI-powered document analysis operational until a real inference request succeeds.

---

## 🤖 Local AI Setup

Dark Lands is designed around local AI inference to reduce the exposure of confidential documents to external services.

The intended model is Google Gemma 3n E2B/E4B or another model explicitly accepted by the hackathon.

The final model and runtime must be selected according to:

* Model availability.
* Hardware compatibility.
* Memory requirements.
* Runtime support.
* Quantization options.
* Model licence.
* Offline inference capabilities.

Model weights may need to be downloaded during initial setup.

Once setup is complete, private document processing should work without networking when the chosen runtime and application dependencies support offline operation.

**Important:** The exact model configuration and setup commands must be documented after the selected runtime has been tested. No particular model variant or inference configuration should be considered verified merely because it appears in the project documentation.

---

## 📂 Project Structure

The final structure depends on the existing repository and the implementation.

A possible organization is:

```text
dark-lands/
├── public/
├── src/
│   ├── app/
│   │   ├── page.tsx
│   │   ├── layout.tsx
│   │   ├── dashboard/
│   │   ├── analysis/
│   │   ├── comparison/
│   │   ├── resources/
│   │   ├── privacy/
│   │   └── api/
│   ├── components/
│   ├── lib/
│   │   ├── document-processing/
│   │   ├── ai/
│   │   ├── retrieval/
│   │   ├── validation/
│   │   └── i18n/
│   ├── messages/
│   └── types/
├── tests/
├── docs/
├── .env.example
├── .gitignore
├── package.json
├── README.md
└── LICENSE
```

This is an illustrative structure, not a claim that every directory already exists. Refer to the actual repository for the current implementation.

---

## 🧪 Testing

Dark Lands should be tested with real documents and reproducible test cases.

Important test categories include:

* PDF text extraction.
* TXT file extraction.
* Empty and malformed files.
* Large documents.
* Page and passage tracking.
* Citation verification.
* Missing information.
* Unsupported questions.
* Incorrect model outputs.
* Prompt injection.
* Document comparison.
* Theme switching.
* Language switching.
* Document deletion.
* Offline document processing.
* Temporary-file cleanup.

Run the checks configured in the repository.

For an npm-based project, the available commands can be inspected using:

```bash
npm run
```

Common commands, when configured, include:

```bash
npm run lint
npm run test
npm run build
```

Not every repository defines all these scripts. Use the actual scripts in `package.json`.

Tests must be executed before reporting their results.

Privacy and offline behavior require verification beyond ordinary unit tests.

---

## 🔒 Privacy and Security

Privacy is a core design objective of Dark Lands.

The application is intended to follow these principles:

* Process private documents locally.
* Avoid unnecessary document persistence.
* Keep private document contents out of logs.
* Avoid transmitting document contents to external AI services.
* Provide document deletion controls.
* Validate uploaded files.
* Treat document contents as untrusted input.
* Avoid automatic sharing with external legal-resource websites.
* Document network requirements.
* Clearly disclose unverified privacy properties.

A local AI architecture does not automatically guarantee complete privacy. Runtime behavior, dependencies, temporary files, application logs, and network connections must also be examined.

The project should document its actual data flows and limitations.

---

## ⚠️ Limitations

Dark Lands is intended to assist with preliminary document understanding.

Its results may be affected by:

* Poor-quality scans.
* Incorrect or incomplete text extraction.
* Complex legal terminology.
* Ambiguous contractual language.
* Unsupported languages or model limitations.
* Missing context.
* Jurisdiction-specific legal requirements.
* Model-generated errors.

A document may refer to laws or circumstances that cannot be established from its text alone.

The application must distinguish document evidence from interpretation and uncertainty.

A lack of detected concerns does not establish that a contract is safe.

---

## 🗺️ Roadmap

The following roadmap describes intended development priorities. Completion depends on implementation and testing.

* [ ] Repository setup and architecture documentation.
* [ ] Responsive landing page and dashboard.
* [ ] PDF and TXT document upload.
* [ ] Local document extraction.
* [ ] Local Gemma model integration.
* [ ] Source-grounded document analysis.
* [ ] Citation verification.
* [ ] Clause Compass.
* [ ] Document Transparency Map.
* [ ] Personal Obligation Timeline.
* [ ] Ask My Document.
* [ ] Document Comparison.
* [ ] English, Hindi, Kannada, Telugu, and Tamil interface.
* [ ] Dark mode and light mode.
* [ ] Legal Resource Connect.
* [ ] Privacy Centre and deletion controls.
* [ ] Offline processing verification.
* [ ] Automated security and regression tests.
* [ ] Installation and contribution documentation.

Update the checklist as features are implemented and verified.

---

## 🤝 Contributing

Contributions are welcome.

You can help by:

* Reporting bugs.
* Improving the user interface.
* Improving document extraction.
* Testing local AI inference.
* Improving language translations.
* Adding automated tests.
* Reviewing security and privacy behavior.
* Improving documentation.
* Suggesting accessibility improvements.

### Contribution Workflow

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Run the available tests.
5. Review your changes for accidentally included secrets or private documents.
6. Submit a pull request describing the changes.

Please avoid submitting confidential legal documents, credentials, or personal information in issues, commits, or test fixtures.

---

## 📜 License

The project's licence should be specified in the repository's `LICENSE` file.

Before publishing, verify the licence compatibility of the source code, dependencies, and selected AI model.

Do not claim that the project uses a particular open-source licence until the corresponding licence file has been added.

---

## ⚖️ Disclaimer

Dark Lands is designed to provide preliminary explanations of legal documents for informational purposes.

It is not a substitute for a qualified lawyer or professional legal advice.

The application cannot guarantee that a document is legally valid, enforceable, complete, or safe.

Legal outcomes depend on applicable law, jurisdiction, facts, and circumstances. Consult a qualified legal professional when making important legal decisions.

---

## 🌑 Dark Lands

**Understand Before You Sign.**

Building a more accessible, transparent, and privacy-conscious way to understand legal documents.

*Open source. Evidence-focused. Privacy-first by design.*
