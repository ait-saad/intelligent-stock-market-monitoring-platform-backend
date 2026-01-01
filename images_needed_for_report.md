# Images Needed for the DevSecOps Report

This document lists all the images/diagrams that should be added to the LaTeX report for completeness. Each image corresponds to a specific `\includegraphics` command in the LaTeX file.

## Required Images (In Order of Appearance)

### 1. ENSIAS Logo
- **File name**: `ensias_logo.png`
- **Location**: Same directory as rapport_devsecops_latex.tex
- **LaTeX Reference**: Line in title page
- **Description**: Official ENSIAS logo for the title page
- **Size**: Recommended 300x300px or vector format
- **Usage**: `\includegraphics[width=0.3\textwidth]{ensias_logo.png}`

### 2. Architecture Overview Diagram
- **File name**: `architecture_overview.png`
- **Location**: Same directory as the LaTeX file
- **LaTeX Reference**: Chapter 2 - Architecture Générale
- **Description**: Global system architecture showing DevSecOps pipeline flow
- **Usage**: `\includegraphics[width=0.9\textwidth]{architecture_overview.png}`
- **Elements to include**:
  - Git repository
  - Jenkins CI/CD pipeline
  - Docker build process
  - Security tools integration
  - Docker Hub registry
  - Grafana monitoring
  - AI processing flow

### 3. Jenkins Pipeline Flow
- **File name**: `jenkins_pipeline_flow.png`
- **Location**: Same directory as the LaTeX file
- **LaTeX Reference**: Chapter 2 - Pipeline CI/CD
- **Description**: Detailed Jenkins pipeline stages visualization
- **Usage**: `\includegraphics[width=1.0\textwidth]{jenkins_pipeline_flow.png}`
- **Elements to include**:
  - Sequential pipeline stages
  - Parallel execution branches
  - Security scanning phases
  - Decision gates
  - Artifact generation

### 4. Container Architecture
- **File name**: `container_architecture.png`
- **Location**: Same directory as the LaTeX file  
- **LaTeX Reference**: Chapter 2 - Architecture Multi-Images
- **Description**: Container architecture and deployment strategy
- **Usage**: `\includegraphics[width=0.8\textwidth]{container_architecture.png}`
- **Elements to include**:
  - Application container
  - AI processor container
  - Multi-stage build process
  - Registry integration
  - Volume mounts

### 5. Security Pipeline Overview
- **File name**: `security_pipeline_overview.png`
- **Location**: Same directory as the LaTeX file
- **LaTeX Reference**: Chapter 3 - Pipeline de Tests de Sécurité  
- **Description**: Complete security testing pipeline with shift-left approach
- **Usage**: `\includegraphics[width=1.0\textwidth]{security_pipeline_overview.png}`
- **Elements to include**:
  - Early stage scans (GitLeaks, Semgrep)
  - Build-time scans (Trivy, Dependency-Check)
  - Runtime testing (OWASP ZAP)
  - Security gates
  - Timeline indicators

### 6. Grafana Dashboard Screenshot
- **File name**: `grafana_dashboard_screenshot.png`
- **Location**: Same directory as the LaTeX file
- **LaTeX Reference**: Chapter 6 - Observabilité Grafana
- **Description**: Real Grafana dashboard showing DevSecOps metrics
- **Usage**: `\includegraphics[width=1.0\textwidth]{grafana_dashboard_screenshot.png}`
- **Elements to include**:
  - Security metrics panels
  - Build performance graphs
  - Vulnerability distribution charts
  - Quality gate status
  - Alert indicators

### 7. Azure Architecture Diagram
- **File name**: `azure_architecture_diagram.png`
- **Location**: Same directory as the LaTeX file
- **LaTeX Reference**: Chapter 6 - Déploiement Azure
- **Description**: Complete Azure cloud deployment architecture
- **Usage**: `\includegraphics[width=1.0\textwidth]{azure_architecture_diagram.png}`
- **Elements to include**:
  - Azure Container Instances
  - Azure Container Registry
  - Azure Key Vault
  - Virtual Network topology
  - Storage accounts
  - Monitoring integration
  - Security boundaries

### 2. Architecture Overview Diagram
- **File name**: `architecture_overview.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Global system architecture showing the flow: Code → Jenkins → Docker Images → Docker Hub → Grafana
- **Elements to include**:
  - Git repository
  - Jenkins CI/CD pipeline
  - Docker build process
  - Docker Hub registry
  - Grafana monitoring
  - Flow arrows between components

### 3. Jenkins Pipeline Visualization
- **File name**: `jenkins_pipeline.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Detailed Jenkins pipeline stages as shown in the presentation slides
- **Elements to include**:
  - Start → Checkout → Pre-commit Security
  - Parallel security scans (GitLeaks, Semgrep)
  - Build Images stage
  - Deep security scans (Trivy, Dependency-Check, SonarQube)
  - DAST with OWASP ZAP
  - Normalize Reports → AI Policy Generation
  - Final deployment stages

### 4. Security Pipeline Flow
- **File name**: `security_pipeline_flow.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Detailed security testing pipeline from the presentation
- **Elements to include**:
  - Early Stage: GitLeaks + Semgrep (parallel)
  - Deep Scans: Build Images + SCA/Container/SonarQube (parallel)
  - Runtime Scans: Ephemeral Deploy + DAST
  - Processing: Reports → Normalized JSON → AI

### 5. Container Strategy Diagram
- **File name**: `container_strategy.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Container build and registry strategy
- **Elements to include**:
  - App image build process
  - AI processor image build process
  - Docker Hub registry with tagging strategy
  - Fast rollback mechanism

### 6. Grafana Dashboard Screenshot
- **File name**: `grafana_dashboard.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Grafana visualization interface showing security metrics
- **Elements to include**:
  - Security metrics panels
  - Build time trends
  - Vulnerability severity distribution
  - Quality gate status indicators

### 7. AI Integration Process
- **File name**: `ai_integration_process.png`
- **Location**: Same directory as the LaTeX file
- **Description**: AI processing workflow for policy generation
- **Elements to include**:
  - Normalized vulnerabilities input
  - DeepSeek R1 processing
  - Policy generation output
  - Standards alignment (NIST, ISO)

### 8. Traceability Mapping
- **File name**: `traceability_mapping.png`
- **Location**: Same directory as the LaTeX file
- **Description**: End-to-end traceability from findings to policies
- **Elements to include**:
  - Vulnerability findings from different tools
  - Normalized format
  - AI-generated policies
  - Remediation playbooks
  - Standards mapping

### 9. Azure Deployment Architecture
- **File name**: `azure_deployment.png`
- **Location**: Same directory as the LaTeX file
- **Description**: Cloud deployment architecture on Microsoft Azure
- **Elements to include**:
  - Azure Container Instances
  - Azure Container Registry
  - Azure Key Vault
  - Azure Monitor integration
  - Network topology

## Optional Diagrams

### 10. Tool Purpose Matrix
- **File name**: `tool_purpose_matrix.png`
- **Description**: Visual representation of the security tools matrix from the presentation

### 11. Normalization Process Flow
- **File name**: `normalization_process.png`
- **Description**: Step-by-step normalization process visualization

### 12. Quality Gate Decision Tree
- **File name**: `quality_gate_decisions.png`
- **Description**: Decision flow for security gates (Block/Alert/Tolerate)

## Image Placement Instructions

To add these images to the LaTeX document, replace the placeholder text with:

```latex
\begin{figure}[H]
    \centering
    \includegraphics[width=0.8\textwidth]{image_filename.png}
    \caption{Image description}
    \label{fig:image_label}
\end{figure}
```

## Notes

- All images should be in PNG or PDF format for best LaTeX compatibility
- Recommended resolution: 1920x1080 for screenshots, 300 DPI for diagrams
- Ensure all text in diagrams is readable when scaled to fit the report
- Use consistent color scheme matching ENSIAS branding where appropriate