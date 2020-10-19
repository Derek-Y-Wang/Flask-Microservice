FROM python:3.6

RUN pip3 install pipenv

ENV PROJECT_DIR /Flask-Microservice/REST_API_Microservice/FlaskBookAPI


WORKDIR ${PROJECT_DIR}

COPY Pipfile .
COPY Pipfile.lock .
COPY . .

RUN pipenv install --deploy --ignore-pipfile

EXPOSE 5000

CMD ["pipenv", "run", "python", "api.py"]
