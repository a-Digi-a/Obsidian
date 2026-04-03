#semester-1 #electronics 

# Mesh Analysis

**Mesh Analysis** is a systematic way of applying [[Kirchhoff's Voltage Law]] to [[Electronics Terminology#Mesh|meshes]] in a circuit. There are **5 distinct steps** to follow to use the technique:

## Step 1

**Identify** the **meshes** in the circuit and assign a **clockwise path** for each one. These are the **mesh currents**

![[Pasted image 20260403052908.png]]

## Step 2

Apply **Kirchhoff's Voltage Law** around each **mesh**:

- Travel clockwise around the loop
- Sum the voltages and set the expression to zero

![[Pasted image 20260403053057.png]]

In this example, we make the equation:

$$V_{S}-V_{A}-V_{C}=0$$

![[Pasted image 20260403053210.png]]

And in this mesh:

$$-V_{C}-V_{B}-V_{D}=0$$

## Step 3

Swap out the voltage values for their [[Ohm's Law]] (or known) values:

$$V_{S}-I_{1}R_{A}-(I_{1}-I_{2})R_{C}=0$$


$$-(I_{1}-I_{2})R_{C}-I_{2}R_{B}-I_{2}R_{D}=0$$
## Step 4

**Solve** the **simultaneous equation** created from step 3.

## Step 5

Use the **current values** to calculate any **unknown voltages**.