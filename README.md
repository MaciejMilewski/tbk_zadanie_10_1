# Instrukcja
W folderze z docker-compose.yml:
```sh
docker swarm init 
docker stack deploy -c docker-compose.yml memory_stress_test 
```
Usuwanie:
```sh
.\clean.ps1  
``` 
# Screenshot
#### Po uruchomienia wewnątrz konsoli kontenera
![](images/allocated_memory.jpg)
#### Po osiągnięciu limitu zasobów kontener jest zatrzymywany
![](images/containers.jpg)
#### Inspect
```sh
docker service inspect --pretty memory_stress_test_app
```
![](images/service_inspect.jpg)
#### Widzimy status healthy obecnego kontenera, poprzedni exited
```sh
docker ps -a
```
![](images/docker_ps_a.jpg)