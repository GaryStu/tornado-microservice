FROM python:3.7-alpine

EXPOSE 6000

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY python-libs.txt /usr/src/app/
RUN pip install --no-cache-dir -r python-libs.txt

COPY listing_service.py .
COPY listings.db .

CMD ["python3", "listing_service.py"]