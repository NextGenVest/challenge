# Code challenge

Hi! Very excited to see what you can do. Please complete this coding challenge and submit within 7 days.    
Pick either the front-end or back-end challenge (depending on what you're interested in applying for). You can also do both if you want to be considered for both positions.   

For **questions**, create a github issue and we will answer within 24 hours or email us at willfalcon@nextgenvest.com if you'd rather remain anonymous.   
Good luck!!   

### Languages
If you know many languages, that's great!! However, we need you to be python and javascript ninja at a minimum.       
- If you do the Front-end challenge, use javascript.    
- If you do the Back-end challenge, use python.   


### Submit instructions     
1. Create a github repository to use while you implement your challenge.    
2. We'll look at the commit history and workflow as part of the evaluation process.   
3. When you are done, email back with the link to your repo (willfalcon@nextgenvest.com).    
4. Make sure you have a README.md with build instructions for your code.    
5. Have fun!    

## Challenge for Front-End    
Imagine your hardwork has paid off and you've been awarded a financial aid package. However, you have the option of choosing 1 loan from the 5 different loans offered :/ ...   
Your loan options are:    
1. Direct Subsidized Loan ([interest here](https://studentaid.ed.gov/sa/types/loans/interest-rates))   
2. Direct Unsubsidized Loan ([interest here](https://studentaid.ed.gov/sa/types/loans/interest-rates))   
3. A private bank loan at 4.2% interest    
4. A loan from the university at 4.0% interest.   

Your challenge is to build a widget to help you vizualize and pick a loan.    
- The Widget: 
  - This widget should be a chart or a similar tool to help you vizualize the loan payment over time. The widget should have as inputs a loan amount, interest, loan period (in months).    
  - This widget should also show me the current interest rate for that loan. The rates listed above are enough. Figure out how to get the rates from [here](https://studentaid.ed.gov/sa/types/loans/interest-rates).      

#### Challenge gotchas    
1. Your widget should be an [angular (1)](https://angularjs.org/) component.   
2. The loan rate information from [here](https://studentaid.ed.gov/sa/types/loans/interest-rates) cannot be done on the front-end. Must be done through a nodejs server.  
3. The other rates for private bank and university can be hardcoded from the instructions above.    

#### Completion checklist    
[ ] Your widget is an angular component    
[ ] Styling is done with SASS    
[ ] Widget shows a graph (or similar) of expected payoff amount given a payoff date           
[ ] Widget can take as input a scholarship amount (typed into an input box). Ex: 60000  
[ ] Widget can take as input an interest rate (typed into an input box). Ex: 0.05    
[ ] Widget can take as input loan period (in months) (typed into an input box). Ex: 36    
[ ] There exists somewhere on the page the current student loan interest rate. Ex: 0.03   
[ ] The rate is fetched by the nodejs server   
[ ] Your project has a README.md with build instructions   

#### Judging criteria    
1. Met all requirements in checklist   
2. Widget 1 animations are creative    
3. Good coding style   
4. Efficient code    
5. Good and clear commit history   
6. Clear README.md build instructions   


## Challenge for Back-End
Lucky you! Your hacking skills have been recognized and you've been awarded a bunch of scholarships (woot!). The catch is that you can only pick 11 scholarships...    

In this challenge, pick the 11 scholarships that give you the most money! You can only pick sequential scholarships and the product of all scholarships you pick is how much money you'll be awarded! (this school is very cheap, so you only need a few dollars... scholarships are in the range 0-100).  

Scholarships can appear on the same row   
...    
... 1 2 **3 4 5** 6 ...    
...    
    
Or same column   
...    
1    
**2**    
**3**    
**4**    
5    
...    

Or on a diagonal    
...    
... **1** 2 3 ...     
... 1 **3** 5 ...    
... 1 2 **5** ...    
...    

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

Answer: 5 * 9 * 25 = 1125   (this is not wrong, figure out where this pattern is...)    

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
