# IdekCTF

### Golden Ticket

from the code , we know that the last chocolate in the bag is the golden ticket which is the flag       
from the code , we also know that all the chocolates were finished in the bag except the last 2 which were the `golden ticket -1` and `golden ticket`     
last 2 chocolates were placed in choclate generator    
hence `c1 = 13**(g-1) + 37**(g-1)  (mod) p`  and `c2 = 13**g + 37**g  (mod) p` where `x=88952575866827947965983024351948428571644045481852955585307229868427303211803239917835211249629755846575548754617810635567272526061976590304647326424871380247801316189016325247` and  `y =67077340815509559968966395605991498895734870241569147039932716484176494534953008553337442440573747593113271897771706973941604973691227887232994456813209749283078720189994152242`       
assuming `13**(g-1)` as x and `37**(g-1)` as y       
the eqns become   `c1= x+y (mod p)` and `c2 = 13x+37y (mod p)`     
substitute `x = c1-y (mod p)` in `c2 = 13x +37y (mod p)`   
you get `24y = c2 - 13c1  (mod p) `      
multiply mod inverse 24 on both sides   
you get `y = (c2 - 13c1).24**(-1) (mod p)`      
we know c2,c1 and p       
solving for p and converting resultant to bytes we get the flag    
```
flag - idek{charles_and_the_chocolate_factory!!!}
```
