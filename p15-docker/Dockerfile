# Imagen base — Node 24 en Alpine (versión liviana de Linux)
FROM node:24-alpine

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar primero los archivos de dependencias
# (Docker cachea esta capa si package.json no cambió)
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código
COPY . .

# Puerto que expone la app
EXPOSE 3000

# Comando que se ejecuta al iniciar el contenedor
CMD ["node", "index.js"]
