# spark_with_docker
Для сборки и старта контейнера необходимо выполнить docker.sh При этом получим: Pull the image from Docker Repository

docker pull sequenceiq/spark:1.6.0
Building the image

docker build --rm -t sequenceiq/spark:1.6.0 .
Running the image

if using boot2docker make sure your VM has more than 2GB memory
in your /etc/hosts file add $(boot2docker ip) as host 'sandbox' to make it easier to access your sandbox UI
open yarn UI ports when running container
docker run -it -p 8088:8088 -p 8042:8042 -p 4040:4040 -h sandbox sequenceiq/spark:1.6.0 bash Далее используем run-ranker.sh для запуска
