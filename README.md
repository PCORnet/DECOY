# DECOY

Data Entrepreneur Clinical Observables Yardstick

synthetic data for labs, meds, etc.  
a clinical equivalent to DeSYN PUF Files

by Dan Connolly  
under the direction of Russ Waitman, KUMC Director of Medical Informatics
 
## Design Sketch

- Take the fact counts on babel and add the places together that report fact counts to create a pooled set of patients and facts at each fact and ontology
- Then distribute them across the patients using different standard distributions.:
  - We’d have “ugly decoy” which uses a uniform distribution but is really useful to do simple unit and integration tests
  - Pink Decoy follow a Poisson Distribution
  - Green DECOY uses a Gaussian
  - Blue DECOY uses Beford
    - related work: by Jason Doctor looking at clinical data distributions and evaluating fraudulent upcoding of diagnoses
- Make them as dirt simple CSV files that mimic the RESDAC files.
  - so that the OMOP people and Sentinetl people can use them too
- Provide the ETL to bring into i2b2.

### Stretch Goal

Evaluate the real distributions and model each type of fact using the most approximate distribution or base on real pooled distributions.
