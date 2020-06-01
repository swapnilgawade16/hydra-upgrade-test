# hydra-upgrade-test

**Steps to migrate**

1) Install hydra v1.0.0
```
$docker-compose up
```

2) Migrate to hydra v1.3
```
$docker-compose -f docker-compose.yaml -f docker-compose-migrate-v1.3.yaml up
```

3) Migrate to hydra v1.4
```
$docker-compose -f docker-compose.yaml -f docker-compose-migrate-v1.4.yaml up
```
