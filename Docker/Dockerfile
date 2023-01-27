FROM rocker/rstudio:4.2.2

RUN apt-get update -y\
&& apt-get install -y python3-pip python3.10-venv

RUN R -e "install.packages('remotes')" \
RUN R -e "remotes::install_github(repo='https://github.com/generalui/synapser/tree/reticulate', ref='reticulate', force=T)"

run mkdir -p /home/lheath/testrun \ 
&& git clone https://github.com/lauraheath/new_synapser_test.git /home/lheath/testrun
