# Team02

## Running baseline version

```
# build
clang++ -O3 -Wall -std=c++17 pathtracer.cc -o pathtracer

# run
./pathtracer --width 512 --height 512 --spp 128 --max-depth 10 --seed 42 --output image.ppm
```

## Running multithreading version 


```
# build
clang++ -O3 -Wall -std=c++17 -fopenmp pathtracer_omp.cc -o pathtracer_omp

# run
OMP_NUM_THREADS=16 ./pathtracer_omp --width 512 --height 512 --spp 128 --max-depth 10 --seed 42 --output image.ppm
```
Set `OMP_NUM_THREADS` to the number of threads you want to use.