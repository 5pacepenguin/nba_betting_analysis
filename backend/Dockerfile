FROM python:3.9.16-buster

COPY requirements_testing.txt requirements.txt
RUN mkdir -p data/pkl
COPY api api
COPY py_files py_files
COPY data/pkl/ngdemo.pkl data/pkl/ngdemo.pkl
COPY data/pkl/boxscores_advanced_team_all.pkl data/pkl/boxscores_advanced_team_all.pkl
COPY data/pkl/demo_2023-03-16.pkl data/pkl/demo_2023-03-16.pkl

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

CMD uvicorn api.fast:app --host 0.0.0.0 --port $PORT
