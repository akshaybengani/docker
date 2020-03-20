# Docker

Docker is a system which provide us functionality to divide our services and software in containerized system. 

## CMD Explanation

```docker
docker container run --publish 80:80 --detach nginx
```
*   Whenever we need to use conatiners either for creating or deleting or modifying we use the argument ```container```
*   To run a container we need ```run``` command.
*   To Publish a container like on a port or server we use the ```--publish``` command with port numbers assigned.
*   The 1st port number is the current system PORT which provide that service. And the 2nd one is the Container port it can be anyone for now but if there is one service I prefer using same port.
*   Since when we run a server it accepts and sends requests in a for loop and wait for the network for an activity, as such these containers dont stop automatically as such we neee to use   ```--detach``` flag to continue running container in background.
*   Now its time to specify the container image name and thats it ```nginx```.

```docker
docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES
c7fb1939cc25        nginx               "nginx -g 'daemon of…"   11 seconds ago      Up 10 seconds       0.0.0.0:80->80/tcp   condescending_robinson
```
* To get information of all running containers we use the parameter ```ps```.
* To get info of all running and not running containers we have to add the flag ```-a``` in the command to list all the containers.
* The container id is always created for us and the name is also required as unique.
* If we dont specify the name it picks a name from an open source list of names.
* The names are of the popular hackers, scientists, researchers and lot more and its interesting sometimes.
```docker
docker conatiner stop 69049265872
```
*   In order to stop a container we need to use the ```stop``` keyword.
*   Next to it is the container ID.

