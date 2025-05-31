# ---- base image -----------------------------------------------------------
FROM python:3.11-slim AS base

# ---- install Python deps --------------------------------------------------
WORKDIR /app
COPY requirements*.txt ./
RUN pip install --no-cache-dir --upgrade pip && \
    if [ -f requirements.txt ]; then pip install --no-cache-dir -r requirements.txt; fi

# ---- copy source & set entrypoint ----------------------------------------
COPY . .
# If your app has a different start-up command, change the line below
CMD ["python", "main.py"]
