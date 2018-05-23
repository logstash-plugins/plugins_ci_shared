# Experimental

Ignore for now.

## Using these definitions

### In a script:

```bash
VERSION=$(curl -s https://raw.githubusercontent.com/logstash-plugins/plugins_ci_shared/master/variables/DEV_6)
```

`VERSION` variable now contains `6.3.0-SNAPSHOT`

### With Travis

```yaml
env:
- LOGSTASH_VERSION=RELEASE_6
- LOGSTASH_VERSION=RELEASE_5
- LOGSTASH_VERSION=DEV_6
- LOGSTASH_VERSION=DEV_7
```

Then the `ci` scripts can use `LOGSTASH_VERSION` to set `VERSION` like so:

```bash
VERSION=$(curl -s https://raw.githubusercontent.com/logstash-plugins/plugins_ci_shared/master/variables/$LOGSTASH_VERSION)
```

## Changing the definitions

Simply edit the files under `variables`.
