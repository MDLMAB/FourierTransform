# **Foundations of the Fourier Transform** 🍌 

The **Fourier Transform** relies on several fundamental concepts in mathematics and physics. This notes breaks down three critical foundations: **sine signals**, **complex numbers**, and the **dot product**.

---

## **1. Sine and Cosine Signals**  

**Sine** and **cosine** signals form the building blocks of the Fourier Transform because they represent **pure periodic oscillations** with constant frequency, amplitude, and phase.

### **Definition of Sine and Cosine Waves**  

1. A **cosine wave** is defined as:

   \[
   \cos(\omega t + \phi)
   \]

2. A **sine wave** is defined as:

   \[
   \sin(\omega t + \phi)
   \]

Where:  
- \( \omega \): Angular frequency, measured in radians per second (\( \omega = 2\pi f \), with \( f \) as the frequency).  
- \( t \): Time.  
- \( \phi \): Phase shift, which determines the displacement of the wave in time.  

---

### **Key Properties of Sinusoidal Signals**  

1. **Periodicity**:  
   Sine and cosine waves are periodic, with period \( T \):

   \[
   T = \frac{2\pi}{\omega}
   \]

2. **Orthogonality**:  
   Sine and cosine functions with **different frequencies** are **orthogonal** over a single period \( T \). This means their inner (dot) product equals zero:

   \[
   \int_0^T \cos(n\omega t) \cos(m\omega t) \, dt = 0 \quad \text{if } n \neq m
   \]

The same property holds for sine waves and for sine-cosine pairs.

---

## **2. Complex Numbers and Euler's Formula**  

**Complex numbers** simplify the representation of sinusoidal signals by combining sine and cosine waves into a single **complex exponential**.

### **Definition of Complex Numbers**  

A complex number \( z \) is written as:

\[
z = a + jb
\]

Where:  
- \( a \): Real part.  
- \( b \): Imaginary part.  
- \( j \): Imaginary unit, where \( j^2 = -1 \).

---

### **Euler's Formula**  

**Euler's formula** connects complex numbers to sinusoidal signals:

\[
e^{j\theta} = \cos(\theta) + j\sin(\theta)
\]

- The **real part** of \( e^{j\theta} \) is \( \cos(\theta) \).  
- The **imaginary part** of \( e^{j\theta} \) is \( \sin(\theta) \).  

This simplifies the manipulation of oscillations mathematically.

---

### **Example: Representing a Cosine Wave with Euler's Formula**  

A cosine wave can be expressed using Euler's formula:

\[
\cos(\omega t) = \text{Re} \left( e^{j\omega t} \right) = \frac{e^{j\omega t} + e^{-j\omega t}}{2}
\]

Similarly, a sine wave is given by:

\[
\sin(\omega t) = \text{Im} \left( e^{j\omega t} \right) = \frac{e^{j\omega t} - e^{-j\omega t}}{2j}
\]

🍌 Euler's formula allows us to express oscillations compactly using complex exponentials.

---

## **3. Dot Product and Orthogonality**  

The **dot product** (inner product) measures the **similarity** between two functions. In the Fourier Transform, complex exponentials act as **basis functions**, and the dot product determines how much each basis contributes to the signal.

### **Definition of the Dot Product**  

The dot product between two functions \( f(t) \) and \( g(t) \) over an interval \( [a, b] \) is defined as:

\[
\langle f, g \rangle = \int_a^b f(t) \cdot \overline{g(t)} \, dt
\]

Where \( \overline{g(t)} \) is the **complex conjugate** of \( g(t) \).

---

### **Orthogonality of Complex Exponentials**  

The complex exponentials \( e^{j\omega t} \) are **orthogonal** over a period \( T \):

\[
\int_0^T e^{j n\omega t} \cdot e^{-j m\omega t} \, dt =
\begin{cases} 
T & \text{if } n = m \\
0 & \text{if } n \neq m 
\end{cases}
\]

**Why is this important?**  
- 🍌 Complex exponentials form an **orthogonal basis**.  
- 🍌 The Fourier Transform projects a signal onto these basis functions to determine the contribution of each frequency.
