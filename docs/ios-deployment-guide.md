# iOS Deployment Guide
> This guideline is used to show what you need to deploy an App to AppleStore.

---

## Build Preparation

First of all, you will need the following certificates to build an App.

1. [iOS Distribution Certificate](#get-distribution-certificate)
2. [Your own developer certificate](#get-developer-certificate)
3. [App Identifier](#get-app-identifier)
4. [A valid testing devices](#register-testing-devices)
5. [Development Provisioning Profile and Production Provisioning Profile]()
6. Download (1), (2), (4) and open those certifiates and profiles
7. Restart XCode

---

## Get Distribution Certificate

1. Login to [Apple Developer](https://developer.apple.com)
2. Goto [Certificates, Identifiers & Profiles](https://developer.apple.com/account/resources/certificates/list)
3. Click `Certificates` tag
4. Find the `iOS Distribution` and download the certificate

---

## Get Developer Certificate

1. Login to [Apple Developer](https://developer.apple.com)
2. Goto [Certificates, Identifiers & Profiles](https://developer.apple.com/account/resources/certificates/list)
3. Click `Certificates` tag
4. Click `+`
5. ↓ Select `Apple Development` and continue
> ![img](./img/ios-dev-cert-001.jpg)
6. Follow this [instruction](https://help.apple.com/developer-account/#/devbfa00fef7) to generate a `CSR file`
7. ↓ Choose the `CSR file`
> ![img](./img/ios-dev-cert-002.jpg)
8. Download the developer certificate and open it

---

## Get App Identifier

1. Login to [Apple Developer](https://developer.apple.com)
2. Goto [Certificates, Identifiers & Profiles](https://developer.apple.com/account/resources/certificates/list)
3. Click `Identifiers` tag
4. Click `+`
5. ↓ Select `App IDs`
> ![img](./img/ios-app-id-001.jpg)
6. ↓ Complete the form by project requirements
> ![img](./img/ios-app-id-002.jpg)
7. Continue to complete

---

## Register Testing Devices

> `TODO`

---

## Get Provisioning Profiles

For seperating the `DEV` and `PROD` in build stage, we will use different profiles to sign our App.

### Differents Between Development Profile and Production Profile


| Certificate Type         | Build on valid test devices | Build on simulator  | Deploy to TestFlight | Deploy to Store|
| ------------------------ |:---------------------------:|:-------------------:|:--------------------:|:--------------:|
| Development Profile      |              O              |          O          |           X          |        X       |
| Production Profile       |              O              |          O          |           O          |        O       |
