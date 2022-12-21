# Elastic stack v6.8 for M1 Mac

I needed to run the Elastic stack in version 6.8 for some internal tests so I created a `docker-compose` deployment for quick, easy and portable installation.

However, I found out that the Docker image for 6.8 does not support M1 Macs. Thanks to [this response in StackOverflow](https://stackoverflow.com/a/70713284/17967885), I created the [Dockerfile](./elastic-stack-6.8-for-M1-Mac/elasticsearch/Dockerfile) and it works!

Anyone cloning this repo can use it by simply running `docker-compose up --build`.

## 🤩 Want to reuse this for more recent versions?

Of course you can! If you want to set a lab for a released version that already supports M1 Mac ARM builds, you can adapt the `docker-compose.yml` file by commenting the line `build: ./elasticsearch` and use the `image: docker.elastic.co/elasticsearch/elasticsearch:{MY_VERSION}` and `volumes:` to mount the `elasticsearch.yml` config file.

Save the file, run `docker-compose up`, and wait for the magic to happen. :tada:
