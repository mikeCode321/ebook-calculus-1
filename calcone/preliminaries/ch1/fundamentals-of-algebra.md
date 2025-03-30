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

# Fundamentals of Algebra

## Exponents 
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

##### Practice Problems

Simplify: $3x(2x)^{3}(x^{-1})$

<details>
  <summary>Answer</summary>
  $3x^{1}(2)^{3}(x)^{3}(\frac{1}{x^{1}})$ = $8(3x)(x^{3})(\frac{1}{x^{1}})$ = $8(3x)x^{3-1}$ = $24x(x^{2})$ = $24x^{3}$ 
</details>

Simplify: $(\frac{2^{-3}}{L})^{-2}$

<details>
  <summary>Answer</summary>
  $\frac{2^{-3*-2}}{L^{-2}}$ = $\frac{2^{6}}{\frac{1}{L^{2}}}$ = $2^{6}L^{2}$ = $64L^{2}$
</details>

## Factoring

## Fractions



















Whether you write your book's content in Jupyter Notebooks (`.ipynb`) or
in regular markdown files (`.md`), you'll write in the same flavor of markdown
called **MyST Markdown**.
This is a simple file to help you get started and show off some syntax.

## What is MyST?

MyST stands for "Markedly Structured Text". It
is a slight variation on a flavor of markdown called "CommonMark" markdown,
with small syntax extensions to allow you to write **roles** and **directives**
in the Sphinx ecosystem.

For more about MyST, see [the MyST Markdown Overview](https://jupyterbook.org/content/myst.html).

## Sample Roles and Directives

Roles and directives are two of the most powerful tools in Jupyter Book. They
are like functions, but written in a markup language. They both
serve a similar purpose, but **roles are written in one line**, whereas
**directives span many lines**. They both accept different kinds of inputs,
and what they do with those inputs depends on the specific role or directive
that is being called.

Here is a "note" directive:

```{note}
Here is a note
```

It will be rendered in a special box when you build your book.

Here is an inline directive to refer to a document: {doc}`markdown-notebooks`.


## Citations

You can also cite references that are stored in a `bibtex` file. For example,
the following syntax: `` {cite}`holdgraf_evidence_2014` `` will render like
this: {cite}`holdgraf_evidence_2014`.

Moreover, you can insert a bibliography into your page with this syntax:
The `{bibliography}` directive must be used for all the `{cite}` roles to
render properly.
For example, if the references for your book are stored in `references.bib`,
then the bibliography is inserted with:

```{bibliography}
```

## Learn more

This is just a simple starter to get you started.
You can learn a lot more at [jupyterbook.org](https://jupyterbook.org).
