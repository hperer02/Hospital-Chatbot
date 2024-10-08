FROM python:3.11-slim
ARG REQUIREMENTS_CONTENT
WORKDIR /app
COPY ./src/ /app
COPY requirements.txt .
RUN echo "$REQUIREMENTS_CONTENT" > requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
COPY ./pyproject.toml /code/pyproject.toml
RUN pip install /code/.
CMD ["sh", "entrypoint.sh"]