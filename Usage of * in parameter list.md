# Usage of * in parameter list

  First, I define a function which return the sum of two numbers. 

>>> def f(a,b):	return a+b

  Then, I input two parameters, it return a correct result. 

>>> f(1,2)
3

  I try an input of a tuple, it fails.

>>> f((1,2))
Traceback (most recent call last):
  File "<pyshell#12>", line 1, in <module>
    f((1,2))
TypeError: f() takes exactly 2 arguments (1 given)

  But, when I insert '*' before the tuple, it works and return a correct result again. It seems that, '*' can remove '()' of a tuple.

>>> f(*(1,2))
3

  Generally, we most use '*' as follows, arg receives all parameters as a tuple.
  In addition, we also use '**' to receive parameters in format like 'key = para', as a dictionary.
  
>>> def h(*arg):    return arg
>>> h(1,2)
(1, 2)

>>> def g(**kwargs):    return kwargs
>>> g(name = "Jim")
{'name': 'Jim'}
