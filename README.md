# TurtlePay® Blockchain Cache API

## Setup

1) Clone this repository to wherever you'd like the API to run:

```bash
git clone https://github.com/TurtlePay/blockchain-cache-api
```

2) Install the required Node.js modules

```bash
cd blockchain-cache-api && npm install
```

3) Use your favorite text editor to change the values as necessary in `config.json`

**Note:** Make sure you use a read-only database user for security reasons

```javascript
{
  "bindIp": "0.0.0.0",
  "httpPort": 80,
  "corsHeader": "*"
}
```

4) Fire up the script

```bash
export RABBIT_PUBLIC_SERVER=localhost
export RABBIT_PUBLIC_USERNAME=yourrabbitmqusername
export RABBIT_PUBLIC_PASSWORD=yourrabbitmqpassword
export MYSQL_HOST=localhost
export MYSQL_PORT=3306
export MYSQL_USERNAME=yourdbusername
export MYSQL_PASSWORD=yourdbpassword
export MYSQL_DATABASE=yourdbname
node index.js
```

5) Optionally, install PM2 or another process manager to keep the service running.

```bash
npm install -g pm2@latest
pm2 startup
pm2 start index.js --name blockchain-cache-api -i max
pm2 save
```
###### (c) 2018-2019 TurtlePay® Development Team / wkibbler (CASH2-js)
