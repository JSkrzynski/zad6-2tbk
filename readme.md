Kontenery znajdują się w tej samej sieci (test-net). Klient przy uruchomieniu wysyła zapytanie na adres kontenera serwera. 

```
docker build -t JSkrzynski_server .       {-- Używamy znajdując się w folderze server
docker build -t JSkrzynski_client .                         oraz client              --}

docker network create test-net

docker run -d --name server --network test-net -p 9000 JSkrzynski_server
docker run -d --name client --network test-net -p 3000 JSkrzynski_client
```
