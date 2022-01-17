# helloweb
New Website Project

The client would like a very simple single page website that has contains the message "Hello World!" and nothing else. 
The client likes to see the background colour of the page change according to his mood. 
However, you won't know what colour and when, until he calls you to let you know. 
He's very fussy and wants to see the changes as fast as possible.

The website has to be cost effective but at the same time support millions of visitors if needed.

Create a project in a public github repo that contains the website and some tooling that creates and deploys the stack into AWS. 
Please consider using Cloudformation along with a CI/CD tool such as Github Actions. 
The actual webpage styling and content is unimportant so don't waste any time on that. 
The repository doesn't need to contain functioning code but you should demonstrate your considerations.

Make a note of how you would tackle any future features e.g. adding a database or creating an API.


# notes
*First steps: create an IAM user with programmatic access

Creat IAT for Github for github actions

Copy secrets to repo (s3 bucket name and region specified in CFN file)

Edit github actions ymls

Create CFN file to make the s3 bucket and return the value/url

*Next steps:

Done - test github s3push actions - *excluded all yml yaml md files from syncing

Done - add cloudfront distribution to CFN file and test

Done - Deploy stack via github actions

*Further improvments:

Include s3push as last step of stack deployment

Return cfront and s3 bucket details to github actions console

Potential to add fancier stacks to CFN file - a database and lambda functions triggered by API gateway

Minimize permissions for helloweb IAM user

Create client billing alarm, cost allocation tags

Add region filters and pricing level for Cloudfront