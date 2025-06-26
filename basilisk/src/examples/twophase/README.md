# To be used with files stored in my basilisk src folder in my naca repository
Ensure you are using the bash file
```
source ~/.bashrc
```
Change to the proper directory
```
cd ~/basilisk/src/examples/twophase
```
Compile code in basilisk with MPI
```
CC99='mpicc -std=c99' qcc -autolink -Wall -O2 -DDISPLAY=-1 -D_MPI=1 cylinder.c -o cylinder -lm -lfb_tiny -disable-dimensions
```
Run simulation with desired parameters with MPI
```
mpirun -np <# of cores> ./cylinder <Re> <Film Thickness> <maxlevel> <duration(t)>
```
