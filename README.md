#BOSH release of Zabbix aggent

add following parameters to your stub
```
releases:
- name: cf
  version: "230"
- name: zabbix_agent
  version: "latest"
```

```
properties:
  zabbix:
    host_metadata: cf-openstack
    server_ip: 192.168.111.5
```

Add the template to your job:
```
- {name: zabbix_agentd, release: zabbix_agent}
```

