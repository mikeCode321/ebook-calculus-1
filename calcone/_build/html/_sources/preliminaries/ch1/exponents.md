---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# Exponents 

## Fundamentals of Exponents
$$
  2^{3} = 8; base^{exponent}
$$ 

```{code-cell}
answer = 2**3
print(answer)
```

Exponential notation consists of two parts: the **base** and the **exponent**. The exponent shows how many times to multiply the base by itself. In this case, $2^3$ means multiplying 2 by itself three times: 2 × 2 × 2 = 8.

```{note}
When we say '_base to the power of n_,' we are referring to raising the base to an exponent.
```

##### Rules For Exponentation 
::::{grid}
:gutter: 2

:::{grid-item}
:outline:
**Product of Powers Rule**  
$base^m * base^n = base^{m+n}$  
When multiplying powers with the same base, add the exponents.
:::

:::{grid-item}
:outline:
**Quotient of Powers Rule**  
$\frac{base^m}{base^n} = base^{m-n}$  
When dividing powers with the same base, subtract the exponents.
:::

:::{grid-item}
:outline:
**Power of a Power Rule**  
$(base^m)^n = base^{m * n}$  
When raising a power to another power, multiply the exponents.
:::

:::{grid-item}
:outline:
**Power of a Product Rule**  
$(ab)^n = a^n * b^n$  
When raising a product to a power, raise each factor to the power.
:::

:::{grid-item}
:outline:
**Power of a Quotient Rule**  
$(\frac{a}{b})^n = \frac{a^n}{b^n}$  
When raising a quotient to a power, raise both the numerator and denominator to the power.
:::

:::{grid-item}
:outline:
**Exponent of a Fraction Rule**  
$a^{\frac{exp}{root}} = \sqrt[root]{a^{exp}}$ or $(\sqrt[root]{a})^{exp}$  
A fractional exponent represents both a root and a power.
:::
:::: 

##### Definitions For Exponentation 
(1) $base^0 = 1$<br>
Proof: 
Lets say we have a case where $base^{n}$ * $base^{-n}$ => $base^{n}/base^{n}$ = 1, so by using
the quotient of powers property we see the $base^{n - n = 0} = 1$

(2) $base^1 = base$<br>

(3) $base^n$ = $base_{1}$ * $base_{2}$ * .... * $base_{n}$<br> 

(4a) $base^{-1}$ = $1/base^{1}$<br>
(4b) $base^{-n}$ = $1/base^{n}$<br>
A base raised to a negative exponent is equivalent to the reciprocal of the base raised to the positive exponent. 

Proof:<br>
$
\frac{base^n}{base^n} = base^{n-n} = base^0 = 1
$
Since $base^0 = 1$, we have:

$
base^{-n} = \frac{base^0}{base^n} = \frac{1}{base^n}
$

```{code-cell}
base = 5

base_0 = base ** 0
print(f"Rule (1) base^0 = {base_0}")

base_1 = base ** 1
print(f"Rule (2) base^1 = {base_1}")

n = 3
base_n = base ** n
print(f"Rule (3) base^n = {base_n}")

base_neg_1 = base ** -1
print(f"Rule (4a) base^-1 = {base_neg_1}")

base_neg_n = base ** -n
print(f"Rule (4b) base^-{n} = {base_neg_n}")
```

##### Definitions for Radicals
A **radical** in mathematics is a symbol used to find the root of a number. It shows the operation of determining a number that, when raised to a certain power, equals the value under the radical.

**Assuming a positive (x)**

$\sqrt[n]{x} = x^{\frac{1}{n}}$
<br>
Example: 
$\sqrt[3]{25} = 25^{\frac{1}{3}} = 5$

**Assuming a negative (x) and an odd numbered root:**

$n = 2k + 1 \quad \text{for some} \, k \in \mathbb{Z}.$
When we write 𝑘 ∈ 𝑍 , we are saying that 𝑘 is an integer, i.e., it can be any of the numbers in the set 𝑍. Therefore, 𝑘 could be any positive integer, negative integer, or zero.

$\sqrt[n]{x} = x^{\frac{1}{n}}$
<br>
Example: 
$\sqrt[3]{-8} = -8^{\frac{1}{3}} = -2$

**Assuming a negative (x) and an even numbered root:**

$n = 2k \quad \text{for some} \, k \in \mathbb{Z}.$

Example: 
$\sqrt[2]{-8} = -8^{\frac{1}{2}} = ?$ (not a real number)

##### Definitions for Fractional Exponents
The root of a product is the product of the roots:<br>
$(xy)^{\frac{1}{n}} = \sqrt[n]{x} * \sqrt[n]{y} = \sqrt[n]{xy}$

The root of a quotient is the quotient of the roots:<br>
$(\frac{x}{y})^{\frac{1}{n}} = \frac{\sqrt[n]{x}}{\sqrt[n]{y}} = \sqrt[n]{\frac{x}{y}}$

##### Practice Problems

(1) Simplify: $3x(2x)^{3}(x^{-1})$

```{dropdown} Answer
  $3x^{1}(2)^{3}(x)^{3}\left(\frac{1}{x^{1}}\right) = 8(3x)(x^{3})\left(\frac{1}{x^{1}}\right) = 8(3x)x^{3-1} = 24x(x^{2}) = 24x^{3}$
```

(2) Simplify: $(\frac{2^{-3}}{L})^{-2}$

```{dropdown} Answer
  $\frac{2^{-3*-2}}{L^{-2}}$ = $\frac{2^{6}}{\frac{1}{L^{2}}}$ = $2^{6}L^{2}$ = $64L^{2}$
```

(3) Simplify: $\frac{y^{4}(x^{6}y^{2})^{-2}}{(2x^{-3}y^{4})^{2}}$

```{dropdown} Answer
  $\frac{y^{4}(x^{-12}y^{-4})}{(2^{2}x^{-6}y^{8})}$ = $\frac{y^{4+(-4)}x^{-12}}{(4x^{-6}y^{8})}$ = $\frac{x^{-12-(-6)}}{(4y^{8})}$ = $\frac{x^{-6}}{4y^{8}}$ = $x^{-6} * \frac{1}{4y^{8}}$ = $x^{-6} * y^{-8} * \frac{1}{4}$
```

(4) Solve: $27^{\frac{2}{3}}$

```{dropdown} Answer
  $\sqrt[3]{27^{2}} or (\sqrt[3]{27})^{2} = 3^{2} = 9$
```

(5) Solve: $\frac{x^\frac{-2}{3}\sqrt[2]{x}y^{-2}{3}}{x^{\frac{3}{2}}\sqrt[3]{y}}$

```{dropdown} Answer
  $x^{\frac{-2}{3} + \frac{1}{2} - \frac{3}{2}} * y^{\frac{-2}{3} - \frac{1}{3}} = x^{\frac{-10}{6}} * y^{-1}$ 
```

```{code-cell}
from sympy import symbols, simplify, Eq
from sympy.printing import pretty

x, y, L = symbols('x y L')

expr1 = 3 * x * (2 * x)**3 * x**(-1)
expr2 = (2**(-3) / L)**(-2)
expr3 = (y**4 * (x**6 * y**2)**(-2)) / ((2 * x**(-3) * y**4)**2)
expr4 = 27**(2/3)
expr5 = (x**(-2/3) * (x**(1/2)) * y**(-2/3)) / (x**(3/2) * y**(1/3))

simplified_expr1 = simplify(expr1)
simplified_expr2 = simplify(expr2)
simplified_expr3 = simplify(expr3)
simplified_expr4 = simplify(expr4)
simplified_expr5 = simplify(expr5)

print("Expression 1:\n", pretty(simplified_expr1))
print("Expression 2:\n", pretty(simplified_expr2))
print("Expression 3:\n", pretty(simplified_expr3))
print("Expression 4:\n", pretty(simplified_expr4))
print("Expression 5:\n", pretty(simplified_expr5))
```