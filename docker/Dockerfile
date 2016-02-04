FROM ubuntu:latest

RUN apt-get update -y
RUN apt-get install -y build-essential python3 python3-pip python3-dev
RUN pip3 install jupyter

EXPOSE 8888

CMD ["jupyter", "notebook", "--ip='*'"]
