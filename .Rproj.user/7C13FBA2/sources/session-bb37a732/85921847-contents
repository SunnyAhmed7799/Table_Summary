# Load packages

library(tidyverse)
library(gtsummary)
library(gt)

data<- read.csv("Data/Thalassemia_QoL.csv")

data |> 
  select(18:28,Gender) |> 
  tbl_summary(
    by = Gender,
    type = everything() ~ "continuous" ,
    statistic = list(
      all_continuous() ~ "{mean},{sd}"
    )
  ) |> 
  as_gt() |> 
  gtsave("Tables/Tables1.docx")
