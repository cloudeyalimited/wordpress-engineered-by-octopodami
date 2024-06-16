# WordPress Engineered by OCTOPODAMI (WEBO) SSL

You can secure your Octopodami installation with an SSL certificate by following the instructions below.

+ Login into your domain registrar.
+ Update your domain `A` or `CNAME` record to point to the EC2 Instance IP Address.
+ Login into your WordPress dashboard and update `WordPress Address (URL)` and `Site Address (URL)`. For example, `http://mydomainname.com`
+ Wait for 15-20 minutes so DNS can propagate.
+ Login into the EC2 instance via the terminal.
+ Run these commands:

```sh
sudo su -
yum update -y
amazon-linux-extras install epel -y
yum install certbot python2-certbot-nginx -y
sudo certbot --nginx
## Answer all the questions (this is a comment)
## Then, specify your domain name (this is a comment)
sudo certbot renew --dry-run
```

+ Access your domain name (`https://mydomainname.com`) in the browser.

## Links

1. [Product Website](https://aws.amazon.com/marketplace/pp/prodview-iyn7nuvxxqcjg)
2. [EULA](./octopodamiEULA.txt)
3. [Knowledgebase](https://github.com/cloudeyalimited/wordpress-engineered-by-octopodami/-/wikis/home)
4. [Issue Tracking](https://github.com/cloudeyalimited/wordpress-engineered-by-octopodami/-/issues)
5. [Changelog](./changelog.md)

## Support

[Email](mailto:tech@cloudeya.org) support is available to Amazon Web Services Marketplace Customers. We do not offer refunds, but you may terminate your WordPress Engineered by OCTOPODAMI (WEBO) Stack at any time.

## License

The documentation is published under [BSD 3-Clause License](license.txt).

## Copyright

(c) 2020 - 2024 [Cloudeya Limited](https://cloudeya.org).