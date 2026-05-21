- The process of making something unclear
- Hide some of the original data with data masking
- But it´s not impossible to understand
- Hide information in plain sight
- Hide information inside of an image
  - Steganography

## Stenography
- Concealed writinig
  - Security through obscurity
- If you know how it was hidden, you can recover it
- Message is Invisible, while still being present
- The covertext - The container document or file

## Common steganography Techiques
## Network based
  - Embed messages in TCP packets
## Use an image
  - Embed the message in the image itself
## Invisible watermarks
  Yellow dots on printers

 ## Audio Steganography
  - Modify the digital audio file
  - Interlace a secret message within the audio
  - similiar technique to image steganography

## Video Steganography
- A sequence of images
- USe iamge steganography on a larger scale
- Manage the signal to noise ratio
- Potientally transfer much more finromation.

## Tokenization
- Replace sensitive data with a non-sensitive placeholder
- Common with credit card processing
  - Use a temporary token during payment
  - An attacker capturing the card numbers, cannot use them later
- This is not encryption or hashing
1. The original data and token are not matehamtically related
2. The mobile phone registers a credit card, by the user.
3. The card is registered with the token service server
4. Token service server provides a token instead
5. Phone is used at a store during checkout using NFC
6. The token is used for the purchase
7. The Merchant Payment processing server sends the token to the token server, which validates the token sent.

