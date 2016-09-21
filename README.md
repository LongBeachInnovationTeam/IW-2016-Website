# IW-2016-Website

Built using [Hugo](https://gohugo.io/) and a modified version of the [Creative theme](http://themes.gohugo.io/creative/) provided by Hugo.

## Required software

The latest version of the [Hugo](https://gohugo.io/) static site generator.

## Modifying the site

- Modify `config.toml` to modify the main text content of the site
- Modify files in the `/themes/hugo-creative-theme/layouts/` directory to change the HTML files to change presentation and rendering of the site elements
- Run `hugo` on the command line to generate the site

### Adding events
- Create a new file under `/data/speakers`
- Add relevant event image to `/themes/hugo-creative-theme/static/img/speakers/`. Images should be 650x350 px
- Run `hugo` on the command line to generate the site

An example of an event:

```yaml
modalID: 1
title: Test Event
img: 1.png
speaker: The City of Long Beach
date: 2016-10-01
presentationDate: Thursday, October 6th 9am
location: Congregation Ale House
description: | 
 A multi-line description of the event here.
link: http://example.com/registration
```

Note that `date` specifies a YAML date that will be used to render the events in ascending date order while `presentationDate` specifies the date presented on the webiste, e.g. "January 1, 2016 9am-4pm".

## Deployment

The static version of the site is compiled into `public/`. Copy everything from `public/` into your deployment target. The site is currenlt hosted in an AWS S3 bucket.
