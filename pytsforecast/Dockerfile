FROM python:3.7.10

# Install Python Packages & Requirements (Done near end to avoid invalidating cache)
COPY requirements.txt requirements.txt


RUN pip install -r requirements.txt

# Install JupyterLab
RUN pip install jupyterlab && jupyter serverextension enable --py jupyterlab

# Expose Jupyter port & cmd
EXPOSE 8808
RUN mkdir -p /opt/app
CMD jupyter lab --ip=* --port=8808 --no-browser --notebook-dir=/opt/app --allow-root