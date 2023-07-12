# JSONPath

1. Find demands where the payer is a resident of street A and B

$.Demands[?(@.payer.address.street=='A' || @.payer.address.street=='B')]


2. Find demands where the payer is a resident of street A and identifies themself as FEMALE

$.Demands[?(@.payer.address.street=='A' && @.payer.gender=='FEMALE')]


Find demands whose payer has the id 34231 and mobile number as 7878787878

$.Demands[?(@.payer.id==34231 && @.payer.mobileNumber=="7878787878")]


Find demands which belong to the tax period - April 1st, 2022 to March 31st, 2023

$.Demands[?(@.taxPeriodFrom >=1648771200000  && @.taxPeriodTo <= 1680307199000)]


Find demands which belong to the tax period - April 1st 2021 to March 31st, 2022

$.Demands[?(@.taxPeriodFrom >=1617235200000 && @.taxPeriodTo <= 1648771199000)]
