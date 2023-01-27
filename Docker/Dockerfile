from rocker/rstudio
RUN apt-get update && apt-get upgrade -y
RUN R -e "install.packages(c('remotes', 'reticulate'))"
RUN R -e "reticulate::install_miniconda()"
RUN R -e "remotes::install_github(repo='https://github.com/generalui/synapser/tree/reticulate', ref='reticulate', force=T)"

run mkdir -p /home/lheath/testrun \ 
&& git clone https://github.com/lauraheath/new_synapser_test.git /home/lheath/testrun
