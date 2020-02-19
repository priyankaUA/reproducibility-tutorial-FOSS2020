# reproducibility-tutorial-FOSS2020    1  df -h
    ##Clone the guthub repo
    6  git clone https://github.com/priyankaUA/reproducibility-tutorial-FOSS2020.git
    7  ls
    ##Download conda
    8  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    9  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
   10  ln -s /opt/conda/pkgs/*/bin/* /bin
   11  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   12  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   13  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   14  /opt/conda/bin/pip install bash_kernel
   15  /opt/conda/bin/pip install ipykernel
   16  /opt/conda/bin/python3 -m bash_kernel.install
   17  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   18  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   19  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial-FOSS2020/'
   20  /opt/conda/bin/conda search -c bioconda snakemake
   21  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   22  ln -s /opt/conda/bin/* /bin
   23  ln -s /opt/conda/lib/* /usr/lib
   24  snakemake --version
   25  sudo apt-get update
   26  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   27  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   28  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   29  sudo apt-get update
   30  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   31  docker run hello-world
   32  cd /scratch/reproducibility-tutorial-FOSS2020/
   33  history >>README.md
