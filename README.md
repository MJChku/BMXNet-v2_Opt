# Build
To build the project, please refer to original BMXNet-v2

# Optimize
This codebase optimize binary gemm kernel of BMXNet-v2 using AVX instructions.
The optimization are two parts:
1. The xnor popcnt gemm. First remove openmp because this slows down the performance. Second use AVX to optimize xnor+popcnt (this gives ~2x speedup).
2. Convert float to bits. This part cost a lot of time and is easily optimized. This gives 5x speedup.


# Supplied with a Binary_IDF
In addition to optimiza binary kernel, A Binary IDF for lossless compression is supplied under example.
 
