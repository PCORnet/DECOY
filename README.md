# DECOY

Data Entrepreneur Clinical Observables Yardstick

synthetic data for labs, meds, etc.  
a clinical equivalent to DeSYN PUF Files

by Dan Connolly  
under the direction of Russ Waitman, KUMC Director of [Medical Informatics](http://www.kumc.edu/ea-mi/medical-informatics.html)

Copyright (c) 2015 University of Kansas Medical Center  
Share and enjoy under the terms of the Apache License, Version 2.0

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

## Acknowledgements

This work was supported by a CTSA grant from NCRR and [NCATS][] awarded
to the University of Kansas Medical Center for [Frontiers: The
Heartland Institute for Clinical and Translational Research][FRONTIERS] #
UL1TR000001 (formerly #UL1RR033179). The contents are solely the
responsibility of the authors and do not necessarily represent the
official views of the NIH, NCRR, or NCATS.

[NCATS]: http://www.ncats.nih.gov/
[Frontiers]: http://frontiersresearch.org/

It's based on HERON, i2b2, and GPC:

  - [Expressing observations from electronic medical record flowsheets in an i2b2 based clinical data repository to support research and quality improvement.](http://www.ncbi.nlm.nih.gov/pubmed/22195209)
    Waitman LR1, Warren JJ, Manos EL, Connolly DW.
    AMIA Annu Symp Proc. 2011;2011:1454-63. Epub 2011 Oct 22.
  - [Serving the enterprise and beyond with informatics for integrating biology and the bedside (i2b2).](http://www.ncbi.nlm.nih.gov/pubmed/20190053)
    Murphy SN, Weber G, Mendis M, Gainer V, Chueh HC, Churchill S, Kohane I.
    J Am Med Inform Assoc. 2010 Mar-Apr;17(2):124-30. doi: 10.1136/jamia.2009.000893.
  - [The Greater Plains Collaborative: a PCORnet Clinical Research Data Network](http://jamia.bmj.com/content/21/4/637.full)
    Lemuel R Waitman, Lauren S Aaronson, Prakash M Nadkarni, Daniel W Connolly, James R Campbell
    J Am Med Inform Assoc 2014;21:637-641 doi:10.1136/amiajnl-2014-002756


