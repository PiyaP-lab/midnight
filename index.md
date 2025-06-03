# Data Science Portfolio 
---
## EDA Project

### Lending Club Case Study
 Used the concepts of EDA to decipher which types of customers default on a loan

 <img width="974" alt="image" src="https://github.com/user-attachments/assets/df1de603-a09b-4e74-84fa-80ddc1571700" />


 [![View on GitHub](https://github.com/PiyaP-lab/MachineLearning/blob/test_branch/LendingClubCaseStudy/PiyaliPodder.ipynb)

## Machine learning

### Bike Sharing Model

Build a multiple linear regression model for the prediction of demand for shared bike
<img width="567" alt="image" src="https://github.com/user-attachments/assets/add1a5dd-259d-4fa7-be8c-0b3e3e3f33a0" />


### Housing Model
Build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
<img width="772" alt="image" src="https://github.com/user-attachments/assets/d4c58c3f-e38e-43ce-9d60-76e0a0cd0260" />


### Feature Generation using RAG 
Built a secure RAG pipeline using in-house OpenAI Langchain stack and Streamlit to auto-generate Gherkin test cases from Squash API data.

<img width="938" alt="image" src="https://github.com/user-attachments/assets/fb79655a-26fe-4c47-b57e-b85c7f3e9c80" />


# Automation Testing Portfolio

## Behave Project using Selenium and Python for UI and API

 ### Internal Domino Data Lab environment automation
   
  #### UI Automation (Selenium + Behave + Page Object Model)
  - Developed a modular test automation framework using Behave (BDD) and Page Object Model (POM) to automate UI workflows in the Domino Data Lab web interface.
  - Automated critical test scenarios including project creation, model training workflows, and workspace management within the Domino platform.
  - Integrated database validation steps using psycopg2 to query Postgres-based metadata stores and validate backend data integrity after UI actions.
  - Implemented parameterized locators using .ini/.py-based locator files for reusable and scalable page object definitions.
  - Enabled dynamic environment-based test execution using .yml configuration, supporting DEV, SIT, and UAT Domino environments.
  - Built custom login and workspace navigation methods in the BasePage class to handle encrypted credentials and session timeouts.
  - Designed reusable test steps for scenarios  like:

          1.Launching a workspace with specific compute resources
          2.Validating Jupyter/VS Code launch success via logs and DB flags
          3.Executing model training pipelines and validating success from both UI and database
          4.Implemented reporting hooks for publishing test results into a centralized test results DB via custom SQL insert queries.
          5.Integrated Allure reporting for visual test case results and historical trend tracking.
          6.Created sanity, smoke, and regression suites to be run in CI pipelines using GitLab.
          7.Configured tests to run on Selenoid Grid for parallel browser execution during overnight runs.
    
  ####  API Automation (Behave + Python Requests + DB Validation)
    - Developed test automation for internal REST APIs used to manage:
           1.Project creation and permissioning
           2.Model deployment (start/stop/check status)
           3.Workspace execution and snapshotting
           4.Validated payloads for model publishing workflows including:
                  - Hardware tier usage limits
                  - Custom Docker environment references
                  -  Git commit  mappings
           5.Verified backend database consistency by connecting to PostgreSQL and asserting job status, artifacts, and logs.
           6.Automated token-based API tests using encrypted credentials from env.json for security compliance.
           7.Generated test evidence and posted results to internal dashboards via APIs.

 #### Performance Testing (Locust + Prometheus + Grafana Integration)
        - Designed and executed performance test scenarios using Locust to simulate high user load on Domino APIs such as:
               1.launch_workspace
               2.execute_model
               3.fetch_job_status

        - Integrated Locust metrics with Prometheus exporters and visualized real-time performance in Grafana dashboards.
        - Embedded performance hooks inside the Behave test framework to trigger load tests conditionally during regression runs.
        - Automated comparison of latency, RPS, and failure rates against SLA thresholds.
        - Enabled Azure Monitor and Log Analytics for extended observability and proactive alerting.
        - Contributed to performance tuning initiatives resulting in 30% improvement in API response times under stress.


    
 ## TDD  project using Selenium and JAVA

 ### Fenergo-Based Application – TDD & Page Object Model (POM) Automation using Moon
   - Implemented automated test coverage for Fenergo's client lifecycle management workflows using Test-Driven Development (TDD) methodology.
   - Worked on a scalable test framework using Page Object Model (POM) in Java with Selenium, improving code reusability and reducing maintenance.
   - Deployed cross-browser UI tests on Moon, enabling efficient test execution across containers in Kubernetes.
   - Developed automation for key Fenergo modules including:

              1.Client onboarding and data collection
              2.KYC and document upload workflows
              3.Regulatory rules validation (MiFID II, FATCA, etc.)
              4.Integrated Cucumber BDD for human-readable test cases aligned with acceptance criteria.
              5.Maintained modular test suites for different entity types (individuals, corporates) and jurisdictions, supporting global compliance workflows.
              6.Enabled parallel test runs on Moon to support nightly and on-demand CI pipelines.
              7.Provided step-level reporting and error diagnostics for test flakiness using Allure and custom logging.
     
 ## BDD(Cucumber) project using Selenium and JAVA & API Automation

  ### Payments-Based Application – Automation for Money Transfer Platform
      - Developed and maintained automated test scripts for a money transfer application using Selenium (Java) and Cucumber BDD, ensuring secure and compliant payment flows.
      - Designed test scenarios covering the full lifecycle of domestic and international money transfers, including initiation, approval, compliance checks, and settlement.
      - Utilized Page Object Model (POM) to create modular and reusable UI test components, improving test stability and maintainability.
      - Automated workflows such as:
                1.Multi-currency transfer setup and FX rate validation
                2.Maker-checker authorization flows for corporate users
                3.Transaction history and receipt generation
                4.Conducted API-level validations for key payment services like initiatePayment, getTransactionStatus, and cancelPayment using **Karate** Framework

    -  Provided detailed reporting through Cucumber HTML reports and integrated alerts for critical test failures.            

