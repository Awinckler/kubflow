FROM python:latest

ENV DATA_PATH ./data.csv
ENV TRAINED_MODEL_PATH ./trained

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY house_pricing_prediction.py ./
COPY training.py ./
ADD gs:/project/data.csv ./data.csv

CMD [ "python", "training.py" ]