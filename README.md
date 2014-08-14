http://math.stackexchange.com/questions/266250/explanation-of-this-image-warping-bulge-filter-algorithm


r = Sqrt[(x - .5)^2 + (y - .5)^2]
a = ArcTan[x - .5, y - .5]
rn = r^2.5/.5 

/* NB: arctan is not really necessary since Cos[a] = (x - .5)/r 
and Sin[a] = (y - .5)/r
*/

And then remap your pixels according to:

x -> rn*Cos[a] + .5 
y -> rn*Sin[a] + .5  