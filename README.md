# 🧠 Smart Loan Portal — Built with Adobe Experience Manager (AEM)

Welcome to the official repository of the **Smart Loan Portal**, an enterprise-grade web application built using **AEM 6.5.18** and **Maven Archetype 41**. This project demonstrates modern AEM development practices including core components, Sling Models, MSM (Multi Site Manager), custom dialogs, and dynamic components with real-world use cases like Adaptive Forms and interactive UI.

---

## 🚀 Project Modules & Structure

The project follows the standard AEM Maven multi-module setup:

loanportal/
│
├── core/ → Java code (Sling Models, Servlets, OSGi Services)
├── ui.apps/ → Components, dialogs, clientlibs, page templates
├── ui.content/ → Sample content structure & policies
├── ui.config/ → OSGi configuration files (runmodes: dev, stage, prod)
├── ui.frontend/ → (Optional) React/Vue SPA front-end module (not used)
├── all/ → Builds and deploys all modules as one package
└── dispatcher/ → Dispatcher configuration (Apache & rewrite rules)

---

## 🧰 Key Technologies & Concepts

- **Adobe Experience Manager 6.5.18**
- **AEM Core Components & Editable Templates**
- **Sling Models & Sling Servlets**
- **OSGi Annotations**
- **MSM (Multi Site Manager)**
- **HTL (Sightly) Templating**
- **Custom Client Libraries (JS/CSS)**
- **Dynamic Drop-downs in Dialogs**
- **AEM Adaptive Forms with Fragments & Logic**

---

## 🛠 Build & Deploy Instructions

### ✅ Prerequisites
- JDK 11
- Maven 3.6.3+
- AEM 6.5.18 (Author instance running on `http://localhost:4502`)
- Permissions to install packages (`admin` user)

### 🧪 1. Clean and Build the Project

From the root of the project:

mvn clean install
🚛 2. Deploy All Modules to AEM
cd all
mvn clean install -PautoInstallSinglePackage
This will deploy all the modules (core, ui.apps, ui.content, etc.) to your local AEM instance.

📝 Adaptive Form Structure
This project includes:

📄 Personal Loan Form

🏢 Business Loan Form

🏠 Housing Loan Form

👤 Reusable Personal Details Fragment

💰 Conditional Logic Based on Family Income

💅 Custom CSS for each form (Tech Glass, Valorant Style, Modern Blue)

Form paths inside AEM:

/content/forms/loanportal/personal-loan
/content/forms/loanportal/business-loan
/content/forms/loanportal/housing-loan
🎨 Front-End Enhancements
Each loan form includes its own custom clientlib:

/apps/loanportal/clientlibs/personalform

/apps/loanportal/clientlibs/businessform

/apps/loanportal/clientlibs/housingform

Using:

Modern CSS3

Frosted glass effects

Valorant-inspired UI panels

Conditional visibility styling (e.g. age, marital status logic)

🧠 Dynamic FAQ Component
FAQ dropdown powered by Sling Servlet fetching category pages

Multi-level dynamic dropdown using Coral UI JS and Granite data sources

Sling Model renders selected child Q&A pages dynamically

Component Path:

/apps/heroforge/components/contents/frequentlyAskedQuestions
📂 Git Repository Structure
python-repl

README.md                 ← This file!
.gitignore                ← Standard Maven + AEM ignore patterns
pom.xml                   ← Parent build file
/core                     ← Java logic (models, servlets, osgi)
...
📸 Screenshots (Coming Soon...)

👨‍💻 Author
OM
AEM Developer @ Infodales Tech Solutions
🔗 GitHub: MrChuck07

📄 License
This project is open-sourced under the MIT License — feel free to fork, modify, and use it as your AEM portfolio starter template
