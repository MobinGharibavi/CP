# Dashboard


# Deployment 

### CI CD 
There ways to deal with gitlab-runner

1 - Using Docker

    docker compose -f docker-compose.gitlab.yml up -d    

    docker run --rm -v /home/ubuntu/jewerly/ecommerce-backend/docker/deployment/gitlab-runner/config/:/etc/gitlab-runner gitlab/gitlab-runner register \
    --non-interactive \
    --url https://gitlab.com/ \
    --token glrt-GVgqrLXutBfyUSLPz9Aj \
    --executor "docker" \
    --docker-image docker:stable \
    --docker-privileged \
    --description "Docker Runner"
For more detail please check:

https://medium.com/@truongbui95/exploring-gitlab-ci-cd-ce6a7ffb5746



2 - Using gitlab-runner service

- Download binary file
- Install the binary with

      `dpkg -i gitlab-runner_<arch>.deb`
- Register Runner with

    `gitlab-runner register \
    --non-interactive \
    --url https://gitlab.com/ \
    --token glrt-_TOKEN \
    --executor "docker" \
    --docker-image docker:stable \
    --docker-privileged \
    --tag-list deployment \
    --description "Docker Runner"`

gitlab-runner register --url https://gitlab.com --token glrt-_fs8CKVxtcj12czixCk7


To install the latest version of gitlab-runner you have to follow below page introduction

https://docs.gitlab.com/runner/install/linux-manually.html
