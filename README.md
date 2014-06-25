vagrant-logplex
===============


Setup
====

Install vagrant dependencies

```bash
    vagrant plugin install vagrant-berkshelf --plugin-version '>= 2.0.1'
    vagrant plugin install vagrant-omnibus
```

Vagrant up

```bash
    vagrant up
```

Logplex Configuration
=====================

Chef will automatically create a "full access" user for logplex with username `logplex-user` and password `logplex-user` ([see](https://github.com/rstudio/vagrant-logplex/blob/master/data_bags/logplex/users.json))
