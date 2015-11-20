## Authentication

### Auth-Overview
The first thing to do in order to use the MaxCDN REST Web Service (RWS) is to register your application. Upon registration, your application will be issued a consumer key and secret which is similar to public and private keys used in ssh protocol. You will need to use this in conjunction with an OAuth library in the programming language of your choice.

<blockquote><p>OAuth defines three roles: client, server, and resource owner (nicknamed the OAuth Love Triangle by Leah Culver).</p></blockquote>

The MaxCDN RWS supports both 2-legged and 3-legged authentication.

3-legged OAuth is best used to allow 3rd party apps/services (e.g. [Leftronic](https://www.leftronic.com/services/maxcdn/)) access to a user's profile - the user just needs to grant access to the app.

2-legged OAuth is more limited in that it only allows a consumer access to resources that belong to it, which can be useful for building a 3rd party app, a control panel where the consumer is a reseller, or an account with sub-accounts (this means the reseller/main account also has access to sub-account resources). This does not require any user intervention in the process.

### 3-legged OAuth
3-legged OAuth describes the scenario for which OAuth was originally developed: a resource owner wants to give a client access to a server without sharing their credentials (i.e. username/password).
On a conceptual level it works in the following way:

* Client has signed up to the server and received their client credentials (also known as "consumer key and secret") ahead of time
* User wants to give the client access to their protected resources on the server
* Client retrieves the temporary credentials (also known as "request token") from the server
* Client redirects the resource owner to the server
* Resource owner grants the client access to their protected resources on the server
* Server redirects the user back to the client
* Client uses the temporary credentials to retrieve the token credentials (also known as "access token") from the server
* Client uses the token credentials to access the protected resources on the server

### 2-legged OAuth
2-legged OAuth describes a typical client-server scenario, without any user involvement. On a conceptual level 2-legged OAuth simply consists of the first and last steps of 3-legged OAuth:

* Client has signed up to the server and received their client credentials (also known as "consumer key and secret")
* Client uses their client credentials (and empty token credentials) to access the protected resources on the server

### Registering Your Application
Login and go to <https://cp.maxcdn.com/account/api/create>

### Signing Requests
All OAuth 1.0a requests use the same basic algorithm for creating a signature base string and a signature.

### Request Tokens
The first step to authenticating a user is to obtain a request token from MaxCDN.

The end point for requesting a token is: `https://rws.maxcdn.com/oauth/request_token`

### User Authorization
The User Authorization step sends the user to the MaxCDN RWS authorization page, which grants your application privileges to use their account with the API. You will need the oauth_token from the previous step to complete this.

The endpoint for the authorization url is: `https://rws.maxcdn.com/oauth/authorize`


### Key: Path Parameters

Parameter | Description |
--- | ---
`{companyalias}` | The alias used when creating the account |
`{zone_type}` | The type of zone you are making a request on — one of `pull`, `push`, or `vod` |
`{report_type}` | The format you want the reports summarized by — `hourly`, `daily`, or `monthly`. This value can be left blank to receive ungrouped totals |
