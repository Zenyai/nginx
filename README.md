### Usage

Pull this repo and run

    docker build -t zenyai/nginx .

To start docker runs

    docker run -d -p 80:80 zenyai/nginx

#### Attach persistent/shared directories

    docker run -d -p 80:80 -v <sites-enabled-dir>:/etc/nginx/conf.d -v <certs-dir>:/etc/nginx/certs -v <log-dir>:/var/log/nginx -v <html-dir>:/var/www/html zenyai/nginx

After few seconds, open `http://<host>` to see the welcome page.
