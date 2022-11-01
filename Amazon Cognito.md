## Test Unauth Creds Grant

### Get IdentityID

POST / HTTP/2
Host: cognito-identity.eu-west-1.amazonaws.com
Content-Length: 67
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.5304.63 Safari/537.36
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityService.GetId
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Sec-Ch-Ua-Platform: "Windows"
Accept: */*
Origin: https://www.
Referer: https://www.
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9

{"IdentityPoolId":""}

### Exchange IdentityId for AWS keys

POST / HTTP/2
Host: cognito-identity.eu-west-1.amazonaws.com
Content-Length: 63
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.5304.63 Safari/537.36
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityService.GetCredentialsForIdentity
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Sec-Ch-Ua-Platform: "Windows"
Accept: */*
Origin: https://www.
Referer: https://www.
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9

{"IdentityId":""}

### Exchange JWT for AWS keys

POST / HTTP/2
Host: cognito-identity.eu-west-1.amazonaws.com
Content-Length: 63
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.5304.63 Safari/537.36
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityService.GetCredentialsForIdentity
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Sec-Ch-Ua-Platform: "Windows"
Accept: */*
Origin: https://www.
Referer: https://www.
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9

{"Logins":{"cognito-identity.eu-west-1.amazonaws.com/eu-west-1_PoolID":"JWT token"},"IdentityId":""}

## Test SignUp

### register
POST / HTTP/2
Host: cognito-idp.eu-west-1.amazonaws.com
Referer: https://www.
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityProviderService.SignUp
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Origin: https://www.
Content-Length: 36

{"ClientId":"","Username":"","Password":"","UserAttributes":[{"Name":"email","Value":""},{"Name":"name","Value":""}]}

### confirmation

POST / HTTP/2
Host: cognito-idp.eu-west-1.amazonaws.com
Referer: https://www.
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityProviderService.ConfirmSignUp
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Origin: https://www.
Content-Length: 36

{"ClientId":"","Username":"","ConfirmationCode":""}

### Login

POST / HTTP/2
Host: cognito-idp.eu-west-1.amazonaws.com
Referer: https://www.
Content-Type: application/x-amz-json-1.1
X-Amz-Target: AWSCognitoIdentityProviderService.InitiateAuth
X-Amz-User-Agent: aws-sdk-js/3.6.1 os/Windows/NT_10.0 lang/js md/browser/Chrome_107.0.5304.63 api/cognito_identity/3.6.1 aws-amplify/4.6.0_js
Origin: https://www.
Content-Length: 204

{
   "AuthParameters" : {
      "USERNAME" : "",
      "PASSWORD" : ""
   },
   "AuthFlow" : "USER_PASSWORD_AUTH",
   "ClientId" : ""
}

