# PSL Bench

## Setup

```bash
git clone https://github.com/addr-rs/pslbench
cd pslbench/docker
docker build -t pslbench .
```

## Sample result

```bash
~/bench]# docker run --rm -it pslbench
Running PyPy benchmark
18.68user 0.66system 0:19.43elapsed 99%CPU (0avgtext+0avgdata 142100maxresident)k
143392inputs+0outputs (238major+25012minor)pagefaults 0swaps
10000000

Running Rust benchmark
1.82user 0.22system 0:02.04elapsed 99%CPU (0avgtext+0avgdata 2780maxresident)k
2544inputs+0outputs (11major+136minor)pagefaults 0swaps
10000000

Running C benchmark
17.07user 0.79system 0:17.92elapsed 99%CPU (0avgtext+0avgdata 2816maxresident)k
1752inputs+0outputs (8major+267minor)pagefaults 0swaps
9999999
```

## Server CPU info

```bash
~/bench]# lscpu
Architecture:        x86_64
CPU op-mode(s):      32-bit, 64-bit
Byte Order:          Little Endian
CPU(s):              4
On-line CPU(s) list: 0-3
Thread(s) per core:  1
Core(s) per socket:  1
Socket(s):           4
NUMA node(s):        1
Vendor ID:           GenuineIntel
CPU family:          6
Model:               63
Model name:          Intel(R) Xeon(R) CPU E5-2680 v3 @ 2.50GHz
Stepping:            2
CPU MHz:             2499.998
BogoMIPS:            4999.99
Hypervisor vendor:   KVM
Virtualization type: full
L1d cache:           32K
L1i cache:           32K
L2 cache:            4096K
L3 cache:            16384K
NUMA node0 CPU(s):   0-3
Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid xsaveopt arat
```
