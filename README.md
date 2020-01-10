# pm2-free-monitoring

For complete setup, please read this <a href="https://medium.com/@nikunjd.np/pm2-microservices-monitoring-with-grafana-influxdb-54fb6f8b5d2d">article</a>.

Pm2 free monitoring project supports your pm2 organized microservice architecture to monitor all the services free. Pm2 supports key-metrics which is free till the 4 dashboard but after that what?

This project provides free monitoring via Grafana through InfluxDB.

First, You need to clone this repo and install dependent packages via `npm i`.
Then, Insert your pm2 service running sever IP in controller.js and execute via `node app.js` or `npm start`.

Yeah! Your scheduler is now working.

## Configuration

For configuration, create a file `.env` and populate it with the following env variables:

```environment
# the ip of the machine pm2 is running on
PM2_IP=127.0.0.1
HOST_MACHINE=

# InfluxDB connection
DB_HOST=
DB_PORT=8086
DB_USER=
DB_PASS=
DB_NAME=
```

## Deploy
- Copy the pm2-monitoring folder to remote host throuh ssh:
```
scp -r /path/to/pm2-monitoring user@remote.host:/path/to/copy
```
- Access the remote host by ssh, go to the pm2-monitoring folder, install library:
```
npm install
```
- Configure .env file
- Start the pm2-web-interface:
```
pm2 web
```
- Start the tool:
```
npm start
```