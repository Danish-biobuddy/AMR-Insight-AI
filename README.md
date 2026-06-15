# AMR Insight AI 

> **A premium, high-fidelity bioinformatics web application powered by Gemini for real-time Antimicrobial Resistance (AMR) sequence analysis, mutation tracking, epidemiological surveillance, and automated scientific reporting.**

AMR Insight AI is designed for molecular microbiologists, clinical researchers, and public health agencies to process raw sequencer read representations and academic literature. Using grounded GenAI and specialized analytical widgets, the platform accelerates resistance mechanism identification aligned with ontology standards (CARD, ResFinder), phenotypic CLSI guidelines, and global surveillance vectors.

---

##  Key Subsystems & Features

### 1. Unified Research Dashboard
*   **Isolate Watch**: Real-time status indicators on processed assemblies and high-impact mutation alerts.
*   **Biosafety Controls**: Fast shortcuts to data ingestion, active workbenches, and epidemiological indicators.

### 2. Multi-Format Data Ingestion
*   **Intelligent File Ingest**: Supports uploading or pasting raw formats:
    *   **FASTA** (nucleotide sequence assemblies and clone vectors)
    *   **VCF** (variant mutation tables)
    *   **AST** (phenotypic antibiotic susceptibility testing grids)
    *   **Literature Papers** (PDF manuscripts and journal extracts)
*   **Sandbox Presets**: One-click preset profiles (Enterobacter surveillance assemblies, S. aureus variants, and Neisseria cephalosporin MIC trials) to demonstration pipelines instantly.
*   **Interactive Sequencing Stepper**: Watch pipeline stages live—verifying sequence formatting, extracting base64 payloads, intersecting target referential databases, and compiling reports.

### 3. Integrated Bioinformatics Workdesk
*   **Nucleotide Alignment Map**: Color-coded visualization (Adenine, Thymine, Guanine, Cytosine) of FASTA sequence fragments with active strand search.
*   **Genomic Mutation Catalog**: Filterable SNP records listing chromatic positions, Consequence classes, CARD ontological alignments, and custom Pathogenicity indexes.
*   **Literature Evidence Reader**: Ask inline scientific inquiries regarding literature manuscripts combined with direct context references.
*   **Phenotypic AST Indicators**: Visual charts (via Recharts) mapping MIC distributions across major chemical families, highlighting multi-drug-resistant (MDRE) alerts.
*   **Residue Protein Folding**: Interactive structural viewer demonstrating catalytic omega-loop active pockets (e.g. Glu104Lys Omega Loop, Gly238Ser pockets in TEM Class A beta-lactamase).

### 4. Grounded AI Consultation (Chat)
*   **CARD Reference Grounding**: Converse with a dedicated AMR expert AI, complete with reference citations of uploaded materials.
*   **Actionable Bio-Prompts**: Pre-configured query cards for drug escape pathway tracking, synergistic therapy, and plasmid conjugative transfer risks.

### 5. Automated Scientific Report Vault
*   **AI Synthesis**: Instantly compiles Academic Dossiers, Susceptibility Briefs, or Executive Outlines of multiple selected isolates.
*   **Editorial Suite**: Live print/preview sheets, complete with manual markdown editors and structured section tables.
*   **Dual-Export Channels**: Export results as portable Markdown files or compile print-ready PDFs.

### 6. One Health Global Surveillance Map
*   **Epidemiological Aggregates**: Interactive longitudinal charts tracing MRSA, Carbapenem-Resistant Klebsiella, and rising Colistin-escaping *mcr* vectors across wastewater canal grids, clinical wards, and livestock environments.

---

##  Technology Stack

| Layer | Technologies Used |
|---|---|
| **Frontend UI** | **React 19**, **Vite**, **TypeScript**, **Tailwind CSS**, **Lucide Icons** |
| **Data Engine & Charts** | **Recharts** (Interactive time-series and phenotypic distributions), Direct SVG canvases |
| **Motion & Dynamics** | **Motion** (Smooth tab Transitions and layout fading animations) |
| **Backend Framework** | **Express.js**, Custom ESM to CommonJS compilation via **esbuild** |
| **AI Ingestion Model** | **Gemini Pro / Flash** via `@google/genai` TypeScript SDK |

---

##  Project Architecture

```bash
├── src/
│   ├── components/            # Dedicated modular components
│   │   ├── LandingPage.tsx        # Initial immersive intro screen
│   │   ├── DashboardView.tsx      # Multi-metric dashboard layouts
│   │   ├── UploadWorkspace.tsx    # Multi-format drag/drop area and stepper pipeline
│   │   ├── AnalysisWorkspace.tsx  # Core Bioinformatics Workdesk (FASTA, VCF, AST summaries, Protein Zoom)
│   │   ├── ChatWorkspace.tsx      # Grounded AI Consultation chatbot
│   │   ├── ReportWorkspace.tsx    # Advanced editorial dossier generator
│   │   ├── LibraryWorkspace.tsx   # Searchable archive library
│   │   ├── TrendsWorkspace.tsx    # Epidemiology charts (Line & Bar Recharts)
│   │   └── SettingsWorkspace.tsx  # Secret overrides and theme preferences
│   ├── initialData.ts         # Sample databases and baseline sandbox configurations
│   ├── types.ts               # Shared TypeScript models and definitions
│   ├── main.tsx               # Entry hook
│   └── index.css              # Global styles (Tailwind imports)
├── server.ts                  # Express.js backend & Vite Dev Server integration layer
├── package.json               # Package declarations & scripts
├── metadata.json              # Applet deployment settings
└── README.md                  # System Documentation
```

---

##  Getting Started

### Prerequisites
*   [Node.js](https://nodejs.org/) (Version 18+ recommended)
*   [NPM](https://www.npmjs.com/) 

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/amr-insight-ai.git
   cd amr-insight-ai
   ```

2. Install the system dependencies:
   ```bash
   npm install
   ```

3. Create your `.env` file at the root based on `.env.example`:
   ```bash
   cp .env.example .env
   ```
   Add your standard Google Gemini API key:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

### Running Locally

*   **Development Mode** (Hot reloading & Vite asset routing):
    ```bash
    npm run dev
    ```
    The application will bind and boot on `http://localhost:3000`.

*   **Production Compilation**:
    ```bash
    npm run build
    npm run start
    ```
    This bundles individual TypeScript files into highly optimized production assets in `dist/server.cjs` and `dist/`.

---

##  Biosafety & Data Privacy Notice
All alignments, literature queries, and genomic streams generated in the app remain sandboxed inside the client memory session unless explicitly dispatched to the proxy models. API secrets and model credentials are strictly sequestered from public web contexts.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

