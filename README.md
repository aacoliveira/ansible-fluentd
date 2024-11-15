# Deployubg Fluentd with Ansible

## Version

Tested with **ansible [core 2.17.0]**

## Install the required collection

Use the following command:

```
ansible-galaxy collection install community.docker
```

## Check if it went well:

```
ansible-galaxy collection list
```

## Testing the config

To run it locally:

```bash
docker container run -p 9880:9880 -v $(pwd)/fluentd-file:/fluentd/etc fluent/fluentd:edge-debian -c /fluentd/etc/fluentd.conf
```