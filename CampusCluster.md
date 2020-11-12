## Logging in

```
ssh username@cc-login.campuscluster.illinois.edu
```

## conda installation

There is an anaconda installation in `/projects/wagner/anaconda3`.

You can activate it by running
```
source /projects/wagner/anaconda3/etc/profile.d/conda.sh
```

For `pyscf`, there is a specific environment
```
conda activate pyscf
```

Here is a simple perl script that submits a pyscf file to the queue (for `qmchamm` members. If you are a `wagner` member, then change all `qmchamm` instances to `wagner`):
```
#!/usr/bin/perl

print "#PBS -S /bin/bash
#PBS -q qmchamm
#PBS -l nodes=1,flags=allprocs
#PBS -l walltime=36:00:00
#PBS -j oe
#PBS -m n
#PBS -W group_list=qmchamm
#PBS -N $ARGV[0]
#PBS -o $ARGV[0].jobout
cd \${PBS_O_WORKDIR}

#If you have trouble with paths, run
source /projects/wagner/anaconda3/etc/profile.d/conda.sh
conda activate pyscf
export OMP_NUM_THREADS=\$numprocs
python3 $ARGV[0] > $ARGV[0].stdout
";
```

Put this in  ~/bin/sub_pyscf directory, run `chmod 700` on the filename, and you can use it as `sub_pyscf pythonfile.py | qsub`. 
You can modify the wall time and so on on the command line; check the man pages. 
