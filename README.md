
# Template used
* [Pavo](https://onepagelove.com/pavo)

# Technologies used
* [Bootstrap 4/5](https://getbootstrap.com/)
* [rrweb library](https://github.com/rrweb-io/rrweb)
* [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/)
* [PostgreSQL](https://www.postgresql.org/)
* [PgAdmin](https://www.pgadmin.org/)
* [Docker](https://www.docker.com/)
* [DigitalOcean](https://www.digitalocean.com/) and [Play with Docker](https://labs.play-with-docker.com/)

# Resources Used
* [Record and Replay the Web: A rrweb Tale](http://www.myriptide.com/rrweb-introduction/)

# Getting Started

## Install chrome extension
* [install moesif-origin-cors-change chrome extension](https://chrome.google.com/webstore/detail/moesif-origin-cors-change/digfbfaphojjndkpccljibejjbppifbc)

## Clone repository

```
git clone https://github.com/soufianeodf/record-in-video-website-visits.git

cd record-in-video-website-visits
```

* Replace localhost with server ip-address
```
sed -i 's/localhost/ip-address/g' .env
sed -i 's/localhost/ip-address/g' website/website/index.html
sed -i 's/localhost/ip-address/g' website/website/replay.html
```

## Deploy on DigitalOcean (method 1)

* Create a droplet
  

* ssh into it
```
ssh root@ip
```

* Open the following ports
```
sudo ufw allow 80/tcp
sudo ufw allow 8080/tcp
sudo ufw allow 55432/tcp
sudo ufw allow 16543/tcp
```

* Run docker compose
```
docker-compose up
```

## Deploy on Play-with-Docker (method 2: free)
* Update alpine
```
apk update
```

* Run docker compose
```
docker-compose up
```

* Open all ports
```
netstat -lntu
```

# License

Licensed under the [Apache License](LICENSE).
