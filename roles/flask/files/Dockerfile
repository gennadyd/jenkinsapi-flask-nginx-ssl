# Start from python
FROM python:3.7.10
# PACKAGES
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt

# RUN FLASK APP
EXPOSE 5000
ENTRYPOINT ["python"]
CMD ["app.py"]
