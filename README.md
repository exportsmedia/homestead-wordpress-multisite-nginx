# Homestead WordPress Multisite Nginx Configuration

A default Nginx template that can be used for a subdirectory WordPress Multisite. 

### Prerequisites

You should already have a working Homestead Vagrant installation on your system.

[Laravel Homestead](https://laravel.com/docs/master/homestead)

### Installing

Copy serve-multisite-subdomains.sh and serve-multisite-subdirectories.sh into the scripts folder of your Homestead repo.

```
homestead/scripts/serve-multisite-subdomains.sh
homestead/scripts/serve-multisite-subdirectories.sh
```

## Configuration

In your Homestead.yaml add a type parameter to your site using the desired multisite setup (subdomain or subdirectory). The type references the filename used for the .sh file.

```
- map: subdomains-example.test
  to: /home/vagrant/code/subdomains-example
  type: multisite-subdomains
- map: subdirectories-example.test
  to: /home/vagrant/code/subdirectories-example
  type: multisite-subdirectories
```

## Deployment

When you vagrant up Homestead will apply the specified Nginx configuration for that specific site.

## License

This project is licensed under the GPL V2 License - see the [LICENSE.md](LICENSE.md) file for details

