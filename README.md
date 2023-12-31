# Monte Carlo-NPT
This repository serves as an illustrative example of an __NPT__ (constant Number of particles, constant Pressure, and constant Temperature) __Monte Carlo (MC)__ simulation.

## Steps:

1. **Generate Atomic Coordinates:**
   - Generate coordinates for atoms within a cubic simulation box with a periodic boundary condition.
   - Simulation box edge length: 18 (all quantities in reduced Lennard-Jones units).
   - Achieve number density of 0.75.

2. **Lennard-Jones Interaction Potential:**
   - Implement the 6-12 Lennard-Jones interaction potential between atoms.
   - Utilize a potential truncated and shifted at a distance of 2.5.
3. **Determine the pressure of the system:**
   - Using an equation of state (EOS), estimate the pressure of Lennard- Jones fluid at a reduced temperature of 1.0 and reduced density of 0.8.
   - According to the reduced form of the Van der Waals equation, we have:
   $$\(P_r + \frac{3}{{V_r}^2}\) \(V_r - \frac{1}{3}\) = \frac{8}{3}T_r $$
   where:
      - $\( P_r \)$ is the reduced pressure,
      - $\( V_r \)$ is the reduced volume,
      - $\( T_r \)$ is the reduced temperature.
   SO, we will have $\( P_r = 0.9891 \)$.

4. **NPT Monte Carlo (MC) Simulation:**
   - Conduct NPT MC simulation, maintaining constant number of particles, Pressure, and temperature (T = 1.0).
   - The simulation will have particle translationas and volume change for the Monte Carlo moves.
   - The simulation should be run till the properties of the system attain steady values.

5. **Analysis and Comparison:**
   - Examine the radial distribution function (RDF) at the beginning and end of the simulation.
   - Monitor the change of Energy with each move (How many MC moves does it take for the system to equilibrate at these conditions)
   - How the density of the system will be changed?

