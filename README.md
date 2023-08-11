# apple-login-via-capacitor
Apple Login using Capacitor

Sign-in with apple is a feature where you can use apple login ID to sign in any application directly without giving password
Cases:

If you have register with phone only on your Ios device
If you have register with phone and email both on your Ios device

using capacitor :

npm i @capacitor-community/apple-sign-in
npx cap update

In your Login Page 
import {
  SignInWithApple,
  SignInWithAppleResponse,
  SignInWithAppleOptions,
} from '@capacitor-community/apple-sign-in';

const data = {
redirectURI: Vue.config.ATLANTIS_URL + "/auth/callback",
              clientId: 'com.gooogle.android.kuvera.app',
              scopes: 'email name',
              state : "initial",
              nonce: 'nonce',
}
we have to send this 5 value to authenticate


SignInWithApple.authorize(options)
  .then((result: SignInWithAppleResponse) => {
    // Handle user information
    // Validate token with server and create new session
  })
  .catch(error => {
    // Handle error
  });


