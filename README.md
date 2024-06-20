# Mass-Spring-Simulation

## Demo
### Cloth simulation 
![ezgif com-video-to-gif-converter](https://github.com/amin1nasim/Mass-Spring-Simulation/assets/49731000/9b11184b-98db-4d7c-b32f-3a8835dad84a)

### Cloth With Collision
![ezgif com-video-to-gif-converter (1)](https://github.com/amin1nasim/Mass-Spring-Simulation/assets/49731000/bbe5850b-3293-4d33-bb0d-628f694747c6)

### Jelly Cube
![jelly-cube-sim-ezgif com-speed](https://github.com/amin1nasim/Mass-Spring-Simulation/assets/49731000/fa41965d-63fd-4f2f-a0f0-ed44726810e7)

## Mathematical Concepts
### Newton’s second law
From Newton’s second law, we know that $F = ma$. For small time intervals ($\Delta t$), we can approximate velocity and position as follows:

$$ V_{\Delta} = V + a \Delta t $$

$$ P_{\Delta} = P + V \Delta t $$

### Hooke's Law
When a spring is pulled or squished in a frictionless environment, it performs harmonic motion, with the spring force given by:

$$F = Kx,$$

where $x$ is the displacement from its rest length and $k$ is called the spring constant.

Using the semi-implicit Euler method, we ensure stable and realistic spring oscillations:

$$V_{t + 1} = V_t + a_t \Delta t$$

$$P_{t + 1} = P_t + V_{t + 1} \Delta t$$

### Air Damping
In the real world, harmonic oscillation is hindered by friction. Air damping introduces a force opposite to the object's velocity:

$$F = -CV,$$

where $C$ is the air-damping constant.

### Spring Damping
Spring damping prevents relative movements that compress or stretch the spring. It is defined as:
$F = -C \\frac{(v_1 - v_2) \\cdot D}{D \\cdot D} D$
where $C$ is the spring damping constant, $v_1$ and $v_2$ are the velocities at either end of the spring, and $D$ is the connecting vector.

### Gravity
The gravitational force on a particle is:

$$F = m \cdot \text{acceleration of gravity}$$

where $m$ is the particle's mass. The gravitational acceleration is typically set to 9.8 m/s².

### Surface Collision
In the jelly cube model, we use penalty-based collision handling. If a particle crosses the boundary, a hypothetical spring forces it back above the boundary line

## Self-Collision
In the cloth-on-sphere model, a Coulomb-like repulsion prevents self-collision. The amount of repulsion force is proportional to the reciprocal distance squared between the two particles.

$$ F = q/r^2 $$
