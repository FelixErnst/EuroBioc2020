FROM bioconductor/bioconductor_docker:devel

COPY *.Rmd /home/RStudio/Microbiome/
COPY *.svg /home/RStudio/Microbiome/
COPY *.rda /home/RStudio/Microbiome/

RUN Rscript -e "install.packages('remotes')" \
    && Rscript -e "remotes::install_github('FelixErnst/mia', repos = BiocManager::repositories(), dependencies = TRUE, upgrade = TRUE)" \
    && Rscript -e "remotes::install_github('microbiome/miaViz', repos = BiocManager::repositories(), dependencies = TRUE, upgrade = TRUE)" \
    && Rscript -e "remotes::install_github('FelixErnst/MicrobiomeExperiment', repos = BiocManager::repositories(), dependencies = TRUE, upgrade = TRUE)"
    && Rscript -e "remotes::install_github('seandavi/BiocPkgTools', repos = BiocManager::repositories(), dependencies = TRUE, upgrade = TRUE)"
    && Rscript -e "BiocManager::install(c('phyloseq'))"
