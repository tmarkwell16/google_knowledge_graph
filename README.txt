# google_knowledge_graph

This is a Drupal module to help generate JSON-LD data, and embed it in the <head> to provide data for the Google Knowledge Graph. This module only generates data for a company, and blog entries. The company data can be configured at /admin/config/system/googlekg.
	
The Blog data is generated on a node-by-node basis. 

The data type is defaulted to BlogPosting, and the Publisher data is generated from the company information configured on the settings page for this module. 

The module checks for an image upload field and if an image has been uploaded. Since the image is a reqired piece of data for the Knowledge Graph, if there is no image uploaded, the module defaults to the company logo.

The description data is pulled from one of three places. First we check to see if a meta description field (from metatags_quick). If there is no meta description field, or the field is empty, we check to see if there is a body summary. If there is no body summary, we pull the data from the body value, and manually trim it to 160 characters and add an elipses. For best results, we recommend using the meta description field, or the body summary.