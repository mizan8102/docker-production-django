```bash
version: '3.7'

services:
  django_gunicorn:
    volumes:
      - static:/static
    env_file:
      - .env
    build:
      context: .
    ports:
      - "8000:8000"
  nginx:
    image: nginx:latest
    ports:
      - "10080:80"
      - "10443:443"
    build: ./nginx
    volumes:
      - .:/app
      - ./config/nginx:/etc/nginx/conf.d
      - ./static_cdn:/static
      - static:/static
    depends_on:
      - django_gunicorn

volumes:
  static:


```
