docker run -dt --name csvserver infracloudio/csvserver:latest /bin/bash

docker run -dt --name my_csv_container -v "$(pwd)/inputFile:/data/inputFile" infracloudio/csvserver:latest /bin/bash

docker stop <container_ID>
docker rm <container_ID>

docker exec -it my_csv_container netstat -tulnp

docker run -dt -p 9393:9393 --name my_app_container infracloudio/csvserver:latest /bin/bash

docker stop <container_ID>
docker rm <container_ID>

docker run -d --name csvserver_app -v /mnt/d/nagaraj/csvserver/solution/inputFile:/csvserver/inputdata -e CSVSERVER_BORDER=Orange -p 9393:9300 infracloudio/csvserver:latest

