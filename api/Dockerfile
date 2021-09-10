FROM python:3
WORKDIR /app
ENV PYTHONPATH=/app/src
COPY requirements.* .
RUN pip install pip-tools && pip-compile && pip-sync
COPY . .
EXPOSE 8000
CMD ["uvicorn", "server:app", "--host", "0.0.0.0", "--reload"]