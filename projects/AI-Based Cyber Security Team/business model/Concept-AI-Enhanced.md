

### **System Architecture**

#### (1) Agent Components
```mermaid
graph TB
    subgraph Core System
        A[AutoPen Agent] -- interacts-with --> B(webapp-vulnerability-detection)
        C[CVE Matching Engine]
    end

    subgraph User Interaction Layer
        D[Dashboard/UI] -- triggers --> E[test-execution]
        F[narrative-chat-interface]
    end

    subgraph Technical Backend
        G[sandbox-creation-service] -- creates --> H[test-sandbox-environment]
        I[scan-agents-container-farm] -- runs --> J(vulnerability-scan-results)
        K[historical-database]
    end
```

```mermaid
graph BT
    %% User interaction
    C[User Input: URL + Parameters] -->|triggers| D[Sandbox Creation/Preparation]

    %% System flow
    A[AI PenTesting Agent] --> B[Enhanced Sandbox]
    B --> L[Reporting Agent]
    D --> B
    B --> F[Collection Agent]
    F --> H[Test Execution Agent]
    H --> I[Testing Results & Observations]
    J[Merged Intelligence Engine] --> K[Data Visualization Layer]
    I --> J

    %% Reused flow made clearer
    C --> D
    I -.-> A
    A -.-> J

    %% Core subgraph
    subgraph "Core Components"
        direction LR
        F --> H
        H --> I
    end

    %% Optional styling section (Mermaid does not support `Style` keyword directly like this)
    %% If you want to style nodes, you need to use the `classDef` and `class` directives

    classDef user fill:#e0f7fa,stroke:#00796b,stroke-width:2px;
    classDef sys fill:#f3e5f5,stroke:#6a1b9a,stroke-width:2px;

    class C,D user;
    class A,B,F,H,I,J,K,L sys;
```

```mermaid
flowchart TD
    %% User interaction
    User["User provides URL, selects test mode"] --> Sandbox["Sandbox environment prepared"]
    User --> AgentScript["Agent scripts tailored to OWASP Top 10 / CUSTOM"]

    %% Sandbox logic
    Sandbox -- "If required" --> OSFingerprint["OS Fingerprinting + Service Detection"]

    %% Execution logic
    AgentScript --> Targets["Scan targets defined"]
    Targets --> Execution["Agent executes test passively on server-side"]
    Execution -- "Captures data" --> Db["Connects to Database / Listserves? (not default)"]
    Execution --> History["Historical database flagged: raw data retained"]

    %% Results
    Execution --> FoundVulnerabilities["Detection of vulnerabilities on target"]
    FoundVulnerabilities --> QandA["Interactive report with Q&A chat"]
```

---
### **Key Features**

1. **Sandbox-Integrated Scanning**
    - Creates fully functional sandbox environments automatically
    - Context-aware vulnerability detection with reasoning capabilities
2. **Adaptive White Hat Testing**
    - NLP-powered test parameter extraction from user input
    - Autonomous agents rewrite penetration tests based on findings
3. **Intelligent Reporting**
	- Interactive report format: 
		- Q&A session interface about vulnerabilities (when user accesses) 
		- Contextual vulnerability explanation including how it was found 
		- Visual context mapping overlaid with attack paths 
			- Example: “Hi, what’s the most dangerous vulnerability on example.com? I heard they’re logging all PII fields?”
4. **Multi-modal Output**
    - Text reports with interactive elements
    - Light debugging session capability view

---

### **Data Model Enhancements**

**Storage Policy:**

```mermaid
graph LR
    G[Scan Execution History] -- customer-approved --> H[1yr Retention]
    I[Historical Database] -- stores --> J[Test Results Metadata]
```

**Data Types:**

- **Findings Database**: Schema-normalized vulnerability data with traceability metadata
    - Web app assessment -> OS fingerprinting -> Service vulnerabilities -> Known CVEs

---
### **Workflow Refinement**

```mermaid
flowchart TB
    subgraph "Customer Interaction"
        A["Submit: https://example.com"]
        B["Initiate test profile"]
    end

    subgraph "AutoPen Engine"
        C(["Scan Initial History?"])
        D{"Yes or No?"}
        D -- "No" --> E["Sandbox Creation"]
        E --> F["Agent dispatches..."]
        F --> G["Execute scan sequence"]
    end

    subgraph "Reporting Layer"
        H["Interactive Explanation"]
        I["Risk Score: 8.2/10"]
    end

    %% Additional flow outside subgraphs
    J["Customer inputs raw vulnerability intelligence"] --> K["Connects to report generation tool without bypassing security controls"]
```

---
### **Competitive Differentiation**

|Feature|Traditional Pentest|AutoPen Agent|
|---|---|---|
|Time to first finding|~30 mins|<5s|
|Understanding context|Requires manual investigation|Automated with interactive Q&A|
|Integration capability|Manual spreadsheet creation|Auto-generated context mapping|

---

### **Security Architecture Considerations**

1. **Sandbox Isolation**:
    
    - Default execution environment uses Docker-in-Docker with network isolation
    - All data flows logged to audit trail
2. **Data Encryption**:
	```mermaid
	graph LR
    G[“Encrypted transit via TLS”] -- passes-by --> H(plaintext-vulnerability-database)

	```
---

### **Requirements Flow Chart**

**Enhanced Workflow:**

```mermaid
flowchart TB

    %% Title is not supported directly in Mermaid, so it's omitted or handled separately in Markdown

    %% Set overall direction
    %% direction LR is not supported inside flowchart TB, use graph LR for left-to-right
    %% Keeping TB as the user wrote but aligning subflows logically

    %% User input and test mode selection
    id1["User Input"] -->|Select test mode:| id2["Testing Modes"]
    id2 --> FullScan["Full Application Assessment"]
    id2 --> OWTFocused["OWTF-focused Scan"]
    id2 --> AdvancedExploitation["Advanced Exploit Testing"]

    %% Sandbox preparation and fingerprinting
    FullScan --> SandboxPrep["Prepare test sandbox"]
    OWTFocused --> SandboxPrep
    AdvancedExploitation --> SandboxPrep

    FullScan --> OSAnalysis["OS Fingerprinting + Service Detection"]
    OWTFocused --> OSAnalysis
    AdvancedExploitation --> OSAnalysis

    %% Agent-driven testing
    SandboxPrep --> AgentDrivenTest["AI-Powered Testing Sequence"]
    OSAnalysis --> AgentDrivenTest

    AgentDrivenTest --> Agents["Agents"]
    Agents -->|run tests| RawFindings["Raw Findings"]

    %% Vulnerability annotation
    RawFindings --> OWASP["OWASP Top 10 Analysis"]
    RawFindings --> NVD["NVD Database Query"]
    OWASP --> AnnotatedVulnerabilities["Annotated Vulnerabilities"]
    NVD --> AnnotatedVulnerabilities

    %% Report generation
    AnnotatedVulnerabilities --> ReportGeneration["Generate Full Assessment"]
    ReportGeneration --> FinalReport["Final Report"]
    FinalReport --> LikelihoodMatrix["Likelihood Matrix"]
```

