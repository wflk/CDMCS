# Reputation

see
* https://redmine.openinfosecfoundation.org/projects/suricata/wiki/IP_Reputation
* https://redmine.openinfosecfoundation.org/projects/suricata/wiki/IPReputationConfig
* https://redmine.openinfosecfoundation.org/projects/suricata/wiki/IPReputationFormat
* https://redmine.openinfosecfoundation.org/projects/suricata/wiki/IPReputationRules

#### configuration

```
#reputation-categories-file: /usr/local/etc/suricata/iprep/categories.txt
#default-reputation-path: /usr/local/etc/suricata/iprep
#reputation-files:
# - reputation.list
```

#### Categories file

The categories file provides a mapping between a category number, short name and long description.


```
<id>,<short name>,<discription>
```

#### Reputation file
The reputation file lists a reputation score for hosts in the categories.

```
<ip>,<cat>,<score>
```

#### Reload

Only the reputation files will be reloaded, the categories file won’t be.
If categories change, Suricata should be restarted.