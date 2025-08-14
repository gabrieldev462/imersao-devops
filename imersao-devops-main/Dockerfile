# Use uma imagem oficial do Python como imagem base
FROM python:3.10-slim

# Defina o diretório de trabalho no contêiner
WORKDIR /app

# Copie o arquivo de dependências para o contêiner
COPY requirements.txt .

# Instale as dependências
RUN pip install --no-cache-dir -r requirements.txt

# Copie o restante do código da aplicação para o contêiner
COPY . .

# Exponha a porta 8000 para o mundo fora deste contêiner
EXPOSE 8000

# Comando para executar a aplicação (será sobrescrito pelo docker-compose para desenvolvimento)
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]


