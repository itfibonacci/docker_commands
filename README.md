docker image ls | grep '<none>' | awk '{ print }' | xargs docker image rm
docker build -t myfuckingshit:listentome --no-cache --rm -f Dockerfile .
docker image rm -f 
docker image rm -f $(docker image ls -q)
