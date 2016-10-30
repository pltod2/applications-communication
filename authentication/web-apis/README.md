# Authenticating Web APIs

How Web APIs Could Communicate with Other Servers Securely

* Keys

> http://weblogs.asp.net/cibrax/authentication-in-web-apis-keys-oauth-or-hmac


* Tokens via Cookies

> in the case of hapi example plugin is https://github.com/hapijs/hapi-auth-cookie

* Tokens via JWT

> http://self-issued.info/docs/draft-ietf-oauth-json-web-token.html

> http://jwt.io/

> http://www.sitepoint.com/using-json-web-tokens-node-js/

> http://angular-tips.com/blog/2014/05/json-web-tokens-introduction/
 
> https://developer.atlassian.com/static/connect/docs/concepts/understanding-jwt.html

* Tokens via oAuth and oAuth2 (as far as I know token based)

oAuth is related with API authorisation but seems it can be used for login local client as well. 
There are nice discussions on the oAuth and beyond here:

> http://stackoverflow.com/questions/14402938/2-legged-auth-standards-in-2013-should-we-use-oauth2

> http://www.thebuzzmedia.com/designing-a-secure-rest-api-without-oauth-authentication/

> http://apiux.com/2013/07/10/oauth-2-trumps-basic-authentication/


* Tokens via HMAC (The former oAuth lead has some custom types of authorizations (which seems to be HMAC implementations?))

> https://github.com/hueniverse/oz

> https://github.com/hueniverse/hawk

> http://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html

