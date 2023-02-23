# Game Projec

Para ejecutar el juego debes seguir las siguiente instrucciones en la terminal:

```sh
cd game
python3 main.py
```

# App Project

```sh
git clone
cd app
python3 -m venv env
source env/bin/activate
pip3 install /r requirements.txt 
python3 main.py
```

# Dockerizando App Project
Se crean los archivos dentro del directorio app:
- docker-compose.yml
- Dockerfile
```sh
cd app
```

Ahora hay que seguir los siguientes pasos para poder desarrollar dentro del contener de docker.

1. Se debe construir la imagen del contenedor o del sistema
```sh
sudo docker compose build
```
2. Para proceder a lanzar el sistema o crear e iniciar la imagen del contenedor
```sh
sudo docker compose up -d
```
3. Para revisar si hay contenedores
```sh
sudo docker compose ps
```
4. Para ingresar al ambiente dentro del contenedor, hay que tener en cuenta que el nombre de la aplicacion o servicio en este caso es "**app-csv**". Por otro lado, la terminal que requerimos es de tipo **bash**.
```sh
sudo docker compose exec app-csv bash
```

Dentro del ambiente de desarrollo del contenedor, se puede ejecutar la aplicación main:
```sh
python main.py
```
