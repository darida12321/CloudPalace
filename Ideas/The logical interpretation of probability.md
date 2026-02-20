The **logical interpretation** is based on [[The classical interpretation of probability]], but the atomic possibilities can have unequal weights. It examines the **confirmation** that an **evidence** has on a **hypothesis** $c(h, e)$.

In a **language**, there are **properties** and **objects** 
A **state descriptions** describes every object with every property, or its negation. 
The **probability measure** is a [[Functions|function]] over all state descriptions.
This measure defines a **confirmation function**: $c(h,e)=m(h\land e)/m(e)$.
We could use any measure, but $m^*$ is proposed, which only distinguishes between structural differences (reordering the object names should not make a difference).

> [!example]-
> 
> We have a property $F$ and objects $a$ and $b$.
> The 4 state descriptions: 
> 1. $Fa\land Fb$
> 2. $\lnot Fa\land Fb$
> 3. $Fa\land \lnot Fb$
> 4. $\lnot Fa\land \lnot Fb$   
> 
> The 3 structure descriptions are:
> - $\{1\}$: Everything is F
> - $\{2, 3\}$: One thing is F
> - $\{4\}$: Nothing is F
> 
> The $m*$ measure gives us equal weight to the 3 structure descriptions:
> 
| State description | Structure Description | Weight | $m^*$
| :----- | :---- | :---- | :----
|  $Fa\land Fb$ | Everything is F | 1/3 | 1/3 |
|  $\lnot Fa\land Fb$ | One thing is F | 1/3 | 1/6 |
| $Fa\land \lnot Fb$ | One thing is F | 1/3 | 1/6 |
| $\lnot Fa\land \lnot Fb$ | Nothing is F | 1/3 | 1/3 |
> 
> We have a hypothesis $h = Fb$, true in 2 state descriptions.
> We examine $a$ and find it has property $F$. This is evidence $e=Fa$.
> We have $m^*(h\land e)=1/3$ and $m^*(e)=1/2$
> Then the confirmation is $c^*(h,e)=m^*(h\land e)/m^*(e)=2/3$

**Problems**: 
- The definition of $m$, and therefore $c$ is arbitrary.
- The meaning of predicates is not defined, a purely syntactic approach has little explaining power.


#todo logic model hyperlinks