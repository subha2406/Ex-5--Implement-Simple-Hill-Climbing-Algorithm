<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name: Subha Shree U          </h3>
<h3>Register Number: 2305002025           </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


<h2>Algorithm:</h2>
<p>
<ol>
 <li> Evaluate the initial state.If it is a goal state then return it and quit. Otherwise, continue with initial state as current state.</li> 
<li>Loop until a solution is found or there are no new operators left to be applied in current state:
<ul><li>Select an operator that has not yet been applied to the current state and apply it to produce a new state</li>
<li>Evaluate the new state:
  <ul>
<li>if it is a goal state, then return it and quit</li>
<li>if it is not a goal state but better than current state then make new state as current state</li>
<li>if it is not better than current state then continue in the loop</li>
    </ul>
</li>
</ul>
</li>
</ol>

</p>
<hr>
<h3> Steps Applied:</h3>
<h3>Step-1</h3>
<p> Generate Random String of the length equal to the given String</p>
<h3>Step-2</h3>
<p>Mutate the randomized string each character at a time</p>
<h3>Step-3</h3>
<p> Evaluate the fitness function or Heuristic Function</p>
<h3>Step-4:</h3>
<p> Lopp Step -2 and Step-3  until we achieve the score to be Zero to achieve Global Minima.</p>

## PROGRAM
```python
import random, string

answer = "Artificial Intelligence"
gen = lambda: [random.choice(string.printable) for _ in range(len(answer))]
score = lambda s: sum(abs(ord(a)-ord(b)) for a,b in zip(s,answer))

best = gen()
while True:
    print("Score:", score(best), "Solution:", "".join(best))
    if score(best) == 0: break
    new = best[:]; new[random.randrange(len(answer))] = random.choice(string.printable)
    if score(new) < score(best): best = new
```

## OUTPUT
<img width="538" height="889" alt="image" src="https://github.com/user-attachments/assets/5203c0e4-302f-4686-b038-b5c65f99ae14" />


<img width="583" height="833" alt="image" src="https://github.com/user-attachments/assets/0cbc629e-77ce-4332-be60-ccffd1e63b7d" />


## RESULT:
Thus the program to Implement Simple Hill Climbing Algorithm has been executed successfully
