# DB Server Setup

Currently sets up MySQL only. May combine other servers in the future or create separate scripts for them.

## Certificates

I was unable to get the certificates to work with anything other than the default names in the default locations. Locally, name them after the domain name of the server you are configuring. For example:

* example.com.crt
* example.com.key

Put these in the `certs/` directory along with the `myCA.pem`.

## Variables

Create a `vault.yml` file based on `vault.yml.example`

## SSL

Some of the ansible modules aren't configured to work with SSL, so if you need to re-run anything after SSL has been set up, you may need to disable SSL and re-enable it afterwards. Some tasks are skipped if the `/etc/mysql/mysql.conf.d/mysql_ssl.cnf` file exists.
