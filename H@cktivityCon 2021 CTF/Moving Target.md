# Another QR looking challenge
![[target_practice.gif]]
The challenge description mentions that the flag is only 24 hexadecimal characters, 
## Solution
Each Frame of the Gif is a different [MaxiCode](https://en.wikipedia.org/wiki/MaxiCode) .  For each frame of the gif, I manually [Decoded](https://products.aspose.app/barcode/recognize/maxicode#/recognized) each Maxicode to see if the frame contained the flag. 
```
lftpxrgwvkvacbuzxlxahwbgixjlgj
ohtqbjogozzngudcnthdryiiqmsacj
syqixjbncbhbtofakbnpmodydssjgd

flag{385e3ae5d7b2ca2510be8ef4}

msywbrkuifxoiipkncgaprqkqwkagb
ylfjdbcwtnwdakudxdocztpnsyhwuy
```
## Rabbit Hole
Prior to receiving a hint [Giant list of Codes](https://www.tamperco.com/barcode-types-2/), I thought the solution was related to the amount of black shapes in each frame. As a result,  I determined which pixels were constant across all frames of the gif and turned the pixels white.
 The next step was to use opencv to detect and count how many black shapes are present in each image which could represent the hex value of an ASCII character.
