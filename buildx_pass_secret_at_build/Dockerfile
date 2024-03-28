FROM ubuntu:22.04

WORKDIR /app

COPY . /app

RUN python3 --version

RUN --mount=type=secret,id=aws,target=./.env  \
    python3 main.py

CMD [ "sleep", "8000" ]

# docker build --secret id=aws,src=./.env .