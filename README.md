Virtual Boltcard
The Virtual Boltcard app leverages Android Host Card Emulation (HCE) to emulate Boltcards, specifically focusing on the POS communication aspect. However, please note that configuring Boltcards using NFC is not supported.

How It Works
Authentication: When you launch the app, you’ll need to authenticate using either your fingerprint or device PIN. This step is essential because once the app starts, you gain access to an LNbits wallet. Additionally, you can switch between active cards.
Starting Without Configured Cards:
Option 1: Create an LNbits Account:
This choice sets up an account, a Boltcard, and an LNURLp link on the specified LNbits server.
You can customize the server URL, name, and limits, or simply use the defaults (currently set to legend.lnbits.com).
The app securely stores your API key and monitors your account balance.
A QR code for the payment link is displayed. Tapping it opens an installed wallet capable of handling LNURLp.
Note: Card export functionality is not available yet, so when setting up a new LNBits card, remember to back up your wallet as usual.
Option 2: Import an Existing Boltcard:
You can import an existing Boltcard from an LNbits wallet using either a QR code or a URL.
Option 3: Manual Setup of an Existing Boltcard.
Multiple Cards:
You can configure multiple cards (accessed via the “+” bubble in the lower-right corner of the screen).
The active card always corresponds to the visual card. Swipe to activate a different card.
Emulation and NFC:
Currently, there is no way to disable emulation. To do so, you’ll need to deactivate NFC.
Emulation even works from the lock screen, although we’re still evaluating whether this is advantageous or problematic.
Security Considerations
Data Storage:
The app securely stores your Boltcard URL, keys, and counter in encrypted settings storage and an encrypted MSSQL database.
The initial password is randomly generated during the first launch and saved securely.
Access to Sats:
Anyone with access to this data can potentially access your satoshis (sats).
LNbits Wallet Creation:
If you create an LNbits wallet within the app, the API keys are also securely saved in the encrypted MSSQL database.
Safety Disclaimer:
While I’ve made efforts to enhance security, I am not an experienced app developer. If you identify any issues, please report them so we can address them promptly.
Boltcard Security:
A Boltcard is an offline device that stores card URLs, keys, and counters. By directly placing this data on your phone, you compromise security.
References
NFCAndroid Repository
Boltcard Repository
Boltcard Official Website
