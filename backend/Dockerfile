FROM python:3.11-slim

# Carpeta de trabajo dentro del contenedor
WORKDIR /app

# Copiar requirements primero (para cache)
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copiar el backend dentro del contenedor
COPY . .

# Exponer puerto
EXPOSE 8000

# Ejecutar FastAPI
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
