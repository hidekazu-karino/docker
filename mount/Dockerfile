FROM python:3.4
RUN pip install Flask==0.10.1
WORKDIR /app
COPY app /app
EXPOSE 6000
CMD ["python", "server.py"]