## Installation Instructions

1. If Docker is not installed on your device follow
  the instructions set out in this guide:
  https://docs.docker.com/get-docker/
2. Clone this repository from GitHub
3. Open a terminal in the repository directory and 
  type `docker-compose up`
4. The docker container with Kong installed should
  now be running
5. In your seach engine of choice search 'localhost:8002'
  this will direct you to the KONG manager dashboard.
6. From here select services
    - click "+ New Services"
    - Name the service
    - Give the service the Host "httpbin.org"
    - Give the service the Path "/anything"
    - Save/create your new service 
7. Select routes 
    - click "+ New route"
    - Asign the route the service you just created 
    - Name the route
    - Set the method to "GET"
    - Give the service the Path "/anything"
    - Save/create your new route
8. To ensure your new httpbin service is working, using your  
  search engine of choice search "http://localhost:8000/anything"
9. the output should look similar to this:   
    {
    "args": {}, 
    "data": "", 
    "files": {}, 
    "form": {}, 
    "headers": {
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9", 
        "Accept-Encoding": "gzip, deflate, br", 
        "Accept-Language": "en-US,en;q=0.9", 
        "Cache-Control": "max-age=0", 
        "Host": "httpbin.org", 
        "Sec-Ch-Ua": "\"Google Chrome\";v=\"107\", \"Chromium\";v=\"107\", \"Not=A?Brand\";v=\"24\"", 
        "Sec-Ch-Ua-Mobile": "?0", 
        "Sec-Ch-Ua-Platform": "\"Windows\"", 
        "Sec-Fetch-Dest": "document", 
        "Sec-Fetch-Mode": "navigate", 
        "Sec-Fetch-Site": "none", 
        "Sec-Fetch-User": "?1", 
        "Upgrade-Insecure-Requests": "1", 
        "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36", 
        "X-Amzn-Trace-Id": "Root=1-63853135-6f2c9a895ea6ed963d82ab99", 
        "X-Forwarded-Host": "localhost", 
        "X-Forwarded-Path": "/anything", 
        "X-Forwarded-Prefix": "/anything"
    }, 
    "json": null, 
    "method": "GET", 
    "origin": "172.19.0.1, 203.86.192.144", 
    "url": "http://localhost/anything"
    }