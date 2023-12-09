A. CONTAINER : <br/>
- NGINX-LoadBalancing<br/>
- Ubuntu PHP7.4 & PHP8.0<br/>
- MARIADB<br/>
- PHPMyAdmin <br/><br/>

B. DIREKTORI [docker-compose_lampp-loadbalancing]<br/>
  - docker-compose.yml<br/>
  + loadbalance<br/>
    - nginx.conf<br/>
  + mariadb_data<br/>
  + web1<br/>
    - index.php<br/>
  + web2<br/>
    - index.php<br/>
  + web3<br/>
    - index.php<br/><br/>

C. DEPLOY DOCKER  [ Cara-1 ] <br/>
1. Download <br/>
   git clone https://github.com/masihgurutkj/lampp-loadbalancing.git \ <br/>
   cd lampp-loadbalancing  <br/>
2. Deploy <br/>
   docker-compose -p 'lampp' up    <br/>
   docker-compose -p 'lampp' up -d  ## Mode Daemon<br/>
3. Running  <br/>
   docker-compose -p 'lampp' start <br/>
   docker-compose -p 'lampp' stop <br/>
   docker-compose -p 'lampp' down ## Mode bersi-bersih Container <br/>
4. Tes Skrip  <br/>
   touch php_app1/index.php \ <br/>
   echo "\<h1>Server 1<\/h1><\?php phpinfo()\; \?>\" > php_app1/index.php  <br/>

D. DEPLOY DOCKER - CLI BASH [ Cara-2 ] <br/>
apt update -y &&
apt install git &&
git clone https://github.com/masihgurutkj/lampp-nginx.git &&
cd lampp-nginx &&
chmod +x server.sh &&
./server.sh

A. TESTING
Browser http://ipaddress:7007 [PHPMyAdmin]
MySQL user : lampp/lampp
MySQL root : root/lampp
Browser http://ipaddress:7000 [Web]
Browser http://ipaddress:7000/haproxy?stats [Haproxy-Statistik]



   

