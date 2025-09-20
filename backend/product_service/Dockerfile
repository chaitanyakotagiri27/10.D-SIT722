FROM python:3.11-slim
WORKDIR /app
COPY . /app
RUN pip install --no-cache-dir --upgrade pip \
 && pip install --no-cache-dir fastapi "uvicorn[standard]" pydantic sqlalchemy
ENV PORT=8000
EXPOSE 8000
CMD ["uvicorn","app.main:app","--host","0.0.0.0","--port","8000"]
