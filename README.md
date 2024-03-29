# Survival Analysis

## Background

- Survival times are typically follow up times from a defined starting point to the occurrence of a given event.
- Use cases:
  - Beginning of a customer-ship to churning of that customer
  - Issue of credit card to customer to first default
  - Start of an insurance policy to it's first claim
  - Time from starting subscription to churning of a telco subscriber
  - Time in employment until attrition
  - Time from current purchase to next purchase of the same product
- Standard statistical techniques do not apply because the underlying distribution is rarely normal and the data are often "censored"

## Business Questions answered by Survival analysis

- What fraction of present customers will be loyal past a certain time frame?
- At what rate will customer churn or attrite?
- How do particular customer characteristics (often called **covariates**) affect the probability of attrition?
- What is the average time spent in the system of a group of individuals?
- What is the comparative time until attrition between two or more groups?
- When will a customer buy a given product next?
- What is the customer lifetime value (CLTV) based on their past behaviour ad their profile?

## Survival Analysis Techniques

Scenario   | Approaches
-----------|-------------
Single Group | <ul><li>Life Table (Actuarial Estimation)<li>Kaplan-Meier<li>Nelson-Aalen Cumulative Hazard Estimation</ul>
Comparison of Groups | <ul><li>Logrank Test<li>Wilcoxon Test</ul>
Semi-parametric estimation model | <ul><li>Cox proportional hazard model(allows explanatory variables)</ul>
Parametric model (accelerated lifetime model) | <ul><li>Exponential<li>Gompertz distribution<li>Weibull distribution<li>Lognormal distribution<li>Loglogistic distribution</ul>

## Censoring

- Types 
  - Right-censoring
  - Left-censoring
  - Interval-censoring
  - Type I and Type II
  - Random

- How Censoring is Informative?
![Illustration of Censored Data from Balavarca](/figure/SampleCensoredData_From_Balavarca.png)

- Crucial but unavoidable assumption
- Examples:
  - An employee who was terminated by an employer
  - A term-insurance customer who drops out 
  - A customer who dies in a customer-loyalty study
  - A customer of TWC who shift's outside TWC's service area
  
## Example of Hazard Function: The Classic Bathtub Curve

![The Classic Bathtub Curve](/figure/TheClassicBathtubCurve.png)

The lifetime of a population is often described using a graphical representation called the bathtub curve. The bathtub curve consists of three periods:
- an infant mortality period with a decreasing failure rate
- a normal life period or "useful life" with a low and relatively constant failure rate
- wear-out period that exhibits an increasing failure rate
