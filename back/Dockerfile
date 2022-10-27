FROM python
RUN apt-get update && apt-get install -y \
    python3-pip \
    wget
RUN alias python=python3 &&  pip=pip3
RUN pip install \
    flask \
    flask_cors \
    gunicorn
CMD rm -rf /etc/systemd/system/backend.service
ADD /backend.service /etc/systemd/system/backend.service
CMD gunicorn --bind 0.0.0.0:8000 wsgi:app
CMD systemctl daemon-reload
CMD systemctl restart backend
  