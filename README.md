# Ansible role `DNS`

An Ansible role for configuring DNS servers in /etc/resolv.conf

-

## Requirements

No specific requirements

## Role Variables


| Variable     | Default         | Comments (type)                        |
| :---         | :---            | :---                                   |
| `dns_domain` | localhost.local | Domain name                            |
| `dns_search` | localhost.local | Search domain                          |
| `dns_intname`| eth0            | Interface name for interface in domain |
| `dns_options`| options single-request-reopen | Options for DNS          |
| `dns_nameservers` |       | Nameservers to be added to /etc/resolv.conf |

## Dependencies

No dependencies.

## Examples
- Add nameservers
```
dns_nameservers: 
  - 192.168.1.10
  - 10.0.2.3
```


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Github can then easily create a PR based on that branch. Don't forget to add your name to the contributor list below!

## License

2-clause BSD license, see [LICENSE.md](LICENSE)

## Contributors

- [Bert Van Vreckem](https://github.com/bertvv/) (maintainer of Ansible Skeleton)
- [Lennert Mertens](https://github.com/LennertMertens/)

