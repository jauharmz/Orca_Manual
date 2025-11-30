# Orca_Manual

## Installation

### Orca Installation
```
chmod a+x orca_6_1_0_linux_x86-64_shared_openmpi416.run
```
excecute:
```
./orca_6_1_0_linux_x86-64_shared_openmpi416.run
```

### OpenMPI Installation
```
sudo apt update
sudo apt install openmpi-bin libopenmpi-dev
```
Verify installation:
```
mpirun --version
```

### Configure ORCA and OpenMPI in `~/.bashrc`
```
export PATH="/root/orca_6_1_0:$PATH"
export OMPI_MCA_plm=isolated
export OMPI_MCA_rmaps_base_oversubscribe=1
export OMPI_MCA_btl_vader_single_copy_mechanism=none
```

### Configure Core and RAM usage
```
% pal nprocs 64 end
% maxcore 3800
```
