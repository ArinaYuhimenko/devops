#FROM openjdk:latest
FROM nginx

# Копируем файлы настроек и index.html в контейнер
COPY config/ /config/
COPY index.html /index.html

# Устанавливаем nginx
RUN apt-get update && apt-get install -y nginx

# Очищаем кэш apt-get
RUN rm -rf /var/lib/apt/lists/*

# Открываем порты для доступа к веб-серверу
EXPOSE 80

# Запускаем nginx в фоновом режиме
CMD ["nginx", "-g", "daemon off;"]