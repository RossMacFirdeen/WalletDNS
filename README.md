
**This document is a working version**

## Cryptographic Wallet DNS based naming convention

The purpose of this document is to propose a new naming approach for cryptographic portfolios whose addresses are most often complex to memorize.

The proposed approach consists of the use of DNS records ( **TXT** record type), to allow the identification of a portfolio *regardless of the type of cryptographic token used* and various optional elements such as protocol or destination tags in the case of XRP .

**Attention point :** Tokens are referenced by their designation according to **ISO 4217**

The structuring of TXT records would be as follow :

**[attribute]. [ISO4217Code]. [protocol]. [[optionalSubdomain.]domain.tld]**

The protocol part is mandatory and linked to each coin to be represented ( eq : for the XRP asset , the corresponding protocol is RTXP)

Below, the accepted values for the attribute part :

 - **address** : Indicates that the value of the TXT record is representing the wallet address
 - **dt**:   Indicates that the value of the TXT record is representing the destination tag (this attribute is facultative)

## Example #1 (with domain contoso.com)

 - XRP Wallet address : rKCSiPJhLDgK24RFpbxJ3bVCqW78EHBZD 
 - Destination tag : 4258
 - Domain : contoso.com

**TXT Record #1 :**
address.xrp.rtxp.contoso.com = rKCSiPJhLDgK24RFpbxJ3bVCqW78EHBZD

**TXT Record #2 :**
dt.xrp.rtxp.contoso.com = 4258

## Example #2 (with the sub-domain mywallets.contoso.com)

 - XRP Wallet address : rP6LSvd6H2fzcqtJhmtDhR33ozH5VFmW8e
 - Destination tag : 75846
 - Domain : mywallets.contoso.com

**TXT Record #1 :**
address.xrp.rtxp.mywallets.contoso.com = rP6LSvd6H2fzcqtJhmtDhR33ozH5VFmW8e

**TXT Record #2 :**
dt.xrp.rtxp.mywallets.contoso.com = 75846

