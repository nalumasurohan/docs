2-Month Day-Wise Training Plan - Data Engineering & Analytics (Uber Context)
Duration: 8 Weeks | 5 Days per Week
Program Objectives
By the end of 2 months, candidates should be able to:
Confidently navigate Uber internal tools and data ecosystem
Write, debug, and optimize queries using Query Builder, UWORC, Kirby
Design and maintain ETL pipelines using Airflow
Follow Git-based development workflows
Understand incident management and on-call responsibilities
Apply AI/ML concepts and tools for productivity and analytics
Build and publish basic dashboards
Understand code deployment lifecycle and tooling
Training Methodology
Watch Me Code (WMC) – mentor codes live or via recordings
Shadowing – trainees observe mentor performing real tasks
Hands-on Assignments – bench-safe or sandbox-based
Self-Learning Notes – Uber-specific documentation & EngWiki
Mini Assessments – weekly or bi-weekly checkpoints
Mock presentations and interviews  - whenever possible and for whichever.
This training program will be a complete end-to-end evaluated one.

WEEK 1: AI/ML Statistical EDA + Uber Data Ecosystem
Day 1 – Statistics, Variance, Std Dev & Skewness
Goal: Understand the "Spread" of data and predicting continuous numbers.
Program overview, evaluation model
Mean vs Median vs Mode
Normal vs Skewed distributions
Variance & Standard Deviation
Outliers and data spread
Assignment 1: Create a histogram of transaction quantities and explain why the distribution is "Leaning" (Skew).
Deliverable: ML Concept Notes - Statistical Handbook for DE/DA.


Central Tendency (StatQuest): The Mean, Median, and Mode - YouTube  or Statistics Intro (Khan Academy) .
Variance & Std Deviation: Khan Academy: Measures of Dispersion
Skewness & Distributions: Statistics By Jim: Skewed Distributions Guide

Day 2 – Linear Regression Basics
Where AI/ML fits in analytics & DE
Linear Regression & OLS
Residuals
MAE vs RMSE
WMC: df.describe() on CSV; Identify outliers; Regression notebook
Deliverable: Mini Notebook for step-by-step calculation of Variance and a simple Regression plot.


Regression Metrics (MAE/RMSE): Scikit-Learn Official Metrics Documentation
Linear Regression Intro: Scikit-Learn Linear Regression Guide

Day 3 – Data Modeling


Data Modelling Doc - link
PPT - link


Explain the Data modelling process.
What is an Incremental Load? How is it different from Full Load?
Explain Scalability.
Differentiate between Vertical and Horizontal Scaling.
Slowly Changing Dimensions SCD Types 1, 2, 3…)
When to apply Type 1 vs Type 2
Impact on downstream analytics and reporting


Data Lake vs Data Warehouse vs Lakehouse 
Differences in architecture and use cases
Storage formats (Parquet/ORC/Avro/JSON/CSV)
Query engines (Spark, Presto, Hive, Trino)
Where Hudi, Delta, Iceberg fit


What is a Hudi Table?
COW vs MOR
Upserts & Deletes
Incremental queries
Hudi vs traditional warehouse tables


Deliverable: Architecture notes
Assignment 2 : 
Design a Hudi Fact Table with Record key, Partition key, Precombine field
Decide : Which tables should be Hudi, Which should remain standard
Output : Hudi table design document


Data Lake vs Data Warehouse 
What is a Data lakehouse?


Day 4 – Data Architecture
Z-Ordering, File Compaction & Data Skipping
How large files are optimized in data lake tables
Improving query performance by clustering related data
Reducing small file problems
Techniques used by Delta Lake, Iceberg, Hudi for data layout optimization


What are Dimension and Fact Tables? 
Grain of a Fact table
Fact table types : Transactional, Snapshot, Accumulating snapshot
Dimension table characteristics


OLTP vs OLAP
Multidimensional OLAP (MOLAP) and Relational OLAP (ROLAP). Hybrid OLAP (HOLAP)
What is Dimension Modelling?
Measures vs Attributes
Partitioning and Bucketing
Surrogate keys


Deliverable: Architecture notes
Assignment 3 :
Design : fact_sales, dim_customer, dim_product, dim_date
Output: Table structures with keys

Day 5 – EngWiki & Data Discovery
Star, Snowflake and other Schemas 
Advantages
Limitations
WMC: Uber data flow overview
How data flows in Uber
What all different types of projects we have in Uber
Business context: Products, Marketplace, Ops, Finance, Eats, Mobility
EngWiki navigation (how to search effectively)
Understanding table ownership & data contracts (Databook) 
Common Uber schemas
List of commonly used schemas & tables [Trips, Driver, Courier, Eats related data]


Deliverable: Architecture notes & Uber data domains
Assignment 4 : 
Design a complete dimensional model with Fact & Dimension tables, Star or Snowflake schema and mark Hudi tables
Explain data flow : Initial load & Incremental updates
Output : Final schema diagrams + Hudi design explanation + Table definitions + Short written summary


WEEK 2: AI/ML Classification, Deep Learning + Query Builder & UWORC
Day 6 – Logistic Regression & Decision Trees
Goal: Predicting categories and understanding "Logic Gates" in AI.
Logistic Regression (Sigmoid Function) and Decision Trees (Information Gain)
Evaluation: Accuracy, Precision, Recall, and the F1-Score
Confusion Matrix pitfalls
Binary classification use cases
WMC: Churn classifier
Deliverable: A Decision Tree visualization showing the "Splits" (e.g., If Spend > $50 -> High Value).
Assignment 5 : Interpret a Confusion Matrix. Explain why 95% accuracy is a failure if you miss all high-risk cases.

Logistic Regression (StatQuest): Logistic Regression Clearly Explained
Decision Trees (StatQuest): Decision Trees Clearly Explained
Confusion Matrix (Data School): Simple Guide to the Confusion Matrix
Precision & Recall: Google Machine Learning Crash Course: Precision/Recall



Day 7 & 8 – Analytical Queries & Optimization
Topic: Writing Analytical Queries – Fundamentals (doc Learning)
Concepts
Analytical vs transactional queries
Fact & Dimension join patterns
Aggregations:
SUM, COUNT, AVG
GROUP BY rules
WHERE vs HAVING
ORDER BY vs window functions
Topic: Core Analytical Queries (Hands-On)
Assignment 6a : 
Daily sales
Monthly revenue
Top 10 products by revenue
Customer-wise sales
Region-wise sales contribution
Focus Areas
Correct joins
Proper GROUP BY
Meaningful aliases
Topic: Advanced Analytical Queries
Concepts
Window functions:
ROW_NUMBER, RANK
Running totals
Subqueries vs CTEs
CASE WHEN logic
Assignment 6b : 
Top 3 products per category
Running total of revenue
Month-over-month growth
Topic: Optimize Slow Queries
Concepts
Why queries become slow:
Full table scan
Large joins
Wrong filters
EXPLAIN plan (Hive/Presto)
Partition pruning
Predicate pushdown
Join order optimization
 Assignment 6c : 
Analyze 3 slow queries
Identify performance issues
Rewrite queries for optimization
Topic: Query Optimization Best Practices
Concepts
Avoid SELECT *
Use correct join types
Filter early
Reduce data scanned
Use partitions & statistics
Avoid unnecessary DISTINCT
Assignment 6d : 
Optimize previously written queries
Compare logic before vs after
Assignment 6 Final Deliverables :
basic_analytics.sql (5 queries)
advanced_analytics.sql (3 queries)
optimized_queries.sql (6–8 queries)
 Short Documentation
Query purpose
Optimization applied
Expected output

Day 9 & 10 – Neural Network Basics, ML Audits and Data Leakage, Overfitting + Watch Me Code on QB and uWORC
Goal: Understanding Neural Networks and avoiding the "Garbage In, Garbage Out" trap.
Neural networks architecture (Input, Hidden, and Output layers)
Audits: Data Leakage (Cheating with future data) and Overfitting.
Activation functions
ML Audits - GIGO principle and Model trust checklist.
Data leakage examples and overfitting detection.
WMC: Building a basic 2-layer "Brain" in a local notebook.
Assignment 7 : Audit a provided "Perfect Model" (100% accuracy) and find the "Cheat Feature" (Data Leakage).
Deliverable Audit Checklist: 5 things every DE/DA must check before trusting a model.

Neural Networks (3Blue1Brown):What is a neural network?
Activation Functions: Activation Functions in Deep Learning
Data Leakage: Data Leakage in Machine Learning (Machine Learning Mastery)

Query Builder UI & use cases
Execution engines supported at Uber
Writing production-style queries
Datacentral (watching
UWORC fundamentals 
Alerting, Tiering, Owner, LDAP
Query execution & logs (Trace)
Backfill pipelines

WEEK 3: Unix Commands + Project + Kirby Debugging

Day 11 – Unix Commands Doc 

File System Navigation: 
Commands like ls, cd, and pwd for navigating directories.


File Management:
 Commands such as cp, mv, and rm to copy, move, and delete files, as well as mkdir to create directories.


Text Processing:
 Commands like cat, grep, head/tail, and sort for viewing and manipulating text file content.


Permissions and Ownership: Commands like chmod and chown for managing file and directory permissions and ownership.


Process Management: Commands such as ps, top/htop, and kill to monitor and control running programs.


System Administration: Commands like df, du, uname, and man for managing the system, including disk usage and obtaining system information.


Networking: Commands such as ping, ssh, scp, and wget/curl for network tasks like testing connectivity and transferring files.


Compression and Archiving: Commands like tar to archive files and gzip/gunzip to compress and uncompress them.



Day 12, 13 and 14 – Python & SQL Project + Mock Interviews
Banking Application - link 
Student Management System - link
Employee Management System - link
Super Market Bill Generation - link (short)
Expense Tracker - link (short)

Day 15 – Kirby Fundamentals Doc + Project Presentation
Kirby basics
Table Lineage & Dependencies
Debugging data issues
How to identify upstream/downstream impacts

WEEK 4: ML Tuning + Business Context
Day 16 – Bias vs Variance & Cross Validation
Bias-Variance tradeoff - Underfitting vs Overfitting; Learning curves (train vs validation); Model complexity vs generalization; Practical examples (tree depth, regularization) - https://ml-cheatsheet.readthedocs.io/en/latest/bias_variance.html


Model stability & Robustness - Sensitivity to data changes; Random seed impact; Stability across folds/time windows; Drift vs noise


Overfitting Control (Shadowing + Regularization) - L1/L2 regularization; Early stopping; Dropout (NN); Pruning (trees); Ensembling (bagging, boosting)


Cross validation techniques - K-Fold, Stratified K-Fold; Time-series CV (important for analytics); Grouped CV (user-based data); Nested CV (for hyperparameter tuning)
https://scikit-learn.org/stable/modules/cross_validation.html


Hyperparameter Tuning - Grid Search vs Random Search; Bayesian Optimization (Optuna, Hyperopt); Automated ML (AutoML); Search space design; Cost vs accuracy tradeoffs - https://www.jeremyjordan.me/hyperparameter-tuning/


Model evaluation - 
Classification: Precision, Recall, F1, ROC-AUC, PR-AUC
Regression: RMSE, MAE, R², MAPE
Business metrics mapping (KPIs)


Data Leakage & Validation Pitfalls - Train-test contamination; Target leakage; Temporal leakage; Feature leakage from pipelines


Assignment 8 : Notes practical checklist:
How to detect overfitting
How to tune models safely
Validation best practices for pipelines

Day 17 – ML in Data Engineering vs Data Analytics + ML in Pipelines vs Reports
ML in Data Engineering (DE) Focus: scalability, reliability, automation.
Examples:
Feature pipelines
Real-time inference systems
Data validation models
Anomaly detection in pipelines
Recommendation systems infra
Model deployment & monitoring
Tuning focus:
Latency vs accuracy
Model size vs cost
Retraining frequency
Pipeline optimization
ML in Data Analytics (DA) Focus: insights, decision-making, interpretability.
Examples:
Forecasting (sales, demand)
Customer segmentation
Churn prediction
A/B testing models
BI + ML integration
Tuning focus:
Explainability vs performance
Metric alignment with business goals
Feature interpretability
Model simplicity vs accuracy
ML in Pipelines
Automated decisions
Continuous training
MLOps integration
SLA & reliability constraints
ML in Reports
Batch predictions
BI dashboards
Offline modeling
Human-in-the-loop
ML Tuning in Data Pipelines 
Topics:
Feature engineering tuning
Sampling strategies
Class imbalance handling
Data volume vs model performance
Feature selection methods
Pipeline-level optimization
Assignment 9: Comparison notes + architecture diagrams:
DE vs DA ML architecture
Tuning checklist for pipelines
Real-world use cases

Day 18 & 19 – Business Metrics  Doc
Understand Uber’s core business KPIs
Translate vague business questions into clear, measurable metrics
Map business asks → facts → dimensions
Define KPI logic at a conceptual / SQL-ready level
Understanding Uber’s Business Model
Two-sided marketplace: Riders, Drivers
Supply vs Demand dynamics
Trip lifecycle: Request → Match → Pickup → Trip → Completion/Cancel
Key entities: Trip, Rider, Driver, City, Time
Output: Business flow diagram + fact events identification
Core Uber KPIs
 Rider KPIs : Trip requests, Completed trips, Rider cancellation rate, Average wait time, Trip frequency per rider
Driver KPIs : Active drivers, Driver utilization rate, Earnings per trip, Driver acceptance rate, Driver cancellation rate
Marketplace KPIs : Matching rate,Fulfillment rate,Supply–demand ratio,Surge frequency
Assignment 10 : For each KPI, identify - 
Metric definition
Grain (trip / driver / rider / time)
Dimension dependencies (city, time, driver type, etc.)
Output : KPI Definition Table
Translating Business Asks → KPIs
Common Business Asks
“Why are rides getting slower in Bangalore?”
“Drivers are churning in Mumbai — why?”
“Why is revenue down this week?”
Translation Framework
Clarify the metric
Identify the time window
Choose relevant dimensions
Define success vs failure
Decide the aggregation level
Example: Business Ask: “Why are cancellations increasing?”
Translated Metrics
Rider cancellation rate
Driver cancellation rate
Breakdown by : City, Time of day, Driver tenure
Assignment 11 : Translate 5 vague business asks into clear KPI definitions.
KPI Logic & Analytical Thinking
Concepts
Numerator vs denominator clarity
Event-based vs snapshot metrics
Leading vs lagging indicators
Ratios vs absolute metrics
Example KPI Logic
Fulfillment Rate : Completed Trips / Trip Requests
Driver Utilization: Time on Trip / Time Online
Assignment 12 : Write logical definitions (formula or pseudo-SQL) for - Fulfillment rate, Average pickup time and Driver utilization
Output : KPI Calculation Document
Validation Checks
Does the trend make business sense?
Can the KPI exceed 100%?
Is the denominator stable and meaningful?
Assignment 13 : Review incorrect KPI definitions + Fix logic and explain corrections
Assignment 14 : “Uber leadership wants to improve trip fulfillment during peak hours.”
Identify relevant KPIs
Define metrics clearly
Choose dimensions
Propose an analysis approach
Deliverable : KPI list, Metric definitions, Analysis plan

Day 20 – Final Foundations Review
Final ML presentation
Pending Project submissions
Week 1–4 evaluation

WEEK 5: ETL & Orchestration Fundamentals
Day 21 – ETL Concepts
ETL in Uber context
Data sources & sinks
Deliverable: Notes

Day 22 – Batch vs Streaming
Batch vs streaming tradeoffs
Hybrid pipelines
Deliverable: Comparison doc

Day 23 – Uber Pipeline Architecture
Current & future architecture
Incremental processing
Deliverable: Architecture notes

Day 24 – Simple ETL Flow
WMC: Simple ETL pipeline
Assignment kickoff
Deliverable: ETL diagram

Day 25 – ETL Design Review
Design walkthrough
Feedback & evaluation
Deliverable: ETL design doc

WEEK 6: Airflow & DAG Design
Day 26 – Airflow Architecture
DAGs, operators, tasks
Scheduling & retries
Deliverable: Notes

Day 27 – Writing DAGs
WMC: Basic DAG
Sandbox practice
Deliverable: Sample DAG

Day 28 – Production DAG Review
Shadowing: Real DAG
Best practices
Deliverable: Review notes

Day 29 – DAG Optimization
Dependencies
Backfills & SLAs
Assignment: DAG design
Deliverable: Design doc

Day 30 – Peer Review
PR-style review
Weekly assessment
Deliverable: Dependency diagram

WEEK 7: Git, Incidents & Prompt Engineering
Day 31 – Git Fundamentals
Git basics
Branching strategies
WMC: Git workflow
Deliverable: Repo setup

Day 32 – PRs & Reviews
Code reviews
Responding to comments
Assignment: Create PR
Deliverable: Sample PR

Day 33 – Incident Management
Incident lifecycle
On-call expectations
Shadowing: RCA walkthrough
Deliverable: RCA doc

Day 34 – Prompt Engineering
Prompt best practices
AI limitations
WMC: Prompt refinement
Deliverable: Prompt set

Day 35 – Cursor & AI Tools
Cursor for coding/debugging
AI for documentation
Weekly assessment
Deliverable: Prompt library

WEEK 8: Visualization & Deployment
Day 36 – Visualization Basics
Dashboard principles
Data modeling
Deliverable: Design sketch

Day 37 – Dashboard Build
WMC: End-to-end dashboard
Assignment: Build dashboard
Deliverable: Dashboard draft

Day 38 – Dashboard Review
Storytelling & best practices
Publish dashboard
Deliverable: Final dashboard

Day 39 – Deployment Lifecycle
Uber deployment flow
Validation & rollback
WMC: Deployment walkthrough
Deliverable: SOP

Day 40 – Final Assessment
End-to-end review
Feedback session
Final outputs submission

FINAL OUTPUTS
Query & DAG repository
ETL & Airflow design docs
Dashboard demo
Deployment SOP & flowchart
Production & on-call readiness



