docker compose new steps

install docker compose:
apt install docker-compose

build image for frontend: 
docker build -t sfit-php-mysql-demo:1.0.0 .

now create container: 
docker run -itd -p 80:80 --name sfit-php-mysql-app -v "$(pwd)"/www:/var/www/html sfit-php-mysql-demo:1.0.0


check on browser
http://url:80


now stop this running container:
docker stop containerid

now docker-compose up:
docker-compose up --build


check all the links: 
:30002 for php myadmin and then import the sql file in moe table
then reach url:80/mysql-connect.php to see the output