FROM rocker/binder:3.6.0
LABEL maintainer='CB'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/reproduciblescience/6-reproreports-cbaldassano/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-11-14/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
