# ComputeStacks images for running ElasticSearch with Wordpress

This repo containers the two images required in order to make ElasticSearch and Wordpress work together: 

* [ElasticSearch](https://github.com/ComputeStacks/cs-docker-es-for-wp/tree/main/elasticsearch/v6)
* The nginx [load balancer](https://github.com/ComputeStacks/cs-docker-es-for-wp/tree/main/nginx-lb/v1)

In order to use this, you will need to install the [ElasticPress](https://wordpress.org/plugins/elasticpress/) wordpress plugin. 


## Configuring ElasticPress

1. After installing the plugin in wordpress and activating it, navigate to the plugin settings and choose the "Self-Hosted" option.
2. Add in your ElasticSearch URL. You can find your URL by:

    * (a) Navigate to the ElasticSearch service in your project.
    * (b) Your URL will be the only URL listed under 'Domains'.
    * (c) Your Password will also be shown on this page. Click 'show' to reveal it.

    Your URL will be in the format: `https://admin:PASSWORD@URL`

3. After entering your URL, continue through the ElasticPress setup wizard.

