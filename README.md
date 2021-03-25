# Peekbank Website

Built using [the jekyll-doc-theme](https://aksakalli.github.io/jekyll-doc-theme/).

## Running locally to make changes to site

You need Ruby and gem before starting. Follow the instructions [here](https://jekyllrb.com/docs/installation/). For OS X Big Sur, follow the instructions for installing with `rbenv` [here](https://jekyllrb.com/docs/installation/macos/).

Once you have Ruby and gem, then:

```bash
# install bundler
gem install bundler

# clone the project
git clone https://github.com/langcog/peekbank-website.git
cd peekbank-website

# install gems with bundler
bundle install

# run jekyll with dependencies
bundle exec jekyll serve
```

## How to host Shiny Apps

This site serves shiny apps that are hosted on a separate EC2 instance and displayed using an iframe. To manage the instance, use the LangCog's AWS Management Console. 

To set up a secure shiny server (without purchasing shiny server pro), we followed the steps outlined in this [post](https://www.r-bloggers.com/shiny-https-securing-shiny-open-source-with-ssl/).

The domain name -- peekbank-shiny.com -- was purchased via namecheap and configured to point at the public IP for the Peekbank-shiny EC2 instance following [these](https://u.osu.edu/walujo.1/2016/07/07/associate-namecheap-domain-to-amazon-ec2-instance/) steps.

To connect to the shiny server via https, an SSL certificate was generated using [CertBot](https://certbot.eff.org/lets-encrypt/ubuntuxenial-apache) and linked to the domain peekbank-shiny.com
