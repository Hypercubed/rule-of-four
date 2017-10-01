# Rule of Four

Determine the most resonable display format for a given numeric value. Using a modified version of the [rule of four](http://www.bmj.com/content/350/bmj.h1845)

## Rule of Four

              Input Value |       toLocaleString |    toPrecision (N=3) |         Rule of Four | Rule of Four (Modified)
              ----------- |       -------------- |    ----------------- |         ------------ | -----------------------
                     0.04 |                 0.04 |               0.0400 |                0.040 |                0.040
                    0.399 |                0.399 |                0.399 |                0.399 |                0.399
                      0.4 |                  0.4 |                0.400 |                 0.40 |                 0.40
                     3.99 |                 3.99 |                 3.99 |                 3.99 |                 3.99
                    4.001 |                4.001 |                 4.00 |                  4.0 |                 4.00
                     39.9 |                 39.9 |                 39.9 |                 39.9 |                39.90
                   40.001 |               40.001 |                 40.0 |                   40 |                40.00

## Integers

              Input Value |       toLocaleString |    toPrecision (N=3) |         Rule of Four | Rule of Four (Modified)
              ----------- |       -------------- |    ----------------- |         ------------ | -----------------------
                        1 |                    1 |                 1.00 |                 1.00 |                    1
                        5 |                    5 |                 5.00 |                  5.0 |                    5
                       10 |                   10 |                 10.0 |                 10.0 |                   10
                       50 |                   50 |                 50.0 |                   50 |                   50
                      100 |                  100 |                  100 |                  100 |                  100
                      500 |                  500 |                  500 |               5.0e+2 |                  500
                     1000 |                1,000 |              1.00e+3 |              1.00e+3 |                1,000
                     5000 |                5,000 |              5.00e+3 |               5.0e+3 |                5,000
                    10000 |               10,000 |              1.00e+4 |              1.00e+4 |               10,000
                    50000 |               50,000 |              5.00e+4 |               5.0e+4 |               50,000
                   100000 |              100,000 |              1.00e+5 |              1.00e+5 |              100,000
                   500000 |              500,000 |              5.00e+5 |               5.0e+5 |              500,000
                  1000000 |            1,000,000 |              1.00e+6 |              1.00e+6 |             1.000e+6
                  5000000 |            5,000,000 |              5.00e+6 |               5.0e+6 |              5.00e+6
                 10000000 |           10,000,000 |              1.00e+7 |              1.00e+7 |             1.000e+7
                 50000000 |           50,000,000 |              5.00e+7 |               5.0e+7 |              5.00e+7
                100000000 |          100,000,000 |              1.00e+8 |              1.00e+8 |             1.000e+8
                500000000 |          500,000,000 |              5.00e+8 |               5.0e+8 |              5.00e+8
                      0.1 |                  0.1 |                0.100 |                0.100 |                0.100
                      0.5 |                  0.5 |                0.500 |                 0.50 |                 0.50
                     0.01 |                 0.01 |               0.0100 |               0.0100 |               0.0100
                     0.05 |                 0.05 |               0.0500 |                0.050 |                0.050
                    0.001 |                0.001 |              0.00100 |              0.00100 |              0.00100
                    0.005 |                0.005 |              0.00500 |               0.0050 |               0.0050
                   0.0001 |                    0 |             0.000100 |             0.000100 |             0.000100
                   0.0005 |                0.001 |             0.000500 |              0.00050 |              0.00050
                  0.00001 |                    0 |            0.0000100 |            0.0000100 |             1.000e-5
                  0.00005 |                    0 |            0.0000500 |             0.000050 |              5.00e-5
                 0.000001 |                    0 |           0.00000100 |           0.00000100 |             1.000e-6
    0.0000049999999999996 |                    0 |           0.00000500 |            0.0000050 |              5.00e-6
                     1e-7 |                    0 |              1.00e-7 |              1.00e-7 |              1.00e-7
                     5e-7 |                    0 |              5.00e-7 |               5.0e-7 |               5.0e-7
                     1e-8 |                    0 |              1.00e-8 |              1.00e-8 |              1.00e-8
                     5e-8 |                    0 |              5.00e-8 |               5.0e-8 |               5.0e-8
                       -1 |                   -1 |                -1.00 |                -1.00 |                   -1
                       -5 |                   -5 |                -5.00 |                 -5.0 |                   -5
                      -10 |                  -10 |                -10.0 |                -10.0 |                  -10
                      -50 |                  -50 |                -50.0 |                  -50 |                  -50
                     -100 |                 -100 |                 -100 |                 -100 |                 -100
                     -500 |                 -500 |                 -500 |              -5.0e+2 |                 -500
                    -1000 |               -1,000 |             -1.00e+3 |             -1.00e+3 |               -1,000
                    -5000 |               -5,000 |             -5.00e+3 |              -5.0e+3 |               -5,000
                   -10000 |              -10,000 |             -1.00e+4 |             -1.00e+4 |              -10,000
                   -50000 |              -50,000 |             -5.00e+4 |              -5.0e+4 |              -50,000
                  -100000 |             -100,000 |             -1.00e+5 |             -1.00e+5 |             -100,000
                  -500000 |             -500,000 |             -5.00e+5 |              -5.0e+5 |             -500,000
                 -1000000 |           -1,000,000 |             -1.00e+6 |             -1.00e+6 |            -1.000e+6
                 -5000000 |           -5,000,000 |             -5.00e+6 |              -5.0e+6 |             -5.00e+6
                -10000000 |          -10,000,000 |             -1.00e+7 |             -1.00e+7 |            -1.000e+7
                -50000000 |          -50,000,000 |             -5.00e+7 |              -5.0e+7 |             -5.00e+7
               -100000000 |         -100,000,000 |             -1.00e+8 |             -1.00e+8 |            -1.000e+8
               -500000000 |         -500,000,000 |             -5.00e+8 |              -5.0e+8 |             -5.00e+8
                     -0.1 |                 -0.1 |               -0.100 |               -0.100 |               -0.100
                     -0.5 |                 -0.5 |               -0.500 |                -0.50 |                -0.50
                    -0.01 |                -0.01 |              -0.0100 |              -0.0100 |              -0.0100
                    -0.05 |                -0.05 |              -0.0500 |               -0.050 |               -0.050
                   -0.001 |               -0.001 |             -0.00100 |             -0.00100 |             -0.00100
                   -0.005 |               -0.005 |             -0.00500 |              -0.0050 |              -0.0050
                  -0.0001 |                   -0 |            -0.000100 |            -0.000100 |            -0.000100
                  -0.0005 |               -0.001 |            -0.000500 |             -0.00050 |             -0.00050
                 -0.00001 |                   -0 |           -0.0000100 |           -0.0000100 |            -1.000e-5
                 -0.00005 |                   -0 |           -0.0000500 |            -0.000050 |             -5.00e-5
                -0.000001 |                   -0 |          -0.00000100 |          -0.00000100 |            -1.000e-6
    -0.000004999999999996 |                   -0 |          -0.00000500 |           -0.0000050 |             -5.00e-6
                    -1e-7 |                   -0 |             -1.00e-7 |             -1.00e-7 |             -1.00e-7
                    -5e-7 |                   -0 |             -5.00e-7 |              -5.0e-7 |              -5.0e-7
                    -1e-8 |                   -0 |             -1.00e-8 |             -1.00e-8 |             -1.00e-8
                    -5e-8 |                   -0 |             -5.00e-8 |              -5.0e-8 |              -5.0e-8

## Floats

              Input Value |       toLocaleString |    toPrecision (N=3) |         Rule of Four | Rule of Four (Modified)
              ----------- |       -------------- |    ----------------- |         ------------ | -----------------------
       0.3555619673806121 |                0.356 |                0.356 |                0.356 |                0.356
       1.3717524180944207 |                1.372 |                 1.37 |                 1.37 |                 1.37
        1.980822246874343 |                1.981 |                 1.98 |                 1.98 |                 1.98
       29.069354129999404 |               29.069 |                 29.1 |                 29.1 |                29.07
         71.9907196667401 |               71.991 |                 72.0 |                   72 |                71.99
        433.2695432704551 |               433.27 |                  433 |               4.3e+2 |               433.27
         978.994900053719 |              978.995 |                  979 |               9.8e+2 |               978.99
        2176.362098073503 |            2,176.362 |              2.18e+3 |              2.18e+3 |              2176.36
        7282.082791707194 |            7,282.083 |              7.28e+3 |               7.3e+3 |              7282.08
        42301.59764788343 |           42,301.598 |              4.23e+4 |               4.2e+4 |              4.23e+4
        90047.41803269243 |           90,047.418 |              9.00e+4 |               9.0e+4 |              9.00e+4
       365716.90066735505 |          365,716.901 |              3.66e+5 |              3.66e+5 |             3.657e+5
        86053.99673913982 |           86,053.997 |              8.61e+4 |               8.6e+4 |              8.61e+4
       2017669.5815287707 |        2,017,669.582 |              2.02e+6 |              2.02e+6 |             2.018e+6
        6563847.949471422 |        6,563,847.949 |              6.56e+6 |               6.6e+6 |              6.56e+6
        19430328.24319243 |       19,430,328.243 |              1.94e+7 |              1.94e+7 |             1.943e+7
        8720677.194098925 |        8,720,677.194 |              8.72e+6 |               8.7e+6 |              8.72e+6
       394392672.18067074 |      394,392,672.181 |              3.94e+8 |              3.94e+8 |             3.944e+8
      0.05726113445905741 |                0.057 |               0.0573 |                0.057 |                0.057
       0.1284627560265572 |                0.128 |                0.128 |                0.128 |                0.128
     0.003206122348199383 |                0.003 |              0.00321 |              0.00321 |              0.00321
     0.018673648365037345 |                0.019 |               0.0187 |               0.0187 |               0.0187
    0.0008555728117371242 |                0.001 |             0.000856 |              0.00086 |              0.00086
     0.001253062929018498 |                0.001 |              0.00125 |              0.00125 |              0.00125
    0.000002881483730940615 |                  0 |           0.00000288 |           0.00000288 |             2.881e-6
    0.00038177269745472223 |                   0 |             0.000382 |             0.000382 |             0.000382
    0.0000023084789418786156 |                 0 |           0.00000231 |           0.00000231 |             2.308e-6
    0.000012769769016543654 |                  0 |            0.0000128 |            0.0000128 |             1.277e-5
    2.3708704797279044e-7 |                    0 |              2.37e-7 |              2.37e-7 |              2.37e-7
    0.0000023339536948967813 |                 0 |           0.00000233 |           0.00000233 |             2.334e-6
      9.00210520488889e-8 |                    0 |              9.00e-8 |               9.0e-8 |               9.0e-8
     4.938024551678913e-7 |                    0 |              4.94e-7 |               4.9e-7 |               4.9e-7
     7.877399072712716e-9 |                    0 |              7.88e-9 |               7.9e-9 |               7.9e-9
     8.721545980193646e-9 |                    0 |              8.72e-9 |               8.7e-9 |               8.7e-9
     -0.17249712836980358 |               -0.172 |               -0.172 |               -0.172 |               -0.172
       -3.965027210120403 |               -3.965 |                -3.97 |                -3.97 |                -3.97
      -1.7856425632831119 |               -1.786 |                -1.79 |                -1.79 |                -1.79
      -14.220910264007358 |              -14.221 |                -14.2 |                -14.2 |               -14.22
       -99.26871668223593 |              -99.269 |                -99.3 |                  -99 |               -99.27
      -126.47732859385852 |             -126.477 |                 -126 |                 -126 |              -126.48
       -341.6284863722541 |             -341.628 |                 -342 |                 -342 |              -341.63
       -3843.375265140827 |           -3,843.375 |             -3.84e+3 |             -3.84e+3 |             -3843.38
        -8316.60942991446 |           -8,316.609 |             -8.32e+3 |              -8.3e+3 |             -8316.61
      -24000.862212101005 |          -24,000.862 |             -2.40e+4 |             -2.40e+4 |            -24000.86
       -82582.09021717402 |           -82,582.09 |             -8.26e+4 |              -8.3e+4 |             -8.26e+4
      -227524.16692196223 |         -227,524.167 |             -2.28e+5 |             -2.28e+5 |            -2.275e+5
       -844081.1300882965 |          -844,081.13 |             -8.44e+5 |              -8.4e+5 |             -8.44e+5
      -2146837.6677082432 |       -2,146,837.668 |             -2.15e+6 |             -2.15e+6 |            -2.147e+6
       -4534660.432160076 |       -4,534,660.432 |             -4.53e+6 |              -4.5e+6 |             -4.53e+6
       -28972170.29702853 |      -28,972,170.297 |             -2.90e+7 |             -2.90e+7 |            -2.897e+7
       -62524408.21238709 |      -62,524,408.212 |             -6.25e+7 |              -6.3e+7 |             -6.25e+7
      -487991917.58792233 |     -487,991,917.588 |             -4.88e+8 |              -4.9e+8 |             -4.88e+8
     -0.08149111962351917 |               -0.081 |              -0.0815 |               -0.081 |               -0.081
     -0.30701128101347375 |               -0.307 |               -0.307 |               -0.307 |               -0.307
    -0.003886339849751641 |               -0.004 |             -0.00389 |             -0.00389 |             -0.00389
    -0.00008040645219987707 |                 -0 |           -0.0000804 |            -0.000080 |             -8.04e-5
    -0.0007365984743528198 |              -0.001 |            -0.000737 |             -0.00074 |             -0.00074
    -0.003078488022631061 |               -0.003 |             -0.00308 |             -0.00308 |             -0.00308
    -0.00004641333312361853 |                 -0 |           -0.0000464 |            -0.000046 |             -4.64e-5
    -0.00012784337315931762 |                 -0 |            -0.000128 |            -0.000128 |            -0.000128
    -0.000006773867753185171 |                -0 |          -0.00000677 |           -0.0000068 |             -6.77e-6
    -0.000012568097011701763 |                -0 |           -0.0000126 |           -0.0000126 |            -1.257e-5
    -9.299193775439201e-7 |                   -0 |             -9.30e-7 |              -9.3e-7 |              -9.3e-7
    -0.000004089857771105385 |                -0 |          -0.00000409 |           -0.0000041 |             -4.09e-6
    -8.492339727697829e-8 |                   -0 |             -8.49e-8 |              -8.5e-8 |              -8.5e-8
    -2.004840602240968e-7 |                   -0 |             -2.00e-7 |             -2.00e-7 |             -2.00e-7
    -1.0949572222007477e-9 |                  -0 |             -1.09e-9 |             -1.09e-9 |             -1.09e-9
     -7.12849825575268e-9 |                   -0 |             -7.13e-9 |              -7.1e-9 |              -7.1e-9

## Special

              Input Value |       toLocaleString |    toPrecision (N=3) |         Rule of Four | Rule of Four (Modified)
              ----------- |       -------------- |    ----------------- |         ------------ | -----------------------
                        0 |                    0 |                 0.00 |                 0.00 |                    0
                       -0 |                    0 |                 0.00 |                 0.00 |                   -0
                 Infinity |                    ∞ |             Infinity |             Infinity |                    ∞
                -Infinity |                   -∞ |            -Infinity |            -Infinity |                   -∞
                      NaN |                  NaN |                  NaN |                  NaN |                  NaN
                    1 + 2 |                    3 |                 3.00 |                 3.00 |                    3
           (0.1 + 0.2)*10 |                    3 |                 3.00 |                 3.00 |                 3.00
                       PI |                3.142 |                 3.14 |                 3.14 |                 3.14
                        E |                2.718 |                 2.72 |                 2.72 |                 2.72
                    SQRT2 |                1.414 |                 1.41 |                 1.41 |                 1.41
                  EPSILON |                    0 |             2.22e-16 |             2.22e-16 |             2.22e-16
