# Riemman

The provided code implements a parallel version of the Riemann sum method to approximate the integral of a function over a given interval.

The program utilizes the MPI (Message Passing Interface) library to enable parallel execution across multiple processes. The main process (process 0) is responsible for receiving input parameters from the command line and dividing the interval into equal segments. It then sends these segments to slave processes to perform the Riemann sum calculations in parallel.

The slave processes (processes other than 0) receive the segments from the main process and perform the Riemann sum calculations for their assigned segment. They use a predefined function f(x) to calculate the value of the function at each point in the segment and accumulate the partial sum in the variable F. They then send the result back to the main process.

The main process receives the partial results from the slave processes and accumulates the total sum in the variable sum. It then sends the next segment to each slave process and continues the process until all segments have been processed.

Once all segments have been processed, the main process prints the final result of the total sum.

## Requirements

To run this program, you need to have:

- A C compiler (such as mpicc)
- MPICH

## Usage



## Output (Example)
```

```

## Credits

This program was created by [mirluvams](https://github.com/mirluvams) ([mirluvams@gmail.com](mailto:mirluvams@gmail.com)) and [Dr. Victor de la Luz](https://github.com/itztli) for the High Performance Computing Course 2023-2, taught by [Dr. Victor de la Luz](https://github.com/itztli) at [*Escuela Nacional de Estudios Superiores*, campus Morelia](https://www.enesmorelia.unam.mx/), [UNAM](https://www.unam.mx/).
