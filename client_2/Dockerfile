FROM python

RUN apt-get update \
	&& apt-get install -y --no-install-recommends && rm -rf /var/lib/apt/lists/*

WORKDIR /client
COPY client_2/requirements.txt ./
RUN pip install -r requirements.txt

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
