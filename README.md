# Homestead WordPress Multisite Nginx Configuration

Nginx templates that handle WordPress Multisite URLs correctly in Homestead. 

### Prerequisites

You should already have a working Homestead Vagrant installation on your system.

[Laravel Homestead](https://laravel.com/docs/master/homestead)

### Installing

Copy wordpress-multisite-sub-domains.sh and wordpress-multisite-sub-directories.sh into the scripts/site-types folder of your Homestead folder.

```
homestead/scripts/site-types/wordpress-multisite-sub-domains.sh
homestead/scripts/site-types/wordpress-multisite-sub-directories.sh
```

## Configuration

In your Homestead.yaml add a type parameter to your site using the desired multisite setup (subdomain or subdirectory). The type references the filename used for the .sh file.

```
- map: subdomains-example.test
  to: /home/vagrant/code/subdomains-example
  type: wordpress-multisite-sub-domains
- map: subdirectories-example.test
  to: /home/vagrant/code/subdirectories-example
  type: wordpress-multisite-sub-directories
```

## Deployment

When you vagrant up Homestead will apply the specified Nginx configuration for that specific site.

## License

This project is licensed under the GPL V2 License - see the [LICENSE.md](LICENSE.md) file for details

