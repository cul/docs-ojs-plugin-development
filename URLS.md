# URLs, OJS and NGINX
## Goals
### Multisite Installation
As a service offering, our first priority is to have multiple journals supported in a single, administered OJS installation.

E.g.: `https://journals.library.columbia.edu/popular_science`

### Custom Domain Support
In rare circumstances requiring executive sponsorship, a journal should be available at a custom domain.

E.g.: `https://omni.columbia.edu`

OJS supports such configurations when the journal's base url is a "subdomain" of the multisite base url. When it is not, we currently can only support this by:
1. Running an independent OJS instance
2. Using the custom domain to proxy for the journal homepage, but serving the content from a "standard" multisite.

## OJS URLs
### Non-RESTful (default)
`https://journals.library.columbia.edu/index.php/popular_science`
### RESTful
`https://journals.library.columbia.edu/popular_science`

RESTful URLs require an NGINX rewrite rule along the lines of:
> location ~ ^/(?!index.php) {
>   rewrite ^/(?!(plugins|lib|templates)).+ /index.php$uri;
> }

#### OJS Configuration
TBD