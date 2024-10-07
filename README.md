# Commission Sales Analysis

### Project Overview

This project is aimed to help Vandes Group's Sales department who wants to use its sales data to build out a commission structure that rewards the various tiers in its Sales hierarchy and also to guide top management to make more informed decisions on the productivity of the Sales team as well as the profitable regions to focus on and also to build a Sales Commission Structure which will serve as a template for rewarding the sales done in future months at Vandes Groups.


![Commission Overview Table](https://github.com/user-attachments/assets/15630b93-8236-497a-bacb-c12772865711)


![Commmision Breakdown](https://github.com/user-attachments/assets/b19c01b4-a2a9-4df0-96ce-4f2cdaf22307)



### Data Sources

The main dataset used for this analysis is the “Vandes Group Sales Data.xlsx” & “Vandes Group-Sales Commission Project Briefing.pdf” files that contains detailed information about the (Sales Agent, Sales Manager, and Affiliate Agent Sales) and (Project Briefing, guide, and expectation) respectively.

### Tools

- Microsoft Excel - Data Cleaning, Sorting, Evaluation, & Analysis
  - [Download Here](https://microsoft.com)
 
### Data Cleaning/Preparation

In the data preparation, we performed the following tasks:
1.	 Data Cleaning and formatting
2.	 Drafted and arranged the parameters required for the various Sales Commissions

### Exploratory Data Analysis (EDA)

The EDA involved a summarized commission payout report that provides the Total payouts per Individual who is eligible to earn the various types of commissions:
-	A summary payout table for the Sales Agents' Designation
-	A summary payout table for the Managers
-	A summary table for the Third-party commission
Note: Each Month’s commission must be reflected

###  Data Analysis 

Include some interesting features/Excel formulars we worked with

```plaintext
=[@Datejoined] + 30
=EOMONTH([@[1st 30 Days Date]],1)
=EOMONTH([@[1st 60 Days  Date]],1)
=COUNTIFS(SalesData[Agentname],[@Agents],SalesData[DateOfSale], "<=" & [@[1st 30 Days Date]])
=COUNTIFS(SalesData[Agentname], [@Agents], SalesData[SaleMonth],9)
=COUNTIFS(SalesData[Agentname], [@Agents], SalesData[SaleMonth], 10)
=XLOOKUP(A2, AgentData[Agents], AgentData[Agent Pay Month1], "")
=SUMIFS(AgentData[SalesMgPay Month1], AgentData[Managers], A2)
=XLOOKUP(B3,Breakdown!$A$13:$A$15, Breakdown!$B$13:$B$15, 0,-1) * B3
```

### Results/Findings

The analysis results are summarized as follows:
- There are 277 active Sales Agent out of 279 Sales Agents and its only 102 active Sales Agents met the criteria for first month sales commissions, 47 active Sales Agent met the criteria for the second month commissions, and 49 active Sales Agent met the criteria for the third month commissions. This decrease in the first and second months when compared with the first month might be as a result of lack of marketing strategy or the commission rate attached to the second and third months when compared with that of first month.
- There are 45 active Sales Managers out of 72 Sales Managers, 31 out of the 45 met the criteria for the first month commissions while 27 active Sales Managers met criteria for second- and third-month criteria respectively. 
- There are 15 affiliate Sales Agent and all met the monthly sales target except one affiliate Sales Agent. 
- Out of the 3 regions (Lagos, Port-Harcourt, & Ilorin), Lagos and Port-Harcourt are regions with most sales while Ilorin is the least. 
 
### Recommendation

Based on the analysis, I recommend the following actions:
- Vandes Group Sales should increase the commissions per sale for the Affiliate Sales Agents, this will encourage the Affiliate Sales Agents to work hard and make more sales.
- I strongly recommend that Vandes Group Sales should focus on expanding its outlet in Ilorin region, as this region not making much sales compared to other regions.


