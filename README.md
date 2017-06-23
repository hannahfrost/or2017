# or2017
Hydra in a box workshop for OR 2017


## Introductions
* Who are you?
* Where do you come from?
* What do you do?
* What do you want to learn?

## What is Hydra in a Box
* IMLS Grant with 3 partners, improve access to Samvera (formerly Hydra)
* Study the landscape, formulate use cases and personas. 
* Feature development on the Hyku application.
* One aspect is [HykuDirect](https://hykudirect.com/). Multi-tenant software as a service
  * In the AWS cloud
* Another aspect is "easy to install".

## What is Hyku
* A Samvera application based on the Hyrax library.
  * More about the relationship between Hyku ahd Hyrax:
    * [Hyku and Hyrax: How are they related and how are they different?](https://wiki.duraspace.org/pages/viewpage.action?pageId=85530575)
    * [Where do I start?](http://samvera.github.io/hyku-vs-hyrax.html)
  * [Full feature list](http://hyr.ax/about/#q3)
* Recipes for Docker (easy to install)
* Multi-tenanted (to support the HydraDirect service; not limited to AWS)
* Architectural components: Fedora, Solr, Redis, PostgreSQL, background workers
* Characterizing and transforming files: FITS, imagemagick, openoffice, ghostscript, ffmpeg

## What is Docker

Small containers that run services

> A container image is a lightweight, stand-alone, executable package of a piece of software that includes everything needed to run it: code, runtime, system tools, system libraries, settings. Available for both Linux and Windows based apps, containerized software will always run the same, regardless of the environment. Containers isolate software from its surroundings, for example differences between development and staging environments and help reduce conflicts between teams running different software on the same infrastructure. 


## What is docker-machine?
Docker running inside a VM (e.g. virtualbox), for older operating systems that don't natively support Docker.

## Getting started
* [Docker Installation Instructions](Install.md)
* [Hyku Installation Instructions](InstallHyku.md)
* [Hyku User Documentation](https://wiki.duraspace.org/display/hyku/User+Documentation)

## Tour of features
* Create a new tenant
* Create an admininstrator account
* Language support
* Easily customizable
  * Change labels - "Settings > Labels"
  * Upload banner - "Settings > Appearance > Banner Image"
  * Change colors - "Settings > Appearance > Colors"
* Upload an image
* Create a collection
* Administrative sets
  * Organizing mechanism for objects that have the same management needs
  * Includes a template of access grants
  * A workflow
  * Options for visibility
  * Differences from User Collections
* Create a new administrative set -- turn on mediated deposit
  * Sign in as a new user
  * Upload something else
  * Select the custom admin set (note that permissions tab vanishes)
  * Now submit, notice that it’s “awaiting approval”
  * The work is now hidden from the public context
  * Add a comment
  * Send back for review
  * Log in as submitting user and fix it.
  * Send it through approval
  * The work is no visible to the public
* Batch create works
* Profile & Reports
* File manager
* APIs
  * Linked data
    * Append .ttl to see RDF as Turtle; .jsonld to see JSON-LD
    * curl -H "Accept: text/turtle" https://hyphy.demo.hydrainabox.org/concern/generic\_works/ed526acf-faf4-413e-8b7e-edcfa9eed0d7
    * curl -H "Accept: application/ld+json" https://hyphy.demo.hydrainabox.org/concern/generic\_works/ed526acf-faf4-413e-8b7e-edcfa9eed0d7
  * Resource Sync - show the resource list and change list, show the metadata that gets picked up by RS
  * IIIF + Universal Viewer - grab the manifest.json for an uploaded image, take it to the Mirador demo and paste it in a viewer



## Show some designs that are not yet implemented.

## Some things we haven't finished yet
* Many UI improvements
* Approval UI
* Browse everything integration
* More work types
* Metadata enhancements
* Audio/Video transcoding
* PDF integration with UniversalViewer
* User groups
* Google analytics integration (pulling stats)
* Single sign in [Shibboleth](https://shibboleth.net/) 

https://github.com/samvera-labs/hyku/issues

https://github.com/samvera/hyrax/issues

## What is the Samvera process
* Decentralized
* Open
* Organized
* Collaborative -- No "owners". You are welcome to contribute.


## Get in touch
* [Slack](http://slack.projecthydra.org/) \([Archive](http://project-hydra.slackarchive.io/)\)
* Google Group email list: [samvera-community](https://groups.google.com/forum/#!forum/samvera-community)
* Web:
  * http://samvera.org/
  * http://hyr.ax/
* Documentation: http://samvera.github.io/ (rough)
* Wiki: https://wiki.duraspace.org/display/samvera
* Weekly "tech" phone call

## Other talks
* ["Working with Hydra"](https://www.conftool.net/or2017/index.php?page=browseSessions&form_session=247) session on Thursday morning


## Technical dive (optinal
```
docker exec -it or2017\_workers\_1 bash
rails console
AccountElevator.switch!('sample.localhost')
Image.all
```
