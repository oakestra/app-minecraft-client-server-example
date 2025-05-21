# How to build the images yourself? 

# Web Client and Proxy: 
Use the Dockerfile and Dockerfile.proxy respectively from [this repository](https://github.com/giobart/minecraft-web-client).

Build the web client first:
```
docker buildx build --platform linux/amd64,linux/arm64 . -t <your_image_name> 
```

Then build the proxy:
```
docker buildx build --platform linux/amd64,linux/arm64 -f Dockerfile.proxy . -t <your_image_name> 
```

# Server: 


move to the server directory
```
cd server
```

Then build the server:
```
docker buildx build --platform linux/amd64,linux/arm64 --target openhack-1.0 . -t <your_image_name> 
```
