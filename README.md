Project overview

A food company is looking to produce the highest profits for the next marketing campagin due next month, the new campagin aims to sell a gadget to the customer base, to build the model, a pilot campagin was carried out involving 2,240 customers, the customers were selected at random and were contacted by phone, and the customers who bought the product were labeled.

The campagin was a huge net loss with a success rate of 15%, the objective of the analysis is to predict customer behaviour and apply the findings to the rest of the customer base by creating a predictive model to predict campagin success rate, and customer clustering and profiling.

the dataset used contains socio-economic and demographic data of the 2,240 customers who were contacted, and a flag for those who bought the product.

the deliverables of this projects are:

- An exploration of the customer base.
- Clustering and profiling of the customer base.

-----

Customer base exploration:
- The median customer base is 50 years old, indicating mature demographics.
  
   <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/793efd1f-3563-4bd6-96b6-285046bf5d9d" width="60%" />
   
   
- household size is small, the average amount of childern per household is 0.75 with a maxinum of 3.

   <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/1e9e29f4-8e86-414d-87d5-f03b45de4ecd" />

- the highest amount is spend on wine products, with the average being skewed by an overspending group. indicated by a much higher average spending than the median. (the median is the 50% in the figure below)

<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/0ac4ee88-9062-4b5e-a46c-64038983411d" />
<img width="450" height="350" alt="image" src="https://github.com/user-attachments/assets/53377e50-c951-4242-b2ec-b28127c21846" />
  
- the median customer has spent 82 months with the company, with a mininum of 70 months. meaning the customer base are all loyal customers

  <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/9b36d2e8-41fe-4e39-bacd-ebda07855c3e" />

- the vast majority of the customer base holds a post-secondary degree, half of which hold a graduate degree. customers with a basic education are a fraction of the population.

  <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/3d31ef5e-1cd2-4e0a-9685-8adca4048a24" />

- couples (married and not) are the highest share of the population making up 56% of all customers.

  <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/93738d80-89d6-4e4e-a84a-76348f47b477" />

- the wealthier the customer the higher the response rate (Lines indicate median values). customers with a yearly income of less than ~25k USD spend signifigantly less than any other spending group.

  <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/dce9a2af-3e4b-441f-9c9c-42855be23cd4" />
  <img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/34e9451e-e625-4118-8872-c282b2415e61" />


- there's no signifigant link between age and response. and amount spent and recency.

  <img width="650" height="250" alt="image" src="https://github.com/user-attachments/assets/d261be57-6fd7-4aeb-a67e-fa0d8d7b9d68" />

Clustering and profiling:

This is being done to determine the population of people who will respond to the AD campaign best, the data points being considered are household size (childern), age, previously complained (true or false), total spending, web and store visits, recency, marital status and education. outliers were removed, and childern (previoiusly split into kids and teen childern) were combined into total childern.

k_means clustering was used to cluster the data into 4 clusters, determined using the elbow method.

<img width="300" height="250" alt="image" src="https://github.com/user-attachments/assets/3e9c4dd9-79f1-4897-8581-e368b8eed73c" />


the recency and age for all clusters are roughly the same (within ~5 months of each other)


Cluster 1, highest income responders:
- Highest earning (72,300$ annual income)
- second most response rate (20%)
- Lowest amount of childern (0.45 childern)
- ~56% hold a graduate degree, ~15% hold a masters, and ~22% hold a PHD. none have a secondary/basic only degree
- Highest spending (average of 1136$)
- ~40% are married, ~25% are unmarried couples, and ~23% are single, almost 1% divorced

Cluster 2, low income non responders:
- lowest earning (38,000$ annual income)
- lowest response rate (11%, tied with cluster 3)
- 2nd highest amount of childern (1.22 childern)
- ~49% hold a graduate degree, ~16% hold a masters, and ~20% hold a PHD. ~0.5% hold a basic degree (highest percentage)
- ~64% are married, and ~36% are single.
- lowest spending (average of 188$)

Cluster 3, lower middle income/ unmarried or divorced non-responders
- earnings around ~40k annually, 15k$ less than the mean (53k annually)
- lowest response rate (11%, tied with cluster 2)
- highest amount of childern (1.27 childern)
- ~46% hold a graduate degree, ~19% hold a masters, and ~20% hold a PHD. ~0.25% hold a basic degree
- ~70% are unmarried copules, ~29% are divorced.
- low spending (average of 252$)

Cluster 4, high income highest responders (widows)
- 2nd highest earning (65,000$ annual income)
- highest response rate (23%)
- 2nd Lowest amount of childern (0.88 childern)
- ~46% hold a graduate degree, ~14% hold a masters, and ~31% hold a PHD. none have a secondary/basic only degree
- 2nd highest spending (average of 672$)
- 100% are widows

Takeaway: 
Target cluster 1 and 4 as the show the highest campaign success rate. income and the amount of childern is directly collerated with campaign success rate. additionally, widows have signifigantly higher response rates than any other marital status. 
