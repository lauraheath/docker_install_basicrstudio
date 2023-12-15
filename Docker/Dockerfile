FROM rocker/rstudio

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y dpkg-dev zlib1g-dev libssl-dev libffi-dev zlib1g-dev libbz2-dev liblzma-dev build-essential libglpk40
RUN apt-get install -y curl libcurl4-openssl-dev libxml2-dev libcairo2-dev libxt-dev r-cran-cairo libgsl-dev
RUN apt-get install -y git openssh-client nano less libxt6 python3 python3-pip python3-venv

RUN R -e "install.packages('devtools')"
RUN R -e "install.packages('R.utils')"
RUN R -e "install.packages('tidyverse')"
RUN R -e "install.packages('ggplot2')"
RUN R -e "install.packages('remotes')"
RUN R -e "install.packages('synapser', repos = c('http://ran.synapse.org', 'http://cran.fhcrc.org'))"

USER rstudio

RUN cd /home/rstudio && git clone https://github.com/lauraheath/docker_install_basicrstudio

USER root
