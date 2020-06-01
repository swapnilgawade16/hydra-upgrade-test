# hydra-upgrade-test

**Steps to reproduce migration issue**

1) Install MySQL and run hydra migrate sql
```
$docker-compose up
```

2) Install hydra v1.0.0
```
$docker-compose -f docker-compose.yaml -f docker-compose-install-v1.0.0.yaml up
```

2) Migrate to hydra v1.3
```
$docker-compose -f docker-compose.yaml -f docker-compose-install-v1.0.0.yaml -f docker-compose-migrate-v1.3.yaml up
```

3) Migrate to hydra v1.4
```
$docker-compose -f docker-compose.yaml -f docker-compose-install-v1.0.0.yaml -f docker-compose-migrate-v1.4.yaml up
```

**Expected test results**
- Migration from v1.0.0 to v1.3 should work
- Migration from v1.3 to v1.4 should fail with below error
```
error="cipher: message authentication failed"
```