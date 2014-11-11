MMLT model readme

Soil respiration data from laboratory incubations are modeled here by a combined flexible exponential temperature response function (Lloyd and Taylor 1994) and Michaelis-Menten type function for microbial biomass carbon and totals soil organic carbon. Soil samples were collected at the same site in February 2011 and July 2011 to capture differences between winter and summer acclimated microbial respiration. Incubations in the lab were conducted at three temperatures: 2, 10 and 22.5 °C, with either sugar addition or as control, for 29 days. Initially, soil underwent 6 treatments encompassing the full factorial combination of temperature by substrate addition. On day 29, each treatment group was split among all possible combinations of temperature by substrate, and a second substrate addition was conducted. Soil respiration was measured from each incubation on day 0 (six hours after substrate addition), day 2, and day 29 (again, 6 hours after substrate addition and temperature change).

Model Overview

See Tucker et al. (2013) Does declining carbon use efficiency explain thermal acclimation of soil respiration with warming? Global Change Biology.

File Contents

model
* Full.Model.odc : this file contains the OpenBUGS model code.
* Full.ModelScript.odc : this file contains the script that will compile the model, load the data and initialize it automatically.

Data
* MBC.day1.txt, MBC.day2.txt, MBC.day29.txt: these files contain microbial biomass carbon (mg C g-1 soil) and total soil (potassium sulfate soluble) organic carbon (mg C g-1 soil), as well as microbial biomass nitrogen (mg N g-1 soil) and total nitrogen (mg N g-1 soil)   for day 0 (pre-incubation), day 2 (immediately post-respiration measurement) and day 29 (immediately pre- second round incubation)

* Resp.day1.txt, Resp.day2.txt, Resp.day3.txt: these files contain incubation respiration (mg CO2-C g-1 soil hr-1) for day 0, day 2 and day 29. In Resp.day1.txt and Resp.day2.txt there are some unnecessary columns (temp.f and treat.f, tp.f and tr.f) which relate to day 29 treatment and temperature but are not used in any way.

Columns are Season (1= winter, 2=summer), Day (remant variable), Initial incubation temperature (day 0-28), final incubation temperature (day 29), initial incubation substrate (day 0-28), final incubation substrate (day 29).

Other
* inits1, 2 and 3.txt : these files contain the initial values  for Ab and Ac to facilitate model convergence for three different mcmc chains.
* Pred.temp.txt: a list of 10 temperature levels at which to predict soil respiration.
