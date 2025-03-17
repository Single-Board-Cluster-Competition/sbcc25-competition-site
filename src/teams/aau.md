# Aalborg University / Aalborg Supercomputer Klub


## Hardware
All SBC’s will communicate over the switch, a raspberry pi will be used as a DHCP server. We
access the SBC’s through the same switch over SSH.

| Name                                      | Description                  | Price   | Amount | Total     |
|-------------------------------------------|------------------------------|---------|--------|-----------|
| NVIDIA Jetson Orin Nano Super Developer Kit | Single-board computer        | $249.00 | 8      | $1,992.00 |
| Raspberry Pi 4B 4GB                       | DHCP server and NAT          | $60.00  | 1      | $60.00    |
| PNY CS1030 250 GB M.2                     | Solid-state drive            | $20.00  | 8      | $160.00   |
| Meanwell UHP-350-12                       | Power supply for SBCs        | $65.00  | 1      | $65.00    |
| UniFi Standard 24 PoE                     | Networking switch            | $370.00 | 1      | $370.00   |
| **Total**                                 |                              |         |        | **$2647.00** |

## Software
MPI: mpich
LINALG: cuBLAS (GPU primary), blis (CPU backup).
COMPILERS: nvcc / mpicc / clang
MGMT SOFTWARE: Ansible, OpenSSH
Operating System: NVIDIA JetPack 6.x (Ubuntu 22.04 LTS-based)

## Strategy
We seek to take advantage of the powerful GPUs on the Jetson boards.
Use cuBLAS over CPU-BLAS libraries wherever possible. Work on rewriting challenges to be
cuBLAS compatible memory allocations and calls (hopefully). Ensure these implementations are
correct + document.

**HPL**: Use NVIDIA cuBLAS implementation of HPL 2.3.
**STREAM**: Run according to the official run rules using MPI.
**D-LLAMA 3 8B**: Distributed Llama can run on any amount of nodes that is a power of 2, which makes our 8
nodes quite suitable.
**Hashcat**: Hashcat has built-in support for GPU acceleration using CUDA. We plan to split the passwords
equally across the 8 nodes, and crack them whenever the nodes are not busy with anything
else.

## Team Details

**Brian Ellingsgaard**: 2nd-semester Software student. First year participating in SBCC.

**Sofie Finnes Øvreild**: 4th semester Software student. Second year participating in SBCC.

**Thomas Møller Jensen**: 10th semester Software student with a bachelor in Computer Engineering. Second year
of participating in SBCC.

**Tobias Sønder Nielsen**: 4th-semester Software student. Second year participating in SBCC.