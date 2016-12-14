# Optitype 

This is the official build repository for OptiType images for Singularity Hub.

This will produce a Singularity image (suitable for running in a cluster environment) using [https://github.com/FRED-2/OptiType](https://github.com/FRED-2/OptiType). We do this by way of a bootstrap file for the Docker image.


## 1. Install Singularity

Instructions can be found on the [singularity site](https://singularityware.github.io).


## 2. Bootstrap the image


    sudo singularity create --size 4000 optitype.img
    sudo singularity bootstrap optitype.img Singularity


## 3. Run commands

How to access the OptiType runtime executable?


      ./optitype.img -h


Mount a data directory

      
      singularity run -b /path/to/data:/data/ optitype.img


To specify inputs and outputs, and run with data (not tested)


      singularity run -b /path/to/data:/data/ -i input1 [input2] (-r|-d) -o /data/ optitype.img


