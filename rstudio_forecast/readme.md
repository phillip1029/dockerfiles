# Readme:

1. ## Build the image: 
  docker build -t rstudio_forecast:1.0 .
3. ## Run the image: 
  docker run -d -p 8787:8787 -v path_on_host:/home/rstudio -e PASSWORD=docker rstudio_forecast:1.0
