FROM python
RUN apt-get update && apt-get install -y \
    python3-pip
RUN alias python=python3 &&  pip=pip3
RUN pip install \
    flask \
    flask_cors
CMD main.py