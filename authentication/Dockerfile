FROM python

RUN apt-get update \
	&& apt-get install -y --no-install-recommends && rm -rf /var/lib/apt/lists/*

WORKDIR /authentication
COPY authentication/requirements.txt ./
RUN pip install -r requirements.txt

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
