# Elastic stack v6.8 for M1 Mac

I needed to run the Elastic stack in version 6.8 for some internal tests so I created a `docker-compose` deployment for quick, easy and portable installation.

However, I found out that the Docker image for 6.8 does not support M1 Macs. Thanks to [this response in StackOverflow](https://stackoverflow.com/a/70713284/17967885), I created the [Dockerfile](./elastic-stack-6.8-for-M1-Mac/elasticsearch/Dockerfile) and it works!

Anyone cloning this repo can use it by simply running `docker-compose up --build`.
