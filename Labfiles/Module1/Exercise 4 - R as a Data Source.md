Install R first – remote to VM for screen shots (on K1??)

![](media/6b13e9e5b30b9048afadb7c900ef8073.png)

**Use R in Query Editor**

[R](https://mran.microsoft.com/documents/what-is-r) is a powerful programming
language that many statisticians, data scientists, and data analysts use. You
can use **R** in Power BI Desktop's **Query Editor** to:

-   Prepare data models

-   Create reports

-   Do data cleansing, advanced data shaping, and dataset analytics, which
    include missing data completion, predictions, clustering, and more.

**Install R**

You can download **R** for free from the [Revolution Open download
page](https://mran.revolutionanalytics.com/download/) and the [CRAN
Repository](https://cran.r-project.org/bin/windows/base/).

**Install mice**

You need to have
the [mice library](https://www.rdocumentation.org/packages/mice/versions/3.5.0/topics/mice) installed
in your R environment. Without **mice**, the sample script code won't work
properly. The **mice** package implements a method to deal with missing data.

To install **mice**:

1.  Launch the R.exe program (for example, C:\\Program Files\\Microsoft\\R
    Open\\R-3.5.3\\bin\\R.exe)

2.  Run the install command:

Copy

\> install.packages('mice')

**Use R in Query Editor**

To demonstrate using **R** in **Query Editor**, we'll use an example stock
market dataset contained in a .csv file and work through the following steps:

1.  from the **Home** ribbon, select **Get Data \> Text/CSV**.

![](media/bb79f1b9b3b6e2b4b4853b0ffaa8e6fb.png)

![](media/68129a0110dd1f023a0c873a25470222.png)

From the transform ribbon

Or create a blank query and type this???

dataset \<- read.csv(file="\<Your File Path\>/EuStockMarkets_NA.csv",
header=TRUE, sep=",")

\# 'dataset' holds the input data for this script

library(mice)

tempData \<- mice(dataset,m=1,maxit=50,meth='pmm',seed=100)

completedData \<- complete(tempData,1)

output \<- dataset

output\$completedValues \<- completedData\$"SMI missing values"

![](media/20a1c00e43a8d248f1d5f3e473dd35b1.png)

![](media/b4bb1090b00224fe006fb15ccd606aec.png)

![](media/e00cd9e6fd20b9d240a88606954fb083.png)

![](media/3ffbf54b05ecef05e6db75c28112fd11.png)

![](media/d286330af3daae80cf5720b7a8998d69.png)

![](media/ad3a5d33ea4547154126dd5bc1f9d0bb.png)

IF you didn’t install the package mice, you’ll get this: (it does take a few
minutes)

![](media/5ec9659b3df4de8e0e05ad753e1a36a4.png)

![](media/466d0734a6835a48d95516ce76944c7d.png)
