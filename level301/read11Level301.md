# this is read11 from 301
# OAuth:
![img](https://upload.wikimedia.org/wikipedia/commons/d/d2/Oauth_logo.svg)


# What is OAuth? How the open authorization framework works :
OAuth allows websites and services to share assets among users. It is widely accepted, but be aware of its vulnerabilities.

# OAuth definition :
is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.
OAuth was released as an open standard in 2010 as RFC 5849, and quickly became widely adopted. Over the next two years, it underwent substantial revision, and version 2.0 of OAuth, was released in 2012 as RFC 6749. Even though version 2.0 was widely criticized for multiple reasons covered below, it gained even more popularity. Today, you can add Amazon, Facebook, Instagram, LinkedIn, Microsoft, Netflix, Paypal and a list of other internet who’s-whos as adopters.

# OAuth examples :
1. The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.
2. OAuth scenario could be a user sending cloud-stored files to another user via email, when the cloud storage and email systems are otherwise unrelated other than supporting the OAuth framework (e.g., Google Gmail and Microsoft OneDrive). When the end-user attaches the files to their email and browses to select the files to attach, OAuth could be used behind the scenes to allow the email system to seamlessly authenticate and browse to the protected files without requiring a second logon to the file storage system. 

In all cases, two or more services are being used for one transaction by the end-user, and every end-user would appreciate not being asked to log in a second time for what they feel is a single transaction. For OAuth to work, the end-user’s client software (e.g., a browser), the services involved and authentication provider must support the right version of OAuth (1.0 versus 2.0).

# OAuth explained :
OAuth scenarios almost always represent two unrelated sites or services trying to accomplish something on behalf of users or their software. All three have to work together involving multiple approvals for the completed transaction to get authorized.It is also helpful to remember that OAuth is about authorization in particular and not directly about authentication.
Authentication is the process of a user/subject proving its ownership of a presented identity, by providing a password or some other uniquely owned or presented factor. Authorization is the process of letting a subject access resources after a successful authentication, oftentimes somewhere else.

OAuth 2.0 is a framework, not a protocol (like version 1.0). It would be like all the car manufacturers agreeing on how valets would automatically request, receive and use valet keys, and how those valet keys would generally look. What the valet keys could do as compared to the full function keys would be up to each car manufacturer. Just like in real life, valets and car owners don’t need to care about how it all works. They just want it all to work seamlessly as possible when they hand off the key.

# How OAuth works :
assume a user has already signed into one website or service OAuth only works using HTTPS. The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens greatly simplified:
   1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
   2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
   3. The first site gives this token and secret to the initiating user’s client software.
   4. The client’s software presents the request token and secret to their authorization provider which may or may not be the second site.
   5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
   6. The user approves or their software silently approves a particular transaction type at the first website.
   7. The user is given an approved access token notice it’s no longer a request token.
   8. The user gives the approved access token to the first website.
   9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
   10. The second website lets the first website access their site on behalf of the user.
   11. The user sees a successfully completed transaction occurring.
   12. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

   # OAuth vs. OpenID :
   There are a couple of other security technologies that you might hear about in the same context as OAuth, and one of them is OpenID. t a base level, the distinction between the two is simple to grasp.

   * OpenID: means for logging into the then-popular LiveJournal blogging site but quickly spread to other sites. The idea, in the early days of Web 2.0, was that rather than having multiple logins for multiple websites, OpenID would serve as a single sign-in, vouching for the identities of users. But in practice OpenID was difficult to implement on the developer side, and never really became that appealing to users, especially as there was competition in that space.OpenID had become an also-ran, and, Wired declared that "The main reason no one uses OpenID is because Facebook Connect does the same thing and does it better. Everyone knows what Facebook is and it's much easier to understand that Facebook is handling your identity than some vague, unrecognized thing called OpenID."

# OAuth vs. SAML :
The Security Assertion Markup Language, or SAML, is another technology you'll hear talked about in the same breath as OAuth.trictly speaking, the name SAML refers to an XML variant language, but the term can also cover various protocol messages and profiles that make up part of the open SAML standard. 
  *  SAML :describes a framework that allows one computer to perform both authentication and authorization on behalf of one or more other computers, unlike OAuth, which requires an additional layer like OpenID Connect to perform authentication. SAML can provide single sign-on functionality on its own.

# OAuth2 :
OAuth2 is less secure, more complex and less prescriptive than version 1.0. Version 2.0 creators focused on making OAuth more interoperable and flexible between sites and devices. They also introduced the concept of token expiration, which did not exist in version 1.0. Regardless of the intent, many of the original founders and supporters threw up their hands and did not support version 2.0.The changes are so significant that version 2.0 is not compatible with version 1.0, and even different implementations of version 2.0 may not work seamlessly with each other. However, nothing prevents a website from supporting both 1.0 and 2.0, although the 2.0 creators released it with the intent of all websites completely replacing version 1.0.
One of the biggest criticisms of OAuth 2.0 is that the standard intentionally does not directly define or support encryption, signature, client verification or channel binding (tying a particular session or transaction to a particular client and server). Instead, OAuth expects implementers to use an outside protection protocol like Transport Layer Security (TLS), to provide those features.

# Is OAuth safe?
Because of the lack of inherent security binding, it’s possible for a rogue website to phish a user’s legitimate credentials during the part of the process where the user is being required to authenticate themselves to the authorization provider. such as a user is using the first service and chooses a feature that forces an OAuth transaction to a second service. It’s possible for the first website to fake the second website, where user authentication is often taking place. The rogue website can then collect the user’s authentication credentials and react as if the OAuth transaction had successfully taken place.This is not just a theoretical threat. 

# Authentication and Authorization Flows :
Auth0 uses the OpenID Connect (OIDC) Protocol and OAuth 2.0 Authorization Framework to authenticate users and get their authorization to access protected resources. With Auth0, you can easily support different flows in your own applications and APIs without worrying about OIDC/OAuth 2.0 specifications or other technical aspects of authentication and authorization.
 1. Authorization Code Flow:Because regular web apps are server-side apps where the source code is not publicly exposed, they can use the Authorization Code Flow, which exchanges an Authorization Code for a token.
 2. Authorization Code Flow with Proof Key for Code Exchange (PKCE): During authentication, mobile and native applications can use the Authorization Code Flow, but they require additional security. Additionally, single-page apps have special challenges. To mitigate these, OAuth 2.0 provides a version of the Authorization Code Flow which makes use of a Proof Key for Code Exchange (PKCE).
 3. Implicit Flow with Form Post :As an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets. While this is no longer considered a best practice for requesting Access Tokens, when used with Form Post response mode, it does offer a streamlined workflow if the application needs only an ID token to perform user authentication.
 
 # Hybrid Flow :
 Applications that are able to securely store Client Secrets may benefit from the use of the Hybrid Flow, which combines features of the Authorization Code Flow and Implicit Flow with Form Post to allow your application to have immediate access to an ID token while still providing for secure and safe retrieval of access and refresh tokens. This can be useful in situations where your application needs to immediately access information about the user, but must perform some processing before gaining access to protected resources for an extended period of time.

 # Client Credentials Flow :
 With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user. For this scenario, typical authentication schemes like username + password or social logins don't make sense. Instead, M2M apps use the Client Credentials Flow.

 # Device Authorization Flow :
 With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. This avoids a poor user experience for devices that do not have an easy way to enter text. To do this, device apps use the Device Authorization Flow ,for use with mobile/native applications.

 # Resource Owner Password Flow :
 Though we do not recommend it, highly-trusted applications can use the Resource Owner Password Flow, which requests that users provide credentials (username and password), typically using an interactive form. The Resource Owner Password Flow should only be used when redirect-based flows like the Authorization Code Flow cannot be used.



   













