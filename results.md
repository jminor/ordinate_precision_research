1/2 inftest.test.Floating point product vs Sum Test...

# Ordinate Precision Exploration


## Float Type Exploration
Reports how many iterations before the sum is not equal to the product by more than half a frame

### Type: f32
 
 | rate | iterations | tolerance | wall clock time |
 |------|------------|-----------|-----------------|
 | 24 | 9418 | 0.020833334 | 6.540m |
 | 24 | 1320 | 0.0005 | 55.001s |
 | 23.976025 | 10059 | 0.020854166 | 6.993m |
 | 23.976025 | 1206 | 0.0005 | 50.301s |
 | 120 | 6410 | 0.004166667 | 53.421s |
 | 120 | 4350 | 0.0005 | 36.251s |
 | 48000 | 8651 | 0.000010416667 | 0.180s |
 | 48000 | 42861 | 0.0005 | 0.893s |
 | 192000 | 8651 | 0.0000026041666 | 0.045s |
 | 192000 | 95880 | 0.0005 | 0.500s |
OK
2/2 inftest.test.Floating point division to integer test...

## Time to Frame Number Test
Measures if the correct integer frame number and phase offset canbe recovered from a large time value.

### Type: f32
 
 | rate | iter | Failure | failure frame | expected | measured |
 |------|------|---------|---------------|----------|----------|
 | 24 | 10e11 | frame is wrong | 2400000100000 |  100000000000 | 100000006144 |
 | 23.976025 | 10e3 | Fract is not 0 | 23976.025 | 0 | measured: 0.000061035156 |
 | 25 | 10e11 | frame is wrong | 2500000000000 |  100000000000 | 99999997952 |
 | 29.97003 | 10e4 | Fract is not 0 | 299700.28 | 0 | measured: 0.99902344 |
 | 120 | 10e9 | frame is wrong | 120000000000 |  1000000000 | 1000000064 |
 | 48000 | 10e8 | frame is wrong | 4800000300000 |  100000000 | 100000008 |
 | 192000 | 10e8 | frame is wrong | 19200001000000 |  100000000 | 100000008 |

### Type: f64
 
 | rate | iter | Failure | failure frame | expected | measured |
 |------|------|---------|---------------|----------|----------|
 | 24 | 10e23 | frame is wrong | 2400000000000000000000000 |  100000000000000000000000 | 100000000000000008388608 |
 | 23.976023976023978 | 10e2 | Fract is not 0 | 2397.602397602398 | 0 | measured: 0.000000000000014210854715202004 |
 | 25 | 10e21 | frame is wrong | 25000000000000000000000 |  1000000000000000000000 | 999999999999999868928 |
 | 29.97002997002997 | 10e16 | frame is wrong | 299700299700299650 |  10000000000000000 | 9999999999999998 |
 | 120 | 10e23 | frame is wrong | 12000000000000000000000000 |  100000000000000000000000 | 99999999999999991611392 |
 | 48000 | 10e23 | frame is wrong | 4800000000000000000000000000 |  100000000000000000000000 | 99999999999999991611392 |
 | 192000 | 10e23 | frame is wrong | 19200000000000000000000000000 |  100000000000000000000000 | 99999999999999991611392 |

OK
All 2 tests passed.