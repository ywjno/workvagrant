# WorkVagrant

It contains `git`, `mysql`, `postgresql`, and `oracle java 7` recipes.

Worked in [Oracle VM VirtualBox 4.1.16](https://www.virtualbox.org/) and [Ubuntu 12.04 LTS](http://www.ubuntu.com/).

## How to use

change ubuntu sources list in `change_sources_list.sh` file FIRST.

```bash
git clone git://github.com/ywjno/workvagrant.git
cd workvagrant
bundle install
rake install_chef
rake up
```

run `rake -T` find other command.

## THANKS

[Vagarnt](http://vagrantup.com/)

[FireUp](https://github.com/SaitoWu/fireup)
