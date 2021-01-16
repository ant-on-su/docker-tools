FROM python:latest

RUN python -m pip install --upgrade pip && pip install --no-cache-dir jupyter jupyterlab
RUN mkdir mkdir -p /root/.jupyter/lab/user-settings/@jupyterlab/apputils-extension && \
    echo "{" > /root/.jupyter/lab/user-settings/@jupyterlab/apputils-extension/themes.jupyterlab-settings && \
    echo "    \"theme\": \"JupyterLab Dark\"" >> /root/.jupyter/lab/user-settings/@jupyterlab/apputils-extension/themes.jupyterlab-settings && \
    echo "}" >> /root/.jupyter/lab/user-settings/@jupyterlab/apputils-extension/themes.jupyterlab-settings

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8888

CMD [ "jupyter", "lab", "--allow-root", "--ip=0.0.0.0" ]
