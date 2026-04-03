#semester-2 #electronics 

# Nodal Analysis

**Nodal analysis** is a way of applying [[Kirchoff's Current Law]] to nodes in a circuit.

There are **6 steps** to follow:

We will be using this circuit for this example:

![[Pasted image 20260403005752.png]]

## Step 1

**Choose a node** as a **reference node**. Typically we choose a node **connected to ground**. All **voltages** will be measured **with respect to this node**.

![[Pasted image 20260403005921.png]]

## Step 2

**Label the voltages on the remaining nodes.** In this case, they will be labelled $V_{1}$, $V_{2}$ and $V_{3}$.

![[Pasted image 20260403010114.png]]

## Step 3

**Label** the **known voltages**. In this case, we know that $V_{1}=V_{s}$.

![[Pasted image 20260403010427.png]]

## Step 4

**Apply** [[Kirchoff's Current Law]] to each node with an unknown voltage. All of the arrows **point towards the node being analysed**.

![[Pasted image 20260403010847.png]]

First lets look at $V_{2}$:

$$I_{A}+I_{B}+I_{C}=0$$

Now lets substitute $I_{A}$, $I_{B}$ and $I_{C}$ for their ohms law variants:
$$I_{A}=\frac{V_{S}-V_{2}}{R_{A}}$$
$$I_{B}=\frac{V_{3}-V_{2}}{R_{B}}$$
$$I_{C}=\frac{0-V_{2}}{R_{C}}$$

Putting this all back into the original equation we get:
$$\frac{V_{S}-V_{2}}{R_{A}}+\frac{V_{3}-V_{2}}{R_{B}}+\frac{0-V_{2}}{R_{C}}=0$$


We then do the same for $V_{3}$:

![[Pasted image 20260403013435.png]]

$$I_{B}=\frac{V_{2}-V_{3}}{R_{B}}$$
$$I_{D}=\frac{0-V_{3}}{R_{D}}$$

$$\frac{V_{2}-V_{3}}{R_{B}}+\frac{0-V_{3}}{R_{D}}=0$$

## Step 5

**Solve** the **simultaneous equation** we just created:

Equation 1:

$$\frac{V_{S}-V_{2}}{R_{A}}+\frac{V_{3}-V_{2}}{R_{B}}+\frac{0-V_{2}}{R_{C}}=0$$

Equation 2:

$$\frac{V_{2}-V_{3}}{R_{B}}+\frac{0-V_{3}}{R_{D}}=0$$

## Step 6

**Use the voltages** solved from **step 5** to **solve for the current of each node**

