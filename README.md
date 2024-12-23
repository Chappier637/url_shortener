# url-shortener

## Descriprion

This is a learning prokect for Data Engineering program at HSE.

The goal is to create service for shorting URLs using FastAPI

## Methods

- POST /shortern - generates short_id for for URL im input
- GET /{short_id} - redirects to URL associated with given short_id
- GET /stats/{short_id} -returns clicks statistics of given short_id
- PUT /short_id - updates existing short_id item
- DELETE /short_id - deletes existing short_id item

## Deployment

### Github

- Clone github project
```
  git clone https://github.com/Chappier637/url_shortener.git
```
- Switch to app directory
```
  cd app
```
- Update pip and install modules from requirements.txt
```
  python3 -m pip install --upgrade pip
```
```
  pip install -r requirements.txt
```
- Compiling docker image
```
  docker build -t <your path> .
```
- Start docker container
```
  docker run -d -p 8000:80 -v shortner-data:/app/data <your image name>
```

### From Docker
```
docker run -d -p 8000:80 -v shortner-data:/app/data tymerrit/shortner-sqlite
```
