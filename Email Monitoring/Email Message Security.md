Secure/Multipurpose Internet Mail Extensions (S/MIME) - An email encryption standard that adds digital signatures and public key cryptography to traditional MIME communications

A user is issued a digital certificate containing his or her public key in order to use S/MIME

1. Jason sends Mary his digital certificate, containing his public key and validated digital ID (distinguished subject name and email address), and signs this message using his private key.
2. Mary uses the public key in the certificate to decode his signature and the signature of the CA (or chain of CAs) validating his digital certificate and digital ID and decides that she can trust Jason's email address
3. Mary responds with her digital certificate and public key and Jason, following the same process, decides to trust Mary
4. Both Jason and Mary now have each other's certificates in their trusted certificate stores

Encrypting the message with the receiver's public key ensures confidentiality, whereas encrypting a hash of your message with your private key ensures integrity and nonrepudiation

The email client will determine if the digital signature is valid and will then display an icon

