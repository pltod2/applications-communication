# oAuth

* token based with generated token that can be revoked and allows checking what data could be read with it

* acounts with two factor authentication needs oAuth authorization

## Create via Web Flow
 
> Normally, tokens are created via a web flow. 
> An application sends users to GitHub to log in. 
> GitHub then presents a dialog indicating the name of the app, 
> as well as the level of access the app has once it’s authorized by the user. 
> After a user authorizes access, GitHub redirects the user back to the application.


### Access Token for CLI

* Generate this token in your github account settings and use it with curl

### Access Token for App

* Register application in your github account settings

> First, you’ll need to register your application. 
> Every registered OAuth application is assigned a unique Client ID and Client Secret. 
> The Client Secret should not be shared! 
> That includes checking the string into your repository.
> You can fill out every piece of information however you like, 
> except the Authorization callback URL. 
> This is easily the most important piece to setting up your application. 
> It’s the callback URL that GitHub returns the user to after successful authentication.

