# Compile for Containerization


## Step 1: Build the docker container of Swirl

```
docker build . -t swirl-search:latest
```

## Step 2: Start Up Swirl

Run `docker compose up` to start up swirl

## Step 3: Setup Super User

```
docker exec -it [Swirl Container] python manage.py createsuperuser --email admin@example.com --username admin --password admin
```

## Step 4: Load Pre-packaged Search Providers

```
docker exec -it [Swirl Container] python scripts/swirl_load.py SearchProviders/google_pse.json -u admin -p your-admin-password
```


