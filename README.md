# passport-auth

## Authentication Strategies using nodeJS and Passport

### Different Tools/Packages used are

1. Bootstrap for the front-end templating

2. Express as the web-framework

3. MongoDB Atlas for the database.

4. Uses the PUG templating tool.

5. mongoose to process mongoDB queries

6. [passport](https://www.npmjs.com/package/passport) package for authentication

## Basic Usage

A default User account is created and assigned to the session.

The account can be created with the following Strategies

1. Local Account with Email and Password

2. Github Login credentials

3. Facebook Login credentials

4. Google Login credentials

5. Twitter Login credentials

Once an account is created, the user can link the other accounts from the Dashboard.

The user can also Unlink any accounts. The ID, will be saved for reference/re-connection, but token deleted.

### Environment Variables

The project needs these 2 variables to be set in .env

1. PORT- The listening port for NodeJS Server(default:3000)

2. MONGODB_URI - Your MongoDB connection string

3. SESSION_SECRET - Any string to use as your session secret key.

4. LOCAL_HOST - The domain used for connection, used to generate the Callback URL

- Eg: 'https://local.domain.com:3001'

5. For Github credentials

- GITHUB_CLIENT_ID

- GITHUB_CLIENT_SECRET

6. For Facebook credentials

- FACEBOOK_CLIENT_ID

- FACEBOOK_CLIENT_SECRET

7. For Google Credentials

- GOOGLE_CLIENT_ID

- GOOGLE_CLIENT_SECRET

8. For Twitter Credentials

- TWITTER_CLIENT_ID

- TWITTER_CLIENT_SECRET

### Recommendations

Would recommend to use an https URL, especially if using localhost to test Facebook Login.
You will need to generate a self-signed certificate for your domain.
If you need help to create the certificate, follow this link ([https://flaviocopes.com/express-https-self-signed-certificate/](https://flaviocopes.com/express-https-self-signed-certificate/))
For a Windows Client, you can use openssl from GIT to generate the certificate.
Example command for Windows, go to your project folder and type as below

```
C:\passport-auth>& 'C:\Program Files\Git\usr\bin\openssl.exe' req -nodes -new -x509 -keyout server.key -out server.cert
```
