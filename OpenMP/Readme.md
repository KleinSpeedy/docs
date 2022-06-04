# OpenMP Guide
### Basics
---

Compiler Arguments:
```bash
    gcc openmp.c -fopenmp
```

To include OpenMP:
```c
    #include<omp.h>
```

OpenMP works with structured blocks:
```c
    {
        int a = foo();
    }
```

To enable parallel execution:  
Number of threads is determined by the system!
```c
    #pragma omp parallel
    {
        ...
    }
```

To specify number of threads (x):
```c
    omp_set_num_threads(x);
```
or
```c
    #pragma omp parallel num_threads(x)
    {
        ...
    }
```
---
