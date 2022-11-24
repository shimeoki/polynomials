![Logo](./images/golynomials.png)

# Polynomials for Go
### A Go package that handles the most essential polynomial operations

## Usage

Import by:   
```
import "github.com/mihonen/polynomials"

```



## Derivatives

## Root Solving

Golynomials uses Quadratic formula to solve roots for simple qudratic polynomials. For higher order polynomials, [Durand-Kerner method](https://en.wikipedia.org/wiki/Durand–Kerner_method) is used. This method should be able to solve all complex roots for polynomials upto around 100 degrees.

### Getting Complex Roots

```
roots, err := poly.ComplexRoots()

```

### Getting Real Roots Only

```
roots, err := poly.Roots()

```


## Examples 
### Solving All Roots for $ P(x) = 3x^3 + 2x^2 -x + 13 $


```
    a :=  3.0
    b :=  2.0
    c := -1.0
    d :=  13.0

    poly := polynomials.CreatePolynomial(a, b, c, d)

    roots, err := poly.ComplexRoots()
    if err != nil {
        log.Printf(`ComplexRoots() errored: %v`, err)
        return
    }
    // Use roots

```







