# OAuth2.0 and OpenID Connect

## OAuth2.0
Is used to obtain an `access token` which can be used to access a resource (often data about the user or access to an API). There are 4 ways to obtain an access token (called flows in OAuth terminology) but here only 2 will be mentioned. They are:

1. Authorization Code Flow  
  In this flow we first obtain a auth code which is then exchanged for a `access token`. We also get a `refresh token` which can be used to to renew the `access token` after it has expired.
2. Implicit Flow  
  In this flow we obtain the `access token` directly but we do NOT get a `refresh token` and hence has to go through the entire flow (including user auth) again when the token expires.

### Authorization Code Flow
![Authorization Code Flow](https://cdn-images-1.medium.com/max/800/1*ULF38OTiNJNQZ4lHQZqRwQ.png)
### Implicit Flow
![Implicit Flow](https://cdn-images-1.medium.com/max/800/1*_7h6INaOWSvRVzDKK5x9Zw.png)

## OpenID Connect
Builds on top of OAuth2.0 and add an extra field to the response (the `id_token`) which is a [JSON Web Token](https://jwt.io/) (JWT). This JWT contains extra information about the user not included in OAuth2.0.

### OpenID Connect and OAuth Learning Resources

1. [https://medium.com/@darutk/the-simplest-guide-to-oauth-2-0-8c71bd9a15bb](https://bitbucket.itgit.oneadr.net/projects/RBAN/repos/wonderbox/null)
2. [https://medium.com/@darutk/diagrams-and-movies-of-all-the-oauth-2-0-flows-194f3c3ade85](https://bitbucket.itgit.oneadr.net/projects/RBAN/repos/wonderbox/null)