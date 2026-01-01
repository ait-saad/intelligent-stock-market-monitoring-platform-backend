# Plan du Rapport de Stage
## AI-Assisted DevSecOps Integration for an Intelligent Stock Market Monitoring Platform

---

## Page de Garde
- Titre du projet
- Auteurs : AIT TALEB Saad, ETTALBI Omar, AKOUR Ayoub
- Encadrement : Pr. SADKI Souad
- Date : 11/07/2025
- Institution

---

## Résumé Exécutif
- Contexte du projet
- Objectifs principaux
- Méthodologie adoptée
- Résultats clés
- Contributions principales

---

## Table des Matières

---

## Liste des Figures et Tableaux

---

## Liste des Abréviations
- CI/CD, SAST, DAST, SCA, OWASP, LLM, etc.

---

## CHAPITRE 1 : INTRODUCTION GÉNÉRALE

### 1.1 Contexte et Problématique
- Importance de la sécurité dans le développement logiciel
- Défis de l'intégration DevSecOps
- Complexité des rapports de sécurité multi-outils
- Besoin d'automatisation et d'intelligence artificielle

### 1.2 Objectifs du Projet
- Objectif principal : Intégration DevSecOps avec assistance IA
- Objectifs spécifiques :
  - Automatiser les tests de sécurité (shift-left)
  - Normaliser les rapports de sécurité
  - Générer des politiques et playbooks avec IA
  - Assurer la traçabilité complète

### 1.3 Méthodologie de Travail
- Approche DevSecOps
- Méthodologie agile
- Outils et technologies utilisés

### 1.4 Structure du Rapport
- Présentation des chapitres

---

## CHAPITRE 2 : ÉTAT DE L'ART

### 2.1 DevOps et DevSecOps
- 2.1.1 Définition et principes DevOps
- 2.1.2 Evolution vers DevSecOps
- 2.1.3 Shift-Left Security
- 2.1.4 Avantages et défis

### 2.2 CI/CD et Automatisation
- 2.2.1 Intégration continue (CI)
- 2.2.2 Déploiement continu (CD)
- 2.2.3 Jenkins comme orchestrateur
- 2.2.4 Pipeline as Code

### 2.3 Tests de Sécurité
- 2.3.1 SAST (Static Application Security Testing)
- 2.3.2 DAST (Dynamic Application Security Testing)
- 2.3.3 SCA (Software Composition Analysis)
- 2.3.4 Container Security
- 2.3.5 Secrets Detection

### 2.4 Containerisation et Orchestration
- 2.4.1 Docker et ses avantages
- 2.4.2 Docker Registry et gestion d'images
- 2.4.3 Bonnes pratiques de sécurité

### 2.5 Intelligence Artificielle en Sécurité
- 2.5.1 LLMs (Large Language Models)
- 2.5.2 Applications en cybersécurité
- 2.5.3 Génération de politiques automatisées
- 2.5.4 Limites et considérations éthiques

### 2.6 Frameworks de Gouvernance
- 2.6.1 NIST Cybersecurity Framework
- 2.6.2 ISO 27001
- 2.6.3 Alignement réglementaire

---

## CHAPITRE 3 : ANALYSE ET CONCEPTION

### 3.1 Analyse des Besoins
- 3.1.1 Besoins fonctionnels
- 3.1.2 Besoins non fonctionnels
- 3.1.3 Contraintes techniques

### 3.2 Architecture Globale du Système
- 3.2.1 Vue d'ensemble
- 3.2.2 Composants principaux
- 3.2.3 Flux de données
- 3.2.4 Interactions entre modules

### 3.3 Conception du Pipeline DevSecOps
- 3.3.1 Phases du pipeline
- 3.3.2 Stages parallèles et optimisation
- 3.3.3 Points de contrôle (gates)
- 3.3.4 Gestion des échecs

### 3.4 Conception de la Normalisation
- 3.4.1 Problématique des formats hétérogènes
- 3.4.2 Schéma de données unifié
- 3.4.3 Processus de transformation
- 3.4.4 Standardisation des sévérités

### 3.5 Conception du Module IA
- 3.5.1 Sélection des modèles LLM
- 3.5.2 Architecture du système IA
- 3.5.3 Prompt engineering
- 3.5.4 Génération de politiques et playbooks

### 3.6 Diagrammes de Conception
- Diagrammes de séquence
- Diagrammes de composants
- Diagrammes de déploiement

---

## CHAPITRE 4 : IMPLÉMENTATION

### 4.1 Fondations DevOps et Outils de Base
- 4.1.1 Configuration Jenkins
  - Installation et configuration
  - Plugins essentiels
  - Gestion des credentials
- 4.1.2 Pipeline CI/CD
  - Jenkinsfile et syntaxe déclarative
  - Stages parallèles
  - Tags déterministes
- 4.1.3 Containerisation
  - Dockerfiles optimisés
  - Images applicatives et AI processor
  - Push vers Docker Hub
- 4.1.4 Observabilité avec Grafana
  - Annotations de build
  - Compteurs de sévérité
  - Statut des gates
  - Configuration des dashboards
  - Métriques temps réel

### 4.7 Déploiement Cloud sur Azure
- 4.7.1 Architecture Cloud
  - Conception de l'architecture Azure
  - Ressources provisionnées (VMs, AKS, etc.)
  - Réseautage et sécurité
  - Groupes de ressources et organisation
- 4.7.2 Azure DevOps CI/CD
  - Migration du pipeline Jenkins vers Azure DevOps
  - Configuration des pipelines YAML
  - Agents de build Azure
  - Intégration avec Azure Repos
  - Service Connections et authentification
- 4.7.3 Azure Container Registry (ACR)
  - Configuration du registry
  - Push et pull d'images
  - Scanning de sécurité intégré
  - Gestion des tags et versioning
  - Intégration avec AKS
- 4.7.4 Sécurité et Gouvernance Azure
  - Azure Key Vault pour secrets
  - RBAC et gestion des accès
  - Azure Policy
  - Network Security Groups
- 4.7.5 Monitoring et Observabilité
  - Azure Monitor intégration
  - Log Analytics
  - Application Insights
  - Alerting et notifications

### 4.2 Pipeline de Tests de Sécurité
- 4.2.1 Détection de secrets (Gitleaks)
  - Configuration
  - Règles personnalisées
  - Intégration au pipeline
- 4.2.2 SAST avec Semgrep
  - Règles Python
  - Analyse statique du code
  - Reporting
- 4.2.3 SCA avec OWASP Dependency-Check
  - Scan des dépendances
  - Base de données NVD
  - Analyse des vulnérabilités
- 4.2.4 Sécurité des conteneurs avec Trivy
  - Scan d'images Docker
  - Détection de CVEs
  - Meilleures pratiques
- 4.2.5 Quality Gate avec SonarQube
  - Métriques de qualité
  - Seuils de sécurité
  - Intégration continue
- 4.2.6 DAST avec OWASP ZAP
  - Déploiement éphémère
  - Health check (port 8000)
  - Scan dynamique
  - Fallback nginx (port 8001)

### 4.3 Security Gates et Gestion des Résultats
- 4.3.1 Logique de décision
  - Block / Alert / Tolerate
- 4.3.2 Seuils configurables
- 4.3.3 Mécanismes de contournement (overrides)

### 4.4 Normalisation des Rapports
- 4.4.1 Formats d'entrée
  - JSON (SonarQube, Trivy, Semgrep, Gitleaks)
  - XML (Dependency-Check)
  - HTML/XML (ZAP)
- 4.4.2 Script de normalisation
  - Parsing des différents formats
  - Transformation en JSON unifié
  - Standardisation des sévérités
- 4.4.3 Classification par catégories
  - data_protection
  - input_validation
  - cryptography
  - access_control
- 4.4.4 Déduplication et corrélation
  - Identification des doublons
  - Fusion des résultats
  - Conservation du contexte

### 4.5 Intégration de l'Intelligence Artificielle
- 4.5.1 Choix des modèles LLM
  - DeepSeek R1 67B (principal)
  - LLaMA 3.3 70B (comparaison)
  - CodeLlama 7B (fallback)
- 4.5.2 Script d'intégration IA
  - Architecture du module
  - Gestion des appels API
  - Traitement des réponses
- 4.5.3 Prompt Engineering
  - Structure des prompts
  - Contexte de sécurité
  - Instructions spécifiques
- 4.5.4 Génération de politiques
  - Prompts NIST CSF
  - Prompts ISO 27001
  - Adaptabilité aux frameworks
- 4.5.5 Génération de playbooks
  - Étapes de remédiation
  - Exemples de code
  - Bonnes pratiques

### 4.6 Traçabilité et Artefacts
- 4.6.1 Archivage des rapports
- 4.6.2 Génération des rapports HTML
  - Executive Summary
  - Policy Cards
  - Playbooks
  - Mapping de traçabilité
- 4.6.3 Versioning et historique

---

## CHAPITRE 5 : RÉSULTATS ET VALIDATION

### 5.1 Déploiement et Exécution
- 5.1.1 Vue du pipeline Jenkins
- 5.1.2 Durée d'exécution des stages
- 5.1.3 Taux de succès

### 5.2 Rapports de Sécurité Générés
- 5.2.1 Gitleaks : gitleaks-report.json
- 5.2.2 Semgrep : semgrep-report.json
- 5.2.3 Dependency-Check : dependency-check-report.json
- 5.2.4 Trivy : trivy-report.json
- 5.2.5 ZAP : zap-report.json
- 5.2.6 SonarQube : sonar-issues.json

### 5.3 Rapports IA Générés
- 5.3.1 Executive Security Summary
- 5.3.2 Policy Cards
  - Authorization/Session Controls
  - Dependencies (SCA)
- 5.3.3 Playbooks de remédiation
  - Fix XSS Example
- 5.3.4 Mapping de traçabilité
- 5.3.5 Appendix par domaine

### 5.4 Analyse des Vulnérabilités Détectées
- Distribution par sévérité
- Distribution par catégorie
- Tendances et patterns

### 5.5 Évaluation de la Qualité des Sorties IA
- Pertinence des politiques générées
- Exactitude des playbooks
- Alignement avec les frameworks

### 5.6 Comparaison Approfondie des Modèles LLM
- 5.6.1 Méthodologie de comparaison
  - Critères d'évaluation définis
  - Métriques quantitatives et qualitatives
  - Protocole de test identique
  
- 5.6.2 Comparaison DeepSeek R1 vs LLaMA 3.3
  - **Qualité des politiques de sécurité**
    - Complétude et exhaustivité
    - Clarté et précision du langage
    - Alignement aux frameworks (NIST CSF, ISO 27001)
    - Pertinence contextuelle
  
  - **Qualité des playbooks de remédiation**
    - Étapes de remédiation (clarté et faisabilité)
    - Exemples de code (syntaxe et bonnes pratiques)
    - Prioritisation des actions
    - Documentation et références
  
  - **Structure et formatage**
    - Organisation de l'information
    - Cohérence du format HTML/Markdown
    - Lisibilité et présentation
  
  - **Compréhension du contexte sécurité**
    - Interprétation des vulnérabilités
    - Identification des risques réels
    - Corrélation entre findings
    - Profondeur de l'analyse
  
  - **Performance et efficacité**
    - Temps de génération
    - Consommation de ressources
    - Stabilité des outputs
    - Taux de réussite
  
  - **Spécificités techniques**
    - Gestion des catégories de vulnérabilités
    - Recommandations spécifiques au langage (Python)
    - Adaptation au contexte de l'application
  
- 5.6.3 Tableaux comparatifs détaillés
  - Tableau 1 : Scores par critère (sur 10)
  - Tableau 2 : Temps de génération moyen
  - Tableau 3 : Analyse qualitative par type de sortie
  
- 5.6.4 Exemples concrets côte-à-côte
  - Exemple 1 : Policy pour XSS (R1 vs LLaMA)
  - Exemple 2 : Playbook pour dépendances vulnérables
  - Exemple 3 : Executive Summary
  - Analyse comparative avec annotations
  
- 5.6.5 Forces et faiblesses de chaque modèle
  - **DeepSeek R1 67B**
    - Points forts identifiés
    - Limitations observées
    - Cas d'usage optimaux
  
  - **LLaMA 3.3 70B**
    - Points forts identifiés
    - Limitations observées
    - Cas d'usage optimaux
  
- 5.6.6 Recommandations d'utilisation
  - Quand utiliser R1
  - Quand utiliser LLaMA
  - Stratégie hybride possible
  - Critères de sélection automatique

### 5.6 Métriques de Performance
- Temps d'exécution total
- Temps par stage
- Optimisations réalisées
- Métriques spécifiques des LLMs

### 5.7 Visualisation et Dashboards Grafana
- 5.7.1 Architecture de monitoring
  - Stack de monitoring déployé
  - Sources de données configurées
  - Intégration avec Jenkins
  
- 5.7.2 Dashboards de sécurité
  - Dashboard principal (Security Overview)
    - Vulnérabilités par sévérité (Critical, High, Medium, Low)
    - Tendances temporelles
    - Distribution par outil de scan
  - Dashboard par catégorie
    - SAST findings
    - DAST findings
    - SCA vulnerabilities
    - Container security issues
  - Dashboard de conformité
    - Status des security gates
    - Taux de succès des builds
    - Métriques de qualité SonarQube
  
- 5.7.3 Alerting temps réel
  - Configuration des alertes
    - Seuils critiques définis
    - Canaux de notification (Email, Slack, etc.)
    - Escalation automatique
  - Règles d'alerte implémentées
    - Détection de secrets exposés
    - Vulnérabilités critiques
    - Échec des quality gates
    - Dégradation de la qualité
  - Gestion des incidents
    - Workflow de réponse
    - Tracking et résolution
  
- 5.7.4 KPIs et métriques clés
  - Métriques de sécurité
    - MTTR (Mean Time To Remediate)
    - Taux de vulnérabilités corrigées
    - Couverture des tests de sécurité
    - Security debt
  - Métriques de performance
    - Durée moyenne du pipeline
    - Taux de succès des builds
    - Fréquence de déploiement
  - Métriques de qualité
    - Code coverage
    - Technical debt ratio
    - Code smells
  - Tableaux de bord exécutifs
    - Vue d'ensemble pour management
    - Tendances et évolutions
    - ROI de la sécurité

- 5.7.5 Captures d'écran et analyses
  - Dashboard principal annoté
  - Exemple d'alerte en action
  - Évolution des métriques dans le temps

---

## CHAPITRE 6 : PERSPECTIVES ET AMÉLIORATIONS

### 6.1 Limitations Actuelles
- Limitations techniques
- Limitations fonctionnelles
- Points d'amélioration identifiés

### 6.2 Perspectives à Court Terme
- 6.2.1 Visualisation Grafana avancée
  - Dashboards de sécurité
  - Alerting temps réel
  - Métriques KPI
- 6.2.2 Amélioration du module IA
  - Fine-tuning des modèles
  - Enrichissement des prompts

### 6.3 Perspectives à Moyen Terme
- 6.3.1 Déploiement sur Azure
  - Architecture cloud
  - CI/CD Azure DevOps
  - Azure Container Registry
- 6.3.2 Extension des tests de sécurité
  - IAST (Interactive Application Security Testing)
  - Fuzzing
  - Pen-testing automatisé

### 6.4 Perspectives à Long Terme
- 6.4.1 Intelligence artificielle avancée
  - Auto-remédiation
  - Apprentissage continu
  - Détection d'anomalies
- 6.4.2 Compliance as Code
- 6.4.3 DevSecOps Maturity Model

### 6.5 Évolution vers la Production
- Scalabilité
- Haute disponibilité
- Monitoring avancé

---

## CONCLUSION GÉNÉRALE

### Synthèse du Travail Réalisé
- Récapitulatif des contributions
- Objectifs atteints

### Apports Techniques et Méthodologiques
- Compétences acquises
- Innovations apportées

### Impact et Valeur Ajoutée
- Pour l'organisation
- Pour la communauté DevSecOps

### Bilan Personnel
- Apprentissages
- Défis relevés
- Expérience acquise

---

## BIBLIOGRAPHIE ET RÉFÉRENCES

### Livres et Publications Académiques

### Articles et Documentation Technique

### Sites Web et Ressources en Ligne

### Outils et Technologies
- Documentation Jenkins
- Documentation Docker
- OWASP Resources
- LLM Documentation

---

## ANNEXES

### Annexe A : Code Source Principal
- Jenkinsfile complet
- Scripts de normalisation
- Scripts IA

### Annexe B : Fichiers de Configuration
- Configuration Jenkins
- Dockerfiles
- Configuration des outils de sécurité

### Annexe C : Exemples de Rapports Complets
- Rapport JSON normalisé
- Policy complète
- Playbook complet

### Annexe D : Captures d'Écran Supplémentaires
- Interface Jenkins
- Dashboards
- Rapports HTML

### Annexe E : Glossaire Technique

---

## Notes de Fin de Document
- Remerciements détaillés
- Contacts et informations complémentaires