Bootstrap: docker
From: fred2/optitype

%runscript

    exec /usr/bin/python /usr/local/bin/OptiType/OptiTypePipeline.py "$@"

%post

    echo "Mount data folder: singularity run -b /path/to/data:/data/ optitype.img"
    echo "To see help and options: ./optitype.img -h"
    echo "To specify inputs and outputs, and run with data"
    echo "singularity run -b /path/to/data:/data/ -i input1 [input2] (-r|-d) -o /data/ optitype.img"

