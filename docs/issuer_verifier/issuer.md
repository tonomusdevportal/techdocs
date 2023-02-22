# tel-veramo-websites
Code repo link - https://github.com/NEOM-KSA/tel-veramo-websites
This repository contains the issuer and verifier websites.

## Issuer Website
### Run the website
1. Move to the directory after cloning the repository
```
cd issuer
```
2. Install dependencies
```
yarn install
```
3. Create .env file with the following fields.
```
PORT=
ISSUER_URL=
ISSUER_DID=
USER_DID=

OCI_URL=

CLIENT_ID=
CLIENT_SECRET=
CLIENT_SIGNING_KEY=
ISS_AUD=

```
4. Start the website
```
yarn start
```
### Issuance flow
1. User gets prompted with options of which Credential type to be issued (only Travel Pass for now)
2. A **form** with the respective claims required is shown for the user to fill, followed by the Submit button press
3. **QR Code** to be scanned (coming from Gateway) by the user from the Wallet App > Scanner feature
4. Spinner is shown on the website letting user know to complete the flow in their wallet
5. Once user has finished the flow on the wallet, website redirects to confirm flow

## Verifier Website
### Run the website
1. Move to the directory after cloning the repository
```
cd verifier
```
2. Install dependencies
```
yarn install
```
3. Start the website
```
yarn start
```
### Verifier flow
1. User gets prompted with options of which Credential type to present (only Travel Pass for now)
2. **QR Code** to be scanned (coming from Gateway) by the user from the Wallet App > Scanner feature
4. Spinner is shown on the website letting user know to complete the flow in their wallet
5. Once user has finished the flow on the wallet, website redirects to confirm flow


## References 
For creating the JWT tokens, example in the case of OIDC Authcode flow,
we need to create an Identity Token in the issuance flow. jsonwebtoken library is used for this purpose.
For any further details of this library , please refer the following link https://www.npmjs.com/package/jsonwebtoken.

For details of the Issuance and verification flows, please refer the following link- 
https://neom.atlassian.net/wiki/spaces/TEL/pages/1217232973/Gateway+Integration+with+custom+provider+Veramo

For details of the payload inside the Issuance flow, please refere the following link - https://neom.atlassian.net/wiki/spaces/TEL/pages/1224343638/Gateway+Issuer+Veramo+integration+with+OIDC+ID+token+hint
