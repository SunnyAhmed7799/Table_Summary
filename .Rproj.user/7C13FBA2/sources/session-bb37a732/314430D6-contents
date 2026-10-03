# Load packages

library(tidyverse)
library(gtsummary)
library(gt)

data<- read.csv("Data/Thalassemia_QoL.csv")

data |> 
    select(18:28, Economic_Class) |> 
  tbl_summary(
    by =  Economic_Class,
    type = everything() ~ "continuous" ,
    statistic = list(
      all_continuous() ~ "{mean},{sd}"
    )
  ) |> 
  add_p() |> 
  bold_p(t=0.05)|> 
  as_gt() |> 
  gtsave("Tables/Tables3.docx")
