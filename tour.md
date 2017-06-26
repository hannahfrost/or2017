---
layout: default
---

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
* Complex works (add a child)
* File manager
* APIs
  * Linked data
    * Append .ttl to see RDF as Turtle; .jsonld to see JSON-LD
    * curl -H "Accept: text/turtle" https://hyphy.demo.hydrainabox.org/concern/generic\_works/ed526acf-faf4-413e-8b7e-edcfa9eed0d7
    * curl -H "Accept: application/ld+json" https://hyphy.demo.hydrainabox.org/concern/generic\_works/ed526acf-faf4-413e-8b7e-edcfa9eed0d7
  * Resource Sync - show the resource list and change list, show the metadata that gets picked up by RS
  * IIIF + Universal Viewer - grab the manifest.json for an uploaded image, take it to the Mirador demo and paste it in a viewer

[Continue to What's Next](whats_next.html)
