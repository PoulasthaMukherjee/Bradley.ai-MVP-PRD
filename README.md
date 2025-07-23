# [Bradley.ai™](https://bradley-ai-front-end.vercel.app/)
**Product Requirements Document for Bradley.ai MVP**

---

**Author:** Poulastha Mukherjee | 
**Status:** Minimum Viable Product | 
**Updated:** 22.07.2025 | 
**Version:** 1.0

---

## Problem

> **Commercial and Industrial (C&I) businesses face massive friction when evaluating Distributed Energy Resources (DER), with traditional feasibility studies taking months and costing tens of thousands in consulting fees.**

The current DER feasibility analysis process is fundamentally broken:

* **Time-intensive:** Traditional studies require 3-6 months to produce preliminary (30%) designs
* **Capital-intensive:** Upfront consulting fees range from $25K-$100K+ before any real commitment
* **Opaque process:** "Black box" methodology with limited client visibility into analysis
* **Manual & error-prone:** Heavy reliance on manual data collection and spreadsheet-based calculations
* **Limited comparison:** Difficult to evaluate different technology and financing options side-by-side

This friction acts as a major barrier to DER adoption, delaying or preventing cost-saving and environmentally beneficial energy solutions from being implemented across the C&I sector.

---

## Vision & Opportunity

> **Transform months of DER analysis into minutes of AI-powered insights, democratizing access to institutional-grade energy feasibility studies.**

The market opportunity is substantial:

* **$280B+ DER market** projected by 2030 with increasing C&I adoption
* **Soft costs represent 40-60%** of total project development expenses
* **Growing regulatory pressure** for corporate decarbonization and ESG compliance
* **Energy resilience** becoming critical business continuity requirement

> ### Core Value Proposition
> "The first generative AI-powered Expert Agent SaaS solution that analyzes organizational energy consumption profiles and recommends highly optimized DER solutions in hours instead of months."

---

## Target Use Cases

### Primary: C&I Facility Owners/Operators
**Who:** Facility Managers, CFOs, Sustainability Officers, Business Owners
**Goal:** Reduce operational costs, meet ESG targets, improve energy resilience
**Pain:** "The DER evaluation process is a black box that takes months and costs too much upfront"

### Secondary: Energy Analysts/Consultants
**Who:** Internal energy engineers, financial analysts, consulting partners
**Goal:** Efficiently manage project portfolios, deliver quality reports faster
**Pain:** "Manual data collection and custom financial modeling is repetitive and time-consuming"

### Tertiary: Demo/Prospect Users
**Who:** Potential clients evaluating the platform
**Goal:** Understand platform capabilities without commitment
**Pain:** "Need to see the output quality before investing time in data entry"

---

## Proposed Solution

> **An AI-powered, web-based SaaS platform that guides users through intelligent data collection and delivers institutional-grade DER feasibility studies with 30% conceptual designs and financial projections.**

### Top 3 MVP Value Props:

#### 🔋 The Vitamin
Comprehensive DER system analysis covering solar, CHP, storage, fuel cells, and nuclear options with automated specifications and balance of plant design

#### 💊 The Painkiller
Eliminate months of waiting and $50K+ consulting fees - get institutional-grade feasibility study in hours for fraction of traditional cost

#### 💉 The Steroid
AI-powered recommendation engine analyzing thousands of system configurations with real-time financial modeling and decarbonization impact analysis

### Core User Journey
Data Input → AI Analysis → System Design → Financial Model → Report Generation

---

## Technology Stack

#### Frontend Framework
* React 18.2.0
* TypeScript 5.2.2
* Vite 5.2.0

#### UI & Styling
* Material-UI (MUI)
* Tailwind CSS 3.4.3
* React Icons

#### State & Routing
* React Context API
* React Router DOM 6.23.1
* js-cookie (persistence)

#### Development Tools
* ESLint
* Prettier
* React Toastify

### Application Architecture
* **Presentation Layer:** React Components + MUI + Tailwind CSS
* **State Management:** Context API + Specialized Form Contexts
* **Routing & Navigation:** React Router + Role-based Access Control
* **Data Persistence:** Cookie-based Session + Future Backend Integration
* **Future Backend:** AI Analysis Engine + File Storage + Database

---

## Goals & Success Metrics

| Goals | Signals | Metrics | Targets (Y1) |
| :--- | :--- | :--- | :--- |
| **User Engagement** | Users complete workflow | Funnel completion rate<br>Time to complete workflow | >75% completion rate<br><60 minutes average |
| **Business Adoption** | Active paying customers | Monthly active domains<br>Demo-to-client conversion | >500 active domains<br>>15% conversion rate |
| **Platform Utilization** | Report generation volume | Reports generated/month<br>Repeat usage rate | >1000 reports/month<br>>40% repeat usage |
| **Customer Satisfaction** | User feedback quality | Net Promoter Score<br>Support ticket volume | NPS >50<br><5% users need support |

---

## Requirements

Requirements are organized by critical user journeys for the Client workflow (primary use case):

### Authentication & Access Control
| Priority | Requirement | Description |
| :--- | :--- | :--- |
| P0 | Multi-role Authentication | Support Client, Analyst, and Demo user types with role-based routing |
| P0 | Credential-less Demo Access | Immediate demo access via single button click on login page |
| P0 | Session Persistence | Maintain user session and workflow progress across browser sessions |
| P1 | User Registration | New user signup with email validation |

### Client Workflow - Data Collection Journey
| Step | Priority | Key Requirements |
| :--- | :--- | :--- |
| **1. Organizational Profile** | P0 | Company details, industry, annual energy spend, facility operations, address collection |
| **2. Energy Profile** | P0 | Electric/gas bill upload, interval data handling, LOA generation, thermal needs assessment |
| **3. Goals & Priorities** | P0 | Priority ranking (financial vs. environmental), investment goal setting |
| **4. Site Assessment** | P0 | Location confirmation, site characteristics, solar suitability, drawing uploads |
| **5. Financial Information**| P0 | Ownership preference (Own vs. Third-party PPA), financing options, existing contracts |
| **6-7. Processing** | P0 | Data verification status, analysis progress indicators |
| **8. Recommendations** | P0 | Interactive visualizations, financial projections, downloadable reports |

### Navigation & Progress Management
| Priority | Requirement | Description |
| :--- | :--- | :--- |
| P0 | Visual Progress Tracking | Sidebar showing all 8 steps with completion status and current position |
| P0 | Sub-step Navigation | Horizontal stepper showing sub-steps within current main step |
| P0 | Non-linear Navigation | Users can click back to any previously visited step |
| P0 | Conditional Branching | Dynamic form routing based on ownership preference selection |
| P1 | Progress Persistence | Save user progress at each step completion |

### Analyst Dashboard
| Priority | Requirement | Description |
| :--- | :--- | :--- |
| P0 | Project Overview | Dashboard showing all client projects with status and progress |
| P0 | Project Management | Detailed project view with client data and analysis controls |
| P1 | Resource Library | Shared documents and tools for analysts |
| P1 | Account Settings | Analyst profile and preference management |

### Demo Experience
| Priority | Requirement | Description |
| :--- | :--- | :--- |
| P0 | Standalone Demo | Completely isolated demo workflow with no dependencies on client data |
| P0 | Interactive Preview | Editable table with real-time graph updates showcasing analysis capabilities |
| P1 | Demo-to-Client Conversion | Clear call-to-action to transition from demo to full client signup |

---

## Non-Goals
* **Detailed Engineering Design:** Platform provides 30% conceptual designs, not final engineering drawings
* **Project Financing:** Financial projections only; not a financing marketplace or lender platform
* **Construction Management:** Analysis and recommendation only; no project execution tools
* **Multi-site Portfolio Management:** Single facility focus for MVP; portfolio features in future releases
* **Real-time Energy Monitoring:** Feasibility analysis tool, not an operational energy management system

---

## Future Backend Integration Points
While the current implementation is frontend-heavy, the following backend services will need integration:

#### 🔐 Authentication Service
Replace hardcoded credentials with secure user management, JWT tokens, and password recovery

#### 💾 Data Persistence Layer
Database integration for storing user profiles, project data, and analysis results

#### 📁 File Storage Service
Secure upload and storage for utility bills, site drawings, and generated reports

#### 🤖 AI Analysis Engine
Core AI service for DER system optimization, financial modeling, and report generation

---

## Appendix
### Technical Considerations
* **Performance:** Lazy loading of step components to minimize initial bundle size
* **Accessibility:** MUI components provide WCAG compliance foundation
* **Browser Support:** Modern browsers with ES2018+ support
* **Responsive Design:** Mobile-first approach with Tailwind CSS utilities
