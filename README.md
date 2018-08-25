# odoo-ci
Odoo image to do CI of our public modules.

This image is bases on the official [odoo image](https://hub.docker.com/_/odoo/) but with the adition of the following packages:
* dockerize
* coverage
* codacy-coverage

## Usage

Add this image as the main image on your CircleCI config file.
