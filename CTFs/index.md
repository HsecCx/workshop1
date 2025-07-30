---
layout: default
title: CTFs
nav_order: 6
---

# Capture The Flag (CTF) Challenges

Welcome to the Checkmarx CTF series - designed for developers seeking to master secure coding practices and integrate security seamlessly into their development workflow.

## Overview

These CTF challenges help developers understand vulnerabilities from a __development perspective__. All challenges use the same comprehensive vulnerable application and focus on practical skills developers need: identifying security issues in code, understanding remediation techniques, and building security awareness into the development lifecycle.

## Application & Project

For these CTF challenges, you will use the __TotallySecure__ application - a comprehensive vulnerable Java Spring Boot application designed to teach all aspects of secure development:

### __TotallySecure Application__
- __Repository__: `https://github.com/HsecCx/workshop-TotallySecure.git` 
- __Technology__: Java Spring Boot application with comprehensive security challenges
- __Associated Application__: TotallySecure Application (in ASPM)
- __Developer Focus Areas__:
  - __Supply Chain Security__: Dependency vulnerabilities, malicious packages, transitive dependencies
  - __Secure Coding Patterns__: Code vulnerability remediation, real-time security feedback, AI-assisted development

__Why TotallySecure?__ This application contains a rich variety of vulnerability types across multiple security domains (SAST, SCA, configuration), making it perfect for comprehensive developer security training. Both CTF challenges explore different aspects of this same codebase, allowing you to develop deep expertise with one application while learning diverse security skills.

## CTF Challenge Series

The two CTF challenges are designed with progressive difficulty and comprehensive coverage:

| Challenge | Duration | TotallySecure Focus | Skills Developed |
|-----------|------------|----------|-------------------|------------------|
| __Supply Chain Detective__  | 30-45 min | SCA & Dependency Security | Package security, dependency analysis, supply chain awareness, malicious package detection |
| __Vulnerability Hunter__  | 30-45 min | SAST & AI-Enhanced Development | Code vulnerability identification, AI-assisted remediation, plugin mastery, ASCA integration |

## Prerequisites

Before attempting these CTF challenges, developers should have:

- __Completed Labs 1-5__: Foundation knowledge of Checkmarx One platform and tools
- __Access Verification__: Confirmed access to TotallySecure project and its associated application in ASPM
- __Tool Familiarity__: Comfort with VS Code, Checkmarx plugin, and development workflows

## Learning Objectives

Upon completing the CTF series, developers will have demonstrated:

### __Secure Development Skills__
- Vulnerability identification and remediation techniques
- Secure coding pattern implementation
- Real-time security feedback integration with development workflows
- Dependency security and supply chain awareness
- AI-assisted security development with ASCA and Copilot

### __Development Workflow Integration__
- Security tool integration in daily development
- Risk-based development decision making
- Collaborative security practices with teams
- Proactive security mindset in feature development

### __Professional Growth__
- Security-aware development practices
- Effective communication about security risks and solutions
- Prioritization of security work within development cycles
- Integration of AI tools for security enhancement

## CTF Format

Each CTF follows a structured format designed for developer skill building:

- __Scenario Setup__: Real-world development context and challenges
- __Hands-on Phases__: Time-boxed coding and analysis exercises
- __Flag Capture__: Specific deliverables demonstrating secure development skills
- __Development Integration__: How to apply learnings in daily development work

## Setup Instructions

1. __Clone TotallySecure__:
   ```bash
   git clone https://github.com/HsecCx/workshop-TotallySecure.git
   ```

2. __Open in VS Code__ and connect to Checkmarx project:
   - Project: `TotallySecure`
   - Branch: `master`

3. __Verify All Scanners__ are complete:
   - SCA: Enabled ✓
   - SAST: Enabled ✓  
   - ASCA: Real-time feedback ✓
   - ASPM: Dashboard active ✓

4. __Ensure GitHub Copilot__ is installed and active for AI-assisted development

## Complete All CTF Challenges

📋 __[Open Comprehensive CTF Form - All Challenges](https://forms.office.com/r/t1vtEj7BEQ)__

The form includes both progressive challenge sections:
- __Supply Chain Detective__ (SCA & dependency analysis, malicious package detection)
- __Vulnerability Hunter__ (SAST, AI-enhanced development, interface mastery, ASCA integration)

### __Total Experience__
- __Duration__: 1-1.5 hours for all challenges
- __Skills Developed__: Complete security-first development mastery
- __Progression__: Builds from supply chain security to AI-enhanced vulnerability management

{: .note }
These CTF challenges are designed for developers who want to integrate security seamlessly into their development workflow. They simulate real development scenarios where security decisions must be made alongside feature development.

{: .warning }
__Development Context__: These challenges represent real-world scenarios you encounter as a developer. The secure coding practices and security integration techniques learned here directly apply to your daily development work.

---

__Ready to master security-first development? Click the form link above to begin your comprehensive security challenge series!__