FROM rocker/rstudio:4.2.2

RUN apt-get update -y\
&& apt-get install -y dpkg-dev zlib1g-dev libssl-dev libffi-dev zlib1g-dev libbz2-dev liblzma-dev build-essential libglpk40\
&& apt-get install -y curl libcurl4-openssl-dev libxml2-dev libcairo2-dev libxt-dev r-cran-cairo libgsl-dev\
&& apt-get install -y git openssh-client nano less libxt6 libcurl4-openssl-dev python3 python3-pip


RUN R -e "install.packages('remotes')" \
&& R -e "install.packages('BiocManager')"\
&& R -e "install.packages('devtools')"\
&& R -e "install.packages('R.utils')"\
&& R -e "install.packages('tidyverse')"\
&& R -e "install.packages('caret')"\
&& R -e "install.packages('data.table')"\
&& R -e "install.packages('ggplot2')"\

run mkdir -p /home/lheath/testrun \ 
&& git clone https://github.com/https://github.com/lauraheath/new_synapser_test.git /home/lheath/testrun