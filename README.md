# TechDivision.Jobs
This is a package for integrating jobs into your site.  
In order to be properly indexed as jobs in google (and other search engines), job semantics need to be correct.  

This is a good read to start with: https://developers.google.com/search/docs/data-types/job-posting 

### Installation
TechDivision.Jobs is available via packagist. Add `"techdivision/jobs" : "~1.0"` to the require section of the composer.json
or run `composer require techdivision/jobs`.  


## What this package offers
You can add the following NodeTypes:
* Job Postings
* Job Locations
* Hiring Organization
* Job List

If you use [ttree/linkedData](https://github.com/ttreeagency/LinkedData) to provide proper json+ld, we also added the required options.

## For editors
Add a Job Overview Document. There you find Content Collections for Locations and Organizations 
which you will need in your Job Postings.  
Below the Job Overview, you can add Job Posting Documents. 
Wherever you want you can add a Job List that displays a simple table of your job offers.

## For developers
This page only delivers some basic NodeTypes and Fusion rendering.
You can adjust it to your needs as you want. We tried to follow Neos best practices.
There is not much rendering for JobPostings whatsoever - this is hard to generalize. What we do is add microdata.
If you want to display the properties to be e.g. inline-editable, you can do so.

### Page output
If you are using your own Fusion Page Prototype instead of Neos.Neos:Page, please inherit from this Page Object
```
prototype(TechDivision.Jobs:Page) >
prototype(TechDivision.Jobs:Page) < prototype(Your.Awesome.Package:Document.PageTemplate)
```
## More Information
If you want to change your logo in search results, check this:
https://developers.google.com/search/docs/guides/enhance-site#provide-business-contact-markup

## Other packages
To make jobs complete, we do offer a set of packages:
* [techdivision/jobs-cards](https://github.com/techdivision/jobs-cards)  
Visual card style for jobs (see also [techdivision/card](https://github.com/techdivision/card))
* [techdivision/jobs-googleapi](https://github.com/techdivision/jobs-googleapi)  
Tell google if you have new jobs, important changes or if a job has been deleted 
* [techdivision/jobs-applicationform](https://github.com/techdivision/jobs-applicationform)  
An application form based on [neos/form-builder](https://github.com/neos/formbuilder)
* [techdivision/form-encryption](https://github.com/techdivision/form-encryption)  
PGP/GPG form encryption to meet data protection standards 

## Update notes

### Breaking changes for update from 1.x.x to 2.x.x

The content of the property `jobPostingEmploymentType` will be lost due to the change of a variable text input to a predefined select.