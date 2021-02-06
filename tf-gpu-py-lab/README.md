# tensorflow with GPU (nvidia runtime) +jupyterlab dark

**tensorflow:nightly**

Runs jupyterlab in dark mode, with following packages (in `requirements.txt`):
- pandas
- pandas-profiling[notebook]
- matplotlib
- seaborn

Compose file attaches the current directory to `/tf` in the container, gets the image from docker hub

*TODO: add build option in compose file*