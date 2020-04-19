# COVID-19-Hackathon. 

### Pandemic Forecasting. 

***Abstract : Todays world is suffering with one of the deadliest virus known as Corona Virus or n-COVID-19. This virus give major damage by its rate of infection. Hence for preparation we need some statistical information about this rate of infection so that we can plan for our next step. To apply machine learning, we don’t have enough data with available data we can make wrong prediction also. Hence it is very important that we cover all the parameters that is required to predict the rate of infection of such deadliest pandemic.***. 

###Introduction. 

Corona virus has some pattern , Which is seen in all the country. It has few stages such as stage 1, stage 2,  stage 3, stage 4 , stage 5. In which each level indicates. 
	
stage1 infection is because of international  citizens . In which citizens which came from outside of India brings infection and spreads infection to Indian citizens. This stage doesn’t have any mortality rate. 
	
stage2 infection is person to person transmission which has some  range of infection and can give some casualties. 
	
stage3 infection is community to community transmission which cause wide range of infection and after that Level increases on the basis of casualties. 
	
The man part is that the infected person doesn’t have ay knowledge about his infection under 14 age hence after 14 days all cases appears at the same time. Let's discuss about the architecture on which we are working.   
### Architecture
![Screenshot 2020-04-19 at 11 48 34 AM](https://user-images.githubusercontent.com/59559365/79681126-ff382000-8234-11ea-84f8-601b6d2d5d37.png)
### Methodology (Process)
The expected graph of rate of COVID-19 with respect to no of days will be 

![Screenshot 2020-04-19 at 11 58 11 AM](https://user-images.githubusercontent.com/59559365/79681170-a87f1600-8235-11ea-9241-6d92a68786fb.png)

The reason behind this graph is that none of the country has completely won with this corona virus. Hence it is just infection period . The another phase is a prevention period in which the number of cases will go down and the recovery rate starts. This can be possible when the vaccination of the disease will  invent. But the thing is the vaccination requires time and till that we have to avoid the growth of infection and try to maintain the figure which is present at the peak. Where the number of cases is minimum. To make plan for minimisation we need to check the idea. Which can be done with the help of this model. 
### Model
#### 1) Probability
Let’s consider 2 sets P(A) and P(B) to calculate the probability. Where P(A) stands for probability of Infected person and P(B) stands for probability of Not infected person. The Venn-diagram will look like  
![Screenshot 2020-04-19 at 11 58 22 AM](https://user-images.githubusercontent.com/59559365/79681261-7e7a2380-8236-11ea-9f05-33f40a31f30c.png)

Here P(A ⋂ B) are nothing but the unknown probability of infected citizens. This P(A ⋂ B) will become P(A) after 14 days    and    another P(A ⋂ B) will form. The recovered person will go from set A to B and the casualties will go in the Universe U. 

Now set P(A) and set P(B)is known to us but P(A ⋂ B) is unknown to us. We need to find the probability of infection under the condition with P(A) 
The Mathematical equation of probability of infection under the condition with P(A) will be
P(B/A)  = P(A ⋂ B)/P(A)

Here,

P(B/A) = P(A ⋂ B)/P(A)

P(A) = Given

P(A ⋂ B)  = Unknown.

To Calculate P(A ⋂B)

The first question to find P(A ⋂ B) is, How many person can a single person can infect? The answer to this question is that it depend from person to person. Hence we need to make levels for that. Level1 indicates that the person is in home and the chances of infection is with their family members. Level2 indicates that the person has gone outside for some work. Level3 indicates that the person has gone in some crowded place . Hence the calculation for a single person will be

Level1 = X*1 (this value will be approximately equal to 4 )

Level2 = X*1(the value of X will come from regression part)

Level3 = X*1(The value of X will come from regression part)

This calculation is for single person. For multiple person the equation will become

Level1  = X*m

Level2  = X*m

Level3  = X*m  . And so on.

A ⋂ B    =  ∑ ( ∑ Levels) (i)

P(A ⋂ B) =   (A ⋂ B) / maximum chances of infection

Hence ,

P(B/A)   = P(A ⋂ B)/P(A)
### 2) Regression
![Screenshot 2020-04-19 at 11 58 32 AM](https://user-images.githubusercontent.com/59559365/79681364-6e167880-8237-11ea-9aba-a5d14a90bb86.png)







