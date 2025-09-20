FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt* /tmp/ 2>$null || true
COPY app/requirements.txt* /tmp/ 2>$null || true
RUN set -eux; \
    pip install --no-cache-dir --upgrade pip; \
    if [ -f /tmp/requirements.txt ]; then pip install --no-cache-dir -r /tmp/requirements.txt; \
    elif [ -f /tmp/app/requirements.txt ]; then pip install --no-cache-dir -r /tmp/app/requirements.txt; \
    else pip install --no-cache-dir fastapi "uvicorn[standard]" pydantic sqlalchemy; fi
COPY . /app
ENV PORT=8000
EXPOSE 8000
CMD ["bash","-lc","uvicorn app.main:app --host 0.0.0.0 --port ${PORT}"]
