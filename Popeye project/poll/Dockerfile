FROM python:3

COPY . .

#Insralling requirements
RUN pip3 install -r requirements.txt

#Expose port
EXPOSE 80

CMD ["flask", "run", "--host=0.0.0.0", "--port=80"]