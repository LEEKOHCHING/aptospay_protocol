# aptospay_protocol
A standardized Payment QR Code protocol built on the Aptos

**1. Background**
   
Aptos offers a low-cost, high-speed environment without external infrastructure, making it ideal for building payment protocols.
Payment QR Codes are widely accepted globally, with mature user habits and strong compatibility.
Clear use cases include online e-commerce payments and offline QR-based transactions.

**2. Proposal Objectives**
   
To establish a universal Payment QR Code specification that includes:
A standardized format (e.g., transaction amount, target wallet address, memo field, etc.).
Support for multiple payment tokens (e.g. Aptos, Usdc, Gui, etc.).
Extensibility to accommodate future tokens or payment methods.
A standard URL protocol for requesting native Aptos transfers, Aptos Token transfers, and Aptos transactions allows for a better user experience across apps and wallets in the Aptos ecosystem.

**3. Real Case**

With this feature, when users scan the merchant’s QR code using Aptos Mobile Wallet (PETRA), both the transaction amount and the Token type will be automatically populated. This not only significantly reduces the risk of errors caused by manual input or incorrect Token selection but also streamlines the payment process, enhancing user experience and transaction accuracy.

**4. Core Features**
   
QR Code Generation and Parsing Specification

Standardized fields ：
```
recipient: Recipient wallet address.

asset: The contract address of the asset used for payment.

amount: Transaction amount.

memo: Optional memo information.
```

```vb.net
aptos:<recipient>
      ?asset=<asset>
      &amount=<amount>
      &memo=<memo>
```

Examples
```vb.net
URL describing a transfer request for 1 Aptos Usdt.
aptos:0x34c4c18881b4ded6671213339b1148f85bf203db93a2a7ad11cdef0799156083?asset=0x357b0b74bc833e95a115ad22604854d6b0fca151cecd94111770e5d6ffc9dc2b&amount=1&memo=OrderId12345
```


![本地图片](https://github.com/LEEKOHCHING/aptospay_protocol/blob/main/aptospay.png)


**5. Ecosystem Value**
   
Enhance Aptos's competitiveness in the payment sector, attracting more merchants and users.
Strengthen the connection between Aptos and real-world applications, promoting mainstream adoption.
Reduce technical costs for developers and merchants while improving user experience.
