---
title: Sign in with passkeys in Authenticator for Android and iOS devices (preview)
description: Learn how to sign in with passkeys for Android and iOS devices with Microsoft Authenticator (preview.

services: active-directory
ms.service: entra-id 
ms.subservice: authentication
ms.topic: how-to
ms.date: 04/18/2024

ms.author: justinha
author: justinha
manager: amycolannino
ms.reviewer: mayurs, calui

ms.collection: M365-identity-device-management
---
# Sign in with passkeys in Authenticator for Android and iOS devices (preview)

This article covers the sign-in experience when using passkeys in Microsoft Authenticator with Microsoft Entra ID. For more information on the availability of Microsoft Entra ID passkey (FIDO2) authentication across native apps, web browsers, and operating systems, see [Support for FIDO2 authentication with Microsoft Entra ID](concept-fido2-compatibility.md).

[!INCLUDE [Passkey roll out](~/includes/entra-authentication-passkey.md)]

## [**iOS**](#tab/iOS)

To sign in with a passkey in Microsoft Authenticator, your iOS device needs to run iOS 17 or later.

### Same-device authentication (iOS)

Follow these steps to sign in to Microsoft Entra ID with a passkey in Microsoft Authenticator on your iOS device. 

1. On your iOS device, open your browser and navigate to the resource you're trying to access at [My Security info](https://aka.ms/mysecurityinfo).

1. You can enter your username to sign in: 

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-user-name.png" alt-text="Screenshot of the sign-in with username in Microsoft Authenticator for iOS devices.":::

   Or click **Sign-in options** to sign in more conveniently without having to enter a username. 

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-microsoft.png" alt-text="Screenshot of the sign-in Microsoft in Microsoft Authenticator for iOS devices.":::

   If you chose **Sign-in options**, select **Face**, **Fingerprint**, **PIN**, or **Security key**. Otherwise, skip to next step.

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-options.png" alt-text="Screenshot of the sign-in options in Microsoft Authenticator for iOS devices.":::

   > [!NOTE]
   > If you signed in without a username and multiple passkeys are saved to your device, you're prompted to choose which passkey to use for sign-in. 

1. To select your passkey, follow the steps in the iOS operating system dialog. Verify that it's you by using Face ID, Touch ID, or entering your device PIN.

1. You're now signed into Microsoft Entra ID.

### Cross-device authentication (iOS)

Follow these steps to sign in to Microsoft Entra ID on another device with a passkey in Microsoft Authenticator on your iOS device.

1. On the other device where you're looking to sign in to Microsoft Entra ID, open your browser and go to `login.microsoftonline.com`.

1. Select **Sign-in options**. 

    :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-microsoft.png" alt-text="Screenshot of the sign-in Microsoft in Microsoft Authenticator for iOS devices.":::

1. Select **Face**, **Fingerprint**, **PIN**, or **Security key**.

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-options.png" alt-text="Screenshot of the sign-in options in Microsoft Authenticator for iOS devices.":::

1. To begin cross-device authentication, follow the steps in the operating system or browser prompt. On Windows 11 23H2 or later, select **iPhone, iPad, or Android device**.

1. A QR code should be shown on screen. Now, on your iOS device, open the Camera app and scan the QR code. Select **Sign-in with passkey** when the option appears.

   > [!NOTE]
   > Bluetooth is required for this step and must be enabled on both your mobile and remote device.

1. To select your passkey, follow the steps in the iOS operating system dialog. Verify that it's you by using Face ID, Touch ID, or entering your device PIN.

1. You're now signed into Microsoft Entra ID on your other device.

### Single-sign on to native Microsoft applications (iOS)

You can use Authenticator on your iOS device to seamlessly sign in with a passkey to other Microsoft apps, such as Microsoft OneDrive, SharePoint, and Outlook. Similar support for Android devices is coming during preview. 

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-ios/sign-in-options-passkey.png" alt-text="Screenshot of the passkey option in Microsoft Authenticator for iOS devices.":::

To use SSO for native applications, you need to register the passkey in Authenticator by using the WebAuthN flow where you scan a QR code: 

1. Register Authenticator passkey on your mobile device. 
1. Sign in to Authenticator. 
1. Setup passkey on you iOS device using the available QR code.
1. Open a Microsoft app, such as Outlook, using the username you created the passkey for.
1. Now you can access other Microsoft apps on your device, and you'll be automatically authenticated. 


## [**Android**](#tab/Android)

To sign in with a passkey in Microsoft Authenticator, your Android device needs to run Android 14 or later.

[!INCLUDE [Need APIs to support browsers](~/includes/passkeys-with-chrome-browser.md)]

<!---Support for browser scenarios aren't yet supported 
### Same-device authentication (Android)

Follow these steps to sign in to Microsoft Entra ID with a passkey in Microsoft Authenticator on your Android device.

1. On your Android device, open your browser and navigate to the resource you're trying to access at [My Security info](https://aka.ms/mysecurityinfo).

1. When prompted to sign in, you have two options. The *usernameless* option can be easier than entering your username.

   1. Type your username. 

       :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-android/sign-in-user-name.png" alt-text="Screenshot of the sign-in with username in Microsoft Authenticator for Android devices.":::

   1. To sign in with the *usernameless* option, select **Sign-in options**. 

       :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-android/sign-in-microsoft.png" alt-text="Screenshot of the sign-in Microsoft in Microsoft Authenticator for Android devices.":::

   1. If you chose **Sign-in options**, select **Face**, **Fingerprint**, **PIN**, or **Security key**. Otherwise, skip to next step.

      :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-android/sign-in-options.png" alt-text="Screenshot of the sign-in options in Microsoft Authenticator for Android devices.":::

    > [!NOTE]
    > If you have more than one passkey saved to your device, you're prompted to choose a passkey. 

1. To select your passkey, follow the steps in the Android operating system dialog. Verify that it's you by scanning your face, fingerprint, or entering your device PIN or unlock gesture.

1. You're now signed into Microsoft Entra ID.
--->

### Cross-device authentication (Android)

Follow these steps to sign in to Microsoft Entra ID on another device with a passkey in Microsoft Authenticator on your Android device.

1. On the other device where you're looking to sign in to Microsoft Entra ID, open your browser and go to [My Security info](https://aka.ms/mysecurityinfo).

1. Select **Sign-in options**. 

    :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-android/sign-in-microsoft.png" alt-text="Screenshot of the sign-in Microsoft in Microsoft Authenticator for Android devices.":::

1. Select **Face**, **Fingerprint**, **PIN**, or **Security key**.

   :::image type="content" border="true" source="media/howto-authenticate-passwordless-passkey-direct-android/sign-in-options.png" alt-text="Screenshot of the sign-in options in Microsoft Authenticator for Android devices.":::

1. To initiate cross-device authentication, follow the steps in the operating system or browser prompt. On Windows 11 23H2 or later, select **iPhone, iPad, or Android device**.

1. A QR code should be shown on screen. Now, on your Android device, open the Camera app and scan the QR code. Select **Sign-in with passkey** when the option appears.

> [!NOTE]
> Bluetooth is required for this step and must be enabled on both your mobile and remote device.

1. To select your passkey, follow the steps in the Android operating system dialog. Verify that it's you by scanning your face, fingerprint, or entering your device PIN or unlock gesture.

1. You're now signed into Microsoft Entra ID on your other device.

---
