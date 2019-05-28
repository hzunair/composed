* Make app.py
* Make requirements.txt
* Make Dockerfile
* Make docker-compose.yml
* Run ```docker-compose up``` to start app
* Go to http://127.0.0.1:5000/
* Edit the Compose file to add a bind mount:
```
version: '3'
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
    environment:
      FLASK_ENV: development
  redis:
    image: "redis:alpine"
```


* Run ```docker-compose up``` to re-build app an run with Compose
* Inside code make an update
* Refresh URL. You should see change.
* Close, ```docker-compose down```.
