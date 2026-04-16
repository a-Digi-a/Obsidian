#semester-1 #semester-2 #maths #statics
# Vectors

## What is a Vector?

A **vector** is a **force** with both a **magnitude** and **direction**
They are usually denoted on the **Cartesian coordinate system**, with the letters $i, j$ and $k$ denoting the $x, y$ and $z$ directions respectively.

## Magnitude of a Vector and it's Components

The **magnitude** of a **vector** represents it's **size**. We can **find** the magnitude by using the **Pythagorean Theorem**. 
![[Pasted image 20260416134544.png]]
in this example, the **magnitude** of this **vector** would be:
$$\sqrt{ 4^2 + 3^2 }=\sqrt{ 25 }=5$$

If we only have the **magnitude**, we can resolve the i and j components:

cos = adjacent/hypotenuse
adjacent = hypotenuse * cos
**i = magnitude * sin(angle)**

sin = opposite/hypotenuse
opposite = hypotenuse * sin
**j = magnitude * sin(angle)**

## Adding and Subtracting Vectors

**Adding vectors** show the **resultant force** that will be applied by the vectors added.

To **add vectors**, simply **add** all of the **i** **components** together, **add** all of the **j** **components** together and **add** all of the **k** **components** together, just like adding variables! 

This is the same for **subtraction**

## Directional Cosines

**Direction Cosines** are the cosines of the angles between a **3d vector** and the **positive x, y and z axes**, denotes as:

$$l = \cos \theta_{x}$$
$$m = \cos \theta_{y}$$
$$n = \cos \theta_{z}$$
![[Pasted image 20260416143936.png|297]]

$$l^2 + m^2 + n^2 = 1$$

Where **v** is the **magnitude**:

$$v_{x} = lv$$
$$v_{y} = mv$$
$$v_{z} = nv$$
$$v^2 = v_{x}^2 + v_{y}^2 + v_{z}^2$$

## Dot Product

### Scalar


$$\vec{P}\cdot\vec{Q}=PQ\cos \theta$$

### Vector

$$\vec{P}\cdot \vec{Q}=P_{x}Q_{x}+P_{y}Q_{y}+P_{z}Q_{z}$$

## Cross Product

The **cross product** is the **vector** **perpendicular** to the vectors in the cross product, and thus the **normal** to the plane containing them.

$$|\vec{P}\times \vec{Q}|=PQ\sin \theta$$
![[Pasted image 20260416155314.png]]

$$\vec{P} \times \vec{Q} = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ P_x & P_y & P_z \\ Q_x & Q_y & Q_z \end{vmatrix}$$
$$= \begin{vmatrix} P_y & P_z \\ Q_y & Q_z \end{vmatrix} \vec{i} + \begin{vmatrix} P_z & P_x \\ Q_z & Q_x \end{vmatrix} \vec{j} + \begin{vmatrix} P_x & P_y \\ Q_x & Q_y \end{vmatrix} \vec{k}$$
$$= (P_y Q_z - P_z Q_y) \vec{i} + (P_z Q_x - P_x Q_z) \vec{j} + (P_x Q_y - P_y Q_x) \vec{k}$$

## Unit Vectors

A **unit vector** is a vector with a **magnitude of one**

You can get a **unit** **vector** by **dividing** a **vectors** **components** by its **magnitude**