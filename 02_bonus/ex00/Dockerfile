FROM python:3
RUN pip install flask
COPY . /home
WORKDIR /home
EXPOSE 3000
ENV FLASK_APP=app/app.py
CMD flask run -h 0.0.0.0 -p 3000

# docker build -t my_flask .
# docker run -it -p 3000:3000 --rm my_flask