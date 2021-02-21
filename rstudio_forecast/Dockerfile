FROM rocker/rstudio:4.0.4

ARG WHEN

RUN mkdir /home/analysis

RUN Rscript -e "install.packages(c('remotes', 'devtools'))"
RUN Rscript -e "remotes::install_github('curso-r/treesnip')"
RUN Rscript -e "devtools::install_github('catboost/catboost', subdir = 'catboost/R-package')"
RUN Rscript -e "install.packages(c('lightgbm', 'catboost', 'xgboost', 'modeltime', 'tidymodels', 'skimr', 'timetk','tidyverse', 'modeltime.ensemble', 'readr'))"


CMD ["/init"]
