# EuroBioc2020 - Upgrading microbiome research in R/Bioc

## Docker image

Build the docker image for trying out the resources

```
docker build -t ebc2020_microbiome .
```

Start it ...

```
docker run -dit -p 8787:8787 --name ebc2020_microbiome ebc2020_microbiome
```

... and login into the RStudio in your browser at `localhost:8787`

## Slides
 
Have a look at `20201218_boaf_TSE_mia.html` for the prebuild slides
