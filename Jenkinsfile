node {
    stage "Create build output"
    docker run kharchenkov/mysql -e MYSQL_ROOT_PASSWORD=pass --volume db:/var/lib/mysql
    docker run kharchenkov/php -p 80:80 -v ./html:/var/www/html
    db:
    
}