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
  + php_app1<br/>
    - index.php<br/>
  + php_app2<br/>
    - index.php<br/>
  + php_app3<br/>
    - index.php<br/>
  + php_app4<br/>
    - index.php<br/>
  + php_app5<br/>
    - index.php<br/>
  + php_app6<br/>
    - index.php <br/><br/><br/>

C. DEPLOY Container<br/>
1. Download <br/>
   git clone https://github.com/masihgurutkj/docker-compose_lampp-loadbalancing.git \ <br/>
   cd lampp-loadbalancing \ <br/>
2. Deploy <br/>
   docker-compose -p 'lampp' up    <br/>
   docker-compose -p 'lampp' up -d  ## Mode Daemon<br/>
3. Start/Stop  <br/>
   docker-compose -p 'lampp' start <br/>
   docker-compose -p 'lampp' stop <br/>
   docker-compose -p 'lampp' down ## Mode bersi-bersih Container <br/>

