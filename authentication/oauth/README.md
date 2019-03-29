# oAuth In Brief

>The OAuth 2.0 authorization framework enables a third-party
>application to obtain limited access to an HTTP service, either on
>behalf of a resource owner by orchestrating an approval interaction
>between the resource owner and the HTTP service, or by allowing the
>third-party application to obtain access on its own behalf.  This
>specification replaces and obsoletes the OAuth 1.0 protocol described
>in RFC 5849.`
> -- <cite>Specification: https://tools.ietf.org/html/rfc6749</cite>

# Types

There are many different scenarious in which oAuth is used.

## Web Flow
 
* An application redirects users to SERVICE to log in. 

* SERVICE then presents a dialog indicating the name of the app as well as the level of access the app has once it’s authorized by the user. 

* After a user authorizes access, the SERVICE redirects the user back to the application.

# Resources

* https://stormpath.com/blog/what-the-heck-is-oauth

* https://stormpath.com/blog/talking-to-oauth2-services-with-nodejs 

* !!! https://www.oauth.com/

* !!! https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2

* !!! https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_understanding_username_password_oauth_flow.htm

* https://alexbilbie.com/2016/07/updated-grants-guide

* https://oauth.net/articles/authentication/

* Series by hueniverse

> oAuth 1 - https://hueniverse.com/oauth/guide/

> oAuth 2 - https://hueniverse.com/2010/05/15/introducing-oauth-2-0/

* https://hueniverse.com/2012/07/26/oauth-2-0-and-the-road-to-hell/

* https://github.com/oauthjs

> https://github.com/oauthjs/node-oauth2-server

* !!! Series Infosec Institute

> http://resources.infosecinstitute.com/securing-web-apis-the-basics-with-node-js-examples/

> http://resources.infosecinstitute.com/securing-web-apis-part-ii-creating-an-api-authenticated-with-oauth-2-in-node-js/