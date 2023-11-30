The steps include following steps to do prediction

Step 1 -- we need to load the package module

library(gdm)

Step 2 -- Load the data and if required set a Subset the data of file pml-training.csv

data(pml-training.csv)

adData = data.frame(diagnosis,predictors)

Step 3 -  fit model

fit <- lda(Class~., data=  adData[ inTrain,])

Step 4 -  summarize the fit

summary(fit)

Step 5 -  make predictions

predictions <- predict(fit, adData)

Step 6 -  make predictions

predictions <- predict(fit,  adData)

step 7  summarize accuracy

rmse <- mean((adData)^2)

print(rmse)

Sample error can be in four category

- False positive

- False negative

- True positive

- True negative

The 20 cases build on the base of pml-training.csv will be using different models like caret , predicting with trees, bagging and random forests.

The 20 cases are

|

user_name

 |

raw_timestamp_part_1

 |

raw_timestamp_part_2

 |

cvtd_timestamp

 |

new_window

 |
|

pedro

 |

1323095002

 |

868349

 |

05/12/11 14:23

 |

no

 |
|

jeremy

 |

1322673067

 |

778725

 |

30/11/11 17:11

 |

no

 |
|

jeremy

 |

1322673075

 |

342967

 |

30/11/11 17:11

 |

no

 |
|

adelmo

 |

1322832789

 |

560311

 |

02/12/11 13:33

 |

no

 |
|

eurico

 |

1322489635

 |

814776

 |

28/11/11 14:13

 |

no

 |
|

jeremy

 |

1322673149

 |

510661

 |

30/11/11 17:12

 |

no

 |
|

jeremy

 |

1322673128

 |

766645

 |

30/11/11 17:12

 |

no

 |
|

jeremy

 |

1322673076

 |

54671

 |

30/11/11 17:11

 |

no

 |
|

carlitos

 |

1323084240

 |

916313

 |

05/12/11 11:24

 |

no

 |
|

charles

 |

1322837822

 |

384285

 |

02/12/11 14:57

 |

no

 |
|

carlitos

 |

1323084277

 |

36553

 |

05/12/11 11:24

 |

no

 |
|

jeremy

 |

1322673101

 |

442731

 |

30/11/11 17:11

 |

no

 |
|

eurico

 |

1322489661

 |

298656

 |

28/11/11 14:14

 |

no

 |
|

jeremy

 |

1322673043

 |

178652

 |

30/11/11 17:10

 |

no

 |
|

jeremy

 |

1322673156

 |

550750

 |

30/11/11 17:12

 |

no

 |
|

eurico

 |

1322489713

 |

706637

 |

28/11/11 14:15

 |

no

 |
|

pedro

 |

1323094971

 |

920315

 |

05/12/11 14:22

 |

no

 |
|

carlitos

 |

1323084285

 |

176314

 |

05/12/11 11:24

 |

no

 |
|

pedro

 |

1323094999

 |

828379

 |

05/12/11 14:23

 |

no

 |
|

eurico

 |

1322489658

 |

106658

 |

28/11/11 14:14

 |

no

 |
