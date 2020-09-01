# Indexing Skilljar LMS using the Generic REST API Connector

## Use case
This example shows how to index Skilljar's training content.

## Pre-requisites
In order to fully understand and use this example, you must:
1. Have a Coveo platform organization
2. Learn about [Coveo Connectivity](https://docs.coveo.com/en/1702/cloud-v2-administrators/add-or-edit-a-source-using-one-of-the-available-connectors)
3. Learn [how to configure a Generic REST API Connector](https://docs.coveo.com/en/1896/cloud-v2-administrators/add-or-edit-a-generic-rest-api-source)

## Step-by-step guide
The two typical objects that get indexed are:
* **Published courses:** https://api.skilljar.com/v1/domains/training.<<ADD_YOUR_DOMAIN_HERE>>.com/published-courses
* **Course series:** https://api.skilljar.com/v1/domains/training.<<ADD_YOUR_DOMAIN_HERE>>.com/course-series

1. Get Skilljar API Key (using Basic Authentication).
2. Create a Generic REST API Source.
3. On the authentication section add your API Key.
4. Configure your Generic REST API source according to the example in SourceJSONConfig.json.
    * This example retrieves the list of published courses (frist endpoint), the course description (using a subquery in the first endpoing), and the course series (using a second endpoint).
5. Make sure you've changed all "placeholders" with your own values, and have adjusted the configuration to your own needs.
6. [Create the appropiate fields and mappings](https://docs.coveo.com/en/1896/cloud-v2-administrators/add-or-edit-a-generic-rest-api-source#completion): In your Coveo Cloud platofrm, make sure you map the fields required ("skjid").

## References
* https://api.skilljar.com/docs/#!/domains
* http://support.skilljar.com/hc/en-us/articles/203811260-Getting-started-with-the-Skilljar-API