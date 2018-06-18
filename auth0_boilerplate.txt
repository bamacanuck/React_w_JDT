import auth0 from 'auth0-js';

export default class Auth {
  auth0 = new auth0.WebAuth({
    domain: 'shaneradio.auth0.com',
    clientID: 'UrkJK7eZlnfC19Z5c3oWZtquyi25oqBV',
    redirectUri: 'http://localhost:3000/callback',
    audience: 'https://shaneradio.auth0.com/userinfo',
    responseType: 'token id_token',
    scope: 'openid'
  });

  login() {
    this.auth0.authorize();
  }
}