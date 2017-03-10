# Code challenge

Hi! Very excited to see what you can do. Please complete this coding challenge and submit within 7 days.    
Pick either the front-end or back-end challenge (depending on what you're interested in applying for). You can also do both if you want to be considered for both positions.   

### Languages
Please choose from one of these languages as these are what we use in-house.    

- Javascript 
- Python

### Submit instructions     
1. Create a github repository to use while you implement your challenge.    
2. We'll look at the commit history and workflow as part of the evaluation process.   
3. When you are done, email back with the link to your repo.    

## Challenge for Front-End    
Imagine your hardwork has paid off and you've been awarded 5 different scholarships! However, you can only pick one :/ ...    
Your challenge is to build a widget to help you vizualize which scholarship you will pick.    
- Widget 1: 
  - This widget should be a chart or a similar tool to help you vizualize the loan payment over time. The widget should have as inputs a scholarship amount, interest, loan period (in months).    
  - This widget should also show me current interest rates for student loans. You can use [this site](https://studentaid.ed.gov/sa/types/loans/interest-rates) or an API of your choice.   

#### Challenge gotchas    
1. Your widgets should be angular components.   
2. The current load rates information cannot be done on the front-end. Must be done through a nodejs server.   

#### Completion checklist    
[ ] Your widgets are angular components    
[ ] Styling is done with SASS    
[ ] Widget 1 shows a graph (or similar) of expected payoff amount given a payoff date           
[ ] Widget 1 can take as input a scholarship amount (typed into an input box). Ex: 60000  
[ ] Widget 1 can take as input an interest rate (typed into an input box). Ex: 0.05    
[ ] Widget 1 can take as input loan period (in months) (typed into an input box). Ex: 36    
[ ] There exists somewhere on the page the current student loan interest rate (Direct Unsubsidized Loans for Undergraduates). Ex: 0.03   
[ ] The rate is fetched by the nodejs server    

#### Judging criteria    
1. Met all requirements in checklist   
2. Widget 1 animations are creative    
3. Good coding style   
4. Efficient code    
5. Good and clear commit history   


## Challenge for Back-End
Lucky you! Your hacking skills have been recognized and you've been awarded a bunch of scholarships (woot!). The catch is that you can only pick 11 scholarships...    

In this challenge, pick the 11 scholarships that give you the most money! You can only pick sequential scholarships and the product of all scholarships you pick is how much money you'll be awarded! (this school is very cheap, so you only need a few dollars... scholarships are in the range 0-100)

The number of scholarships n is such that n >= 100.    

Once you've implemented your scholarship selection algorithm, build a small REST API that takes in the nxn matrix of scholarships given and returns your selections. An example request is outlined below.    

- Example (can only pick 3 scholarships) (n=5)          
```
1 2 3 4 5    
1 1 2 3 5   
3 4 5 5 5    
3 4 5 9 5    
1 1 5 5 25    
```

Answer: 5 * 9 * 25 = 1125          

API Specs:    
POST /max_scholarship     
'Content-Type: application/json'    

Sample json:    
```
{"data": [[1,2,3,4,5], [1,1,2,3,5], [3,4,5,5,5], [3,4,5,9,5], [1,1,5,5,25]]}
```    

Response:    
```
{"sequence": [5,9,25], "total": 1125}
```    
