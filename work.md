$$
z1 = W \cdot x + b
$$

$$
h= tan(z1) 
\\
\implies h= tan(W \cdot x + b)
$$
which is not a linear function, so when this is placed in y hat you get:
$$
\hat{y}= h \cdot x + b
\\
\hat{y}=tan(W \cdot x + b) \cdot x + b 
$$

Whis is a nonlinear function
However
without the h
$$
z1 = W \cdot x + b
$$
Which is a linear function
$$
\hat{y}= z1 \cdot x + b
\\
\implies \hat{y}=(W \cdot x + b) \cdot x + b 
$$

Which also results in a linear funcion.


So each layer would be a result of a sum of linear equations which would lead to a bigger linear equation.

Using the chain rule
$$
\frac{\partial loss}{\partial w}= \frac{\partial loss}{\partial \hat{y}} \cdot \frac{\partial \hat{y}}{\partial w}
$$

$$
loss= \frac{(\hat{y}-y)^2}{n}
\\

\frac{\partial loss}{\partial \hat{y}} =2((\hat{y}-y))
$$

$$
\hat{y}=wx+b
\\
\frac{\partial \hat{y}}{\partial w}= x
$$

$$
\frac{\partial loss}{\partial w}=2((\hat{y}-y)) \cdot x

$$
for an arbitrary value of n

for all values of n it would be 
$$
\frac{\partial loss}{\partial w}= \frac{1}{n} \cdot \sum^n_{i=0} 2((\hat{y}-y)) \cdot x
$$