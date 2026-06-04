# Obfuscation

Obfuscation is the concept of hiding information in plain sight by making it seem unclear. If you do not even realize what you are looking at, you will have no way of knowing information. If you know the obfuscation process, you can reverse engineer it (or just observe) and find the wanted information.

## Steganography

This is a common method where you store some form of information in anm image. It comes from the greek term "concealed writing". Often time, many images or accessible things will have some data put into them that can not just be seen or accessed from basic view. Often times, the cover image is called the covertext.

## Steganography exists beyond images

Network based exists too. Embeded messages in TCP packets for example.

Just as image exists, video steganography exists and is a larger scale of image. It is essential a sequence of images.

Audio steganography exists too, where secret messages can be interlaced in the audio data.

## Tokenization

A common method of obfuscation used everyday is **tokens**. Sensitive data is replaced with a non-sensitive placeholder. Behind the scenes, people aware of this data know to match the token to the real data. However, if anyone gets their hand on this token without knowing the real data, they would have no use for it.

This is how credit card processing works. A temporary (one time use) token is sent from you credit card across the network and authorized. 

Because the token is not directly linked to any data, it does not need to be encrypted or hashed.

