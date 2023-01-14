# Securing Your Server with Certbot: A Step-by-Step Guide to Easy SSL Installation

In today's digital world, security is more important than ever. One crucial aspect of ensuring your online presence's safety is using Secure Socket Layer (SSL) certificates. These certificates not only encrypt the data transmitted to and from your website but also help establish trust with your users and improve your search engine rankings. This article will discuss how to easily install Certbot on your server to secure your website with an SSL certificate.

## Load Balancing Server

The first step is to connect to your load-balancing server, which will secure all incoming and outgoing traffic to your other slave servers. For this tutorial, I'll be using an HAProxy-configured server.

```apache
$ ssh hostname@IP-address
```

## Compatibility

The next step to installing Certbot, the official Let's Encrypt client, is to ensure that your server meets the requirements for running Certbot. This includes having a version of Linux that is supported by Certbot, as well as having a web server (such as Apache or Nginx) that is configured to serve your website.

## Installation

Once you have confirmed that your server meets the requirements, the next step is to install the Certbot package for your Linux distribution. This can typically be done using your system's package manager (e.g. `apt-get` on Ubuntu or `yum` on CentOS).

To install, simply run these commands on your CLI one after the other.

```apache
// refresh and install core
$ sudo snap install core
$ sudo snap refresh core

// uninstall certbot incase there is an exsiting installation
$ sudo apt-get remove certbot

// install certbot
$ sudo snap install --classic certbot
```

## Symbolic link

After a successful installation, we need to create a symbolic link to the certbot directory.

```apache
$ sudo ln -s /snap/bin/certbot /usr/bin/certbot
```

## Disable HAProxy

The next step is to ensure that HAProxy is disabled by running the below command.

```apache
$ sudo systemctl stop haproxy
```

## Obtain a Certificate

To obtain a new certificate, you can use the `certbot certonly` command with the `--webroot` or `--standalone` options.

The `--webroot` an option allows you to specify the web root directory of your website, while the `--standalone` option starts its web server to verify that you control the domain you are requesting a certificate for.

Examples:

```apache
$ certbot certonly --webroot -w /var/www/example -d example.com -d www.example.com

// or

$ certbot certonly --standalone -d example.com -d www.example.com

// once completed, remember to start HAProxy
$ sudo systemctl start haproxy
```

The above examples show how to obtain a certificate for the domain [`example.com`](http://example.com) and its subdomain [`www.example.com`](http://www.example.com)

Note that the `certbot certonly` the command is used to obtain a new certificate, and it does not automatically install the certificate on your web server.

To install it on your web server, make sure to add the certificate *usually ending with* `.pem` to your HAProxy config file.

Once all of these are done, restart your server so that all of your changes can take effect.

## Conclusion

In conclusion, Certbot is a powerful tool that allows you to easily obtain and install SSL/TLS certificates from Let's Encrypt. By ensuring that your server meets the requirements, installing the Certbot package, and using the appropriate `certbot` command, you can quickly and securely encrypt your website's traffic. It is also important to note that you can use the `certbot renew` command to automatically renew your certificates before they expire, which helps ensure that your website remains secure and accessible to your users. Certbot is an essential tool for website administrators who want to keep their websites secure and improve their search engine ranking.