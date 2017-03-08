# Code challenge

Hi! Very excited to see what you can do! Please complete this coding challenge and submit within 7 days.    

### Languages
Please choose from one of these languages as these are what we use in-house.    

- Javascript 
- Python

### Submit instructions     
1. Create a github repository to use while you implement your challenge.    
2. We'll look at the commit history and workflow as part of the evaluation process.   
3. When you are done, email back with the link to your repo.    

## Challenge for Front-End    
Congratulations, you've been accepted to 5 amazing schools! To help you decide where to go, you've decided to build a little game.        
Your game is played like memory. You have 10 cards face down. A blue card for each school and a red card for how much you want to go (1, 2, 3, 4, 5).   

Your game is so cool, I want to play it too but with my schools!    
Build a little UI that takes in a JSON string (text input box is fine) like:    
```
[{"school_name": "Monsters U"}, {"school_name": "Slippery Rock"}, {"school_name": "Hard ball"}, {"school_name": "Prince U"}, {"school_name": "Sand Castle Rock"}]
```    
And builds a game for me to try.     
Once I give you my schools JSON, make sure you can save it and restore the game from it (use a node.js server to handle this part). Saving to a JSON file is fine (please don't use any databases of any kind).    

The rest of this challenge is open-ended on purpose to see what you can do and how creative you can be.    


## Challenge for Back-End
Lucky you! Your hacking skills have been recognized and you've been awarded a bunch of scholarships (woot!). The catch is that you can only pick 11 scholarships...    

In this challenge, pick the 11 scholarships that give you the most money! You can only pick sequential scholarships and the product of all scholarships you pick is how much money you'll be awarded!    

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
