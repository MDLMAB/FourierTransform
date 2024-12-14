<!-- MathJax Script -->
<script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# **Euler's Formula and Its Importance** 🍌  

Euler's formula is a fundamental relationship in mathematics that connects complex exponentials with trigonometric functions. It provides an elegant way to represent oscillations using complex numbers, which is essential for applications like the **Fourier Transform**.

---

## **Euler's Formula**  

Euler's formula states:

\[
e^{j\theta} = \cos(\theta) + j\sin(\theta)
\]

Where:  
- \( e \): The base of the natural logarithm (\( e \approx 2.718 \)).  
- \( j \): The imaginary unit, where \( j^2 = -1 \).  
- \( \theta \): An angle in radians. ⚠️ 
- \( \cos(\theta) \): The real part of the expression.  
- \( \sin(\theta) \): The imaginary part of the expression.  

This formula shows that a **complex exponential** combines both cosine and sine terms, which are the building blocks of oscillations.

---

## **Geometric Interpretation**  

Euler's formula can be interpreted geometrically in the **complex plane**:  
- The complex number \( e^{j\theta} \) represents a point on the unit circle (radius \( 1 \)).  
- \( \theta \) is the angle between the point and the positive real axis, measured counterclockwise.

### **Key Rotations on the Complex Plane**  

| Angle \( \theta \)       | \( e^{j\theta} \) | Coordinates in Complex Plane |
|--------------------------|------------------|------------------------------|
| \( 0 \)                  | \( 1 \)          | \( (1, 0) \)                 |
| \( \frac{\pi}{2} \)      | \( j \)          | \( (0, 1) \)                 |
| \( \pi \)                | \( -1 \)         | \( (-1, 0) \)                |
| \( \frac{3\pi}{2} \)     | \( -j \)         | \( (0, -1) \)                |
| \( 2\pi \)               | \( 1 \)          | \( (1, 0) \)                 |

Thus, \( e^{j\theta} \) describes a **rotation** by angle \( \theta \) around the origin in the complex plane.

---

## **Decomposing Cosine and Sine**  

Euler's formula can also be used to derive expressions for cosine and sine in terms of exponentials:

1. **Cosine**:
   \[
   \cos(\theta) = \frac{e^{j\theta} + e^{-j\theta}}{2}
   \]

2. **Sine**:
   \[
   \sin(\theta) = \frac{e^{j\theta} - e^{-j\theta}}{2j}
   \]

These formulas are particularly useful in the **Fourier Transform**, where signals are represented as combinations of complex exponentials.

---

## **Example 1: Representing a Cosine Wave**  

Suppose we have the cosine function:

\[
f(t) = \cos(2\pi t)
\]

Using Euler's formula, we can rewrite it as:

\[
\cos(2\pi t) = \frac{e^{j2\pi t} + e^{-j2\pi t}}{2}
\]

This means that a **cosine wave** can be expressed as the sum of two complex exponentials:  
- \( e^{j2\pi t} \): A rotating vector in the counterclockwise direction (positive frequency).  
- \( e^{-j2\pi t} \): A rotating vector in the clockwise direction (negative frequency).  

---

## **Example 2: Rotating a Point on the Unit Circle**  

Let \( \theta = \pi/4 \) (45 degrees). Using Euler's formula:

\[
e^{j\frac{\pi}{4}} = \cos\left(\frac{\pi}{4}\right) + j\sin\left(\frac{\pi}{4}\right)
\]

From trigonometric values:

\[
\cos\left(\frac{\pi}{4}\right) = \sin\left(\frac{\pi}{4}\right) = \frac{\sqrt{2}}{2}
\]

Thus:

\[
e^{j\frac{\pi}{4}} = \frac{\sqrt{2}}{2} + j\frac{\sqrt{2}}{2}
\]

This represents a point on the unit circle at a 45° angle in the complex plane.

---

## **Why Is Euler's Formula Important?**  

1. **Compact Representation**: It unifies cosine and sine into a single exponential function.  
2. **Signal Analysis**: Used in the Fourier Transform to represent signals as sums of complex exponentials.  
3. **Simplified Math**: Operations like differentiation, integration, and multiplication become much easier with exponentials.  
4. **Geometric Insight**: Provides a clear understanding of rotations in the complex plane.

---

## **Summary**  

Euler's formula:

\[
e^{j\theta} = \cos(\theta) + j\sin(\theta)
\]

- Connects trigonometric functions and complex exponentials.  
- Represents rotations in the complex plane.  
- Allows us to decompose and analyze signals efficiently, particularly in **Fourier analysis**.
