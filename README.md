# Ansible role `DNS`

An Ansible role for configuring DNS servers



## Requirements

No specific requirements

## Role Variables


| Variable          | Default         | Comments (type)                             |
| :---              | :---            | :---                                        |
| `dns_intname`     | eth0            | Interface name for interface in domain      |
| `dns_nameservers` |                 | Nameservers to be added to /etc/resolv.conf |
| `dns_search`      | avalon.lan      | Configure search domain                     |

## Dependencies

No dependencies.

## Examples

- Add the interface name for which these options are added. This is necessary because all changes are made in the `/etc/sysconfig/network-scripts/ifcfg-eth0` files in order to be persistent
```
dns_intname: eth1
```
- Add nameservers as following, be sure to add `DNS1=`,`DNS=2`etc.
```
dns_nameservers: 
  - "DNS1=192.168.1.10"
  - "DNS2=10.0.2.3"
```

- Add the domain name in which the DNS is sought
```
dns_search: local.domain
```


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch. Don't forget to add your name to the contributor list below!

## License

2-clause BSD license, see [LICENSE.md](LICENSE)

## Contributors

- [Lennert Mertens](https://github.com/LennertMertens/) (maintainer)
- [Bert Van Vreckem](https://github.com/bertvv/) (maintainer of Ansible Skeleton)
