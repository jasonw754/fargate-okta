FROM python:3
ENV ENV=dev
COPY requirements.* .
RUN pip install pip-tools && pip-compile && pip-sync
EXPOSE 8000
CMD ["uvicorn", "server:app", "--host", "0.0.0.0", "--reload"]