## Description 
```
## Hexible

### 100

Decode this string!
``47%50%53%43%54%46%7b%30%65%32%38%33%64%64%37%64%63%37%63%31%64%38%62%39%66%37%38%65%61%31%36%62%30%32%62%32%30%38%33%7d``
```

## Problem
  The provided  string looks like a url encoded with the %'s in the string.' I used Cyberchef to explore common encoding schemes.
  
  ![Hexible Flag](images/Hexible%20Flag%201.png)
  
GPSCTF{0e283dd7dc7c1d8b9f78ea16b02b2083}


## Description 
```
## Baseic

### 200

Decode this string!

`4YX1Cb6Q7vDq5bt3SiYsnCFq4Sp5bBbkYTdiFgtyCUkGhPeM5pVJy4g`
```

## Problem
The challenge name suggest that it could be a combination of several  encodings applied to the same string several times. The string appears to use an alphabet of a-zA-Z0-9. Using the cyberchef magic function, it determined that it was base58.

![Baseic-Flag 1.png](images/Baseic-Flag%201.png)

# Description 
```
## Encoding Challenge

### 400

Someone did some real work to this string. See what you can do with it!

```
Payload =
```
    90kMOdWSU50ZFpXTnlEROdWUU50ZFRlTnVkeNdWSU50ZjRkTn1kMOdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnFkaNdWQq10ZBpWTnlkeNdWV610ZBpWTnVkeNdWT610ZBpWTnlkeNdWU610ZBpWTnFleNdWV610ZBpWTnVkeNdWV610ZBpWTnVkeNdWT610ZBpWTnlkeNdWV610ZBpWTnNmeNdWU610ZBpWTnFkaNdWQ610ZNpXTnFkeNdWQ610ZBpXTnFkeNdWQ610ZBpXTnV0RNdWTy40ZVpmTnVkMOdWUq50ZF1mTnV1ROdWUU50ZNpmTnFleNdWUH50ZJpXTnlFROdWUt50ZrRlTnNGVOd2aE50ZFpXTn1kMOdWQq10ZBpWTnVleNdWW610ZBpWTnVkaOd2Y610ZBpWTnFleNdWW610ZBpWTnVkaOdWW610ZBpWTnVlaOdWU610ZBpWTnFleNdWV610ZBpWTn1keNdWW610ZBpWTnFleNdWT610ZBpWTnFlaOdWU610ZBpWTnlkeNdWT610ZBpWTnlleNdWU610ZBpWTnFlaOdWW610ZBpWTntmeNdWV610ZBpWTnNmeNdWV610ZBpWTntmeNdWU610ZBpWTnVkeNdWT610ZBpWTnFkaNdWQ610ZJpXTnFkeNdWQ610ZBpXTnFkeNdWQ610ZBpXTnV0RNdWTy40ZRdkTnFFVOd2Yq50ZBpXTnV0VOdWUU50ZjpmTndmeOdWRX50ZRRkTnVEVOdWV610ZZdkTnNGROdWRU50ZFJjTn1kMOdWQq10ZBpWTnFlaOdWU610ZBpWTnFleNdWV610ZBpWTnNmeNdWW610ZBpWTnFkeNdWT610ZBpWTnVkaOdWV610ZBpWTnFleNdWV610ZBpWTnNmeNdWW610ZBpWTndmeNd2Y610ZBpWTnVkaOdWV610ZBpWTnFleNdWU610ZBpWTnVkeNdWV610ZBpWTnVleNdWT610ZBpWTnllaOdWU610ZBpWTnNmeNdWU610ZBpWTnVkeNdWV610ZBpWTnVkaOd2Y610ZBpWTnFkaNdWQ610ZFpXTnFkeNdWQ610ZBpXTnFkeNdWQ610ZBpXTnV0RNdWTy40ZZdkTnFFROdWSt50ZnpnTnl1ROd2YU50ZFRlTndmeOdWWH50ZjRkTnVFROd2Z650ZZpmTnVEVOdWUy00ZRJTTn1kMOdWQq10ZBpWTnllaOdWU610ZBpWTnFleNdWU610ZBpWTnlkaOdWW610ZBpWTndmeNd2Y610ZBpWTnllaOdWU610ZBpWTnNmeNdWV610ZBpWTnVkeNdWV610ZBpWTndmeNd2Y610ZBpWTnllaOdWU610ZBpWTnNmeNdWU610ZBpWTnVleNdWU610ZBpWTndmeNd2Y610ZBpWTnlleNdWW610ZBpWTnVkeNdWV610ZBpWTnFlaOdWT610ZBpWTnFlaOdWT610ZBpWTnFkaNdWQ610ZBpXTnFkeNdWQ610ZBpXTnFkeNdWQ610ZBpXT
```
# Problem
I didn't solve this challenge! 

The nature of this payload suggests that there is some repetition of the key or the flag is repeated in order to pad the length of the message.
In the begining there is this repeating string `q10ZBpWTnFkaNdWQ` repeated 8 times.
`610ZBpWTn` could be a special character or delimiter of some kind?


# Shark Fail
## Description 
    ## Shark Fail

### 400

A very interesting Capture! [https://drive.google.com/file/d/16-Vd5K7SjhhJ3KsRPnx_ggz4JLnjuTTh/view?usp=sharing](https://drive.google.com/file/d/16-Vd5K7SjhhJ3KsRPnx_ggz4JLnjuTTh/view?usp=sharing)

We are given a pcap file.

## Attack
Wireshark is only detecting Frames for USB traffic (SCSI) on this pcap. Perhaps the flag.txt was transferred between two devices.
[USB reference](https://www.wireshark.org/docs/dfref/u/usbms.html)
The BULK_IN/OUT are the transfer commands [Microsoft article on it](https://docs.microsoft.com/en-us/windows-hardware/drivers/usbcon/usb-bulk-and-interrupt-transfer)

device 1.6.1 has the largest conversation with the host machine.
Seems to contain an alphabet in some of the packets.
```
----
# Packet 42 from /tmp/mozilla/sharkfail.pcapng
- 542
- 11.300608
- 1.6.1
- host
- USB
- 7232
- URB_BULK in
```  
![USB-frame.png](images/USB-frame%201.png)
The uRB_bulk ins seem to contain info about pdf files or other windows/mac strings. This was the filter I used to isolate the frames of interest.
`((usb.dst == "host" ) && (usb.src == "1.6.1")) && (usb.endpoint_address == 0x81) and !usbms` useful filter, somehow need to extract it
[Maybe a way to extract?](https://github.com/g4ngli0s/CTF/blob/master/AlexCTF2017/Fore3_usb_probing.md)
By the second of night, I was still convinced that each frame had to be extracted and used to re-assemble a file of some kind. I also noticed that  Each non zero area of the left over capture field contained data related to file transfers.
![Difference-in-leftover%20.png](images/Difference-in-leftover%20.png)

So I eventually got a hint that it is a simple challenge and that I may be over thinking. So I went back to wireshark and played around with some basic functions. Then I tried strings on the pcap and saw an odd looking string which turned out to be base64 encoded.

![shark-fail-flag.png](images/shark-fail-flag%201.png)
`StormCTF{Misc2:76eF124163763B352B988cBA1e775A8A}`

## Blocky
### Description
```
## Blocky

### 200

We found this archive with indecipherable text. Can you make sense of it?
```

Well it was zip file that when unzip returned a bunch of ascii files. Since I recently attempted a challenge that involved ASCII art of commands, I immediately zoomed out on the text file to check.

![Qr-looking-text.png](images/Qr-looking-text%201.png)
`424c426c447a576b414373507855716f674f6e666c58774c50486151784e4a737a46514654755944756171`  is an example of a  string I got from the qr code. 
A separate text file produced a separate string `7554796f7049654e51576962746a71666b52724263594a776c6a6c675367554857665948515a50674a6a75` This suggest that only one text file had the flag  or we have to append each string together to get the resulting flag.

I used the below script to extract the payload for each text file.

```
from PIL import Image
from pyzbar.pyzbar import decode
import os



def get_all_files():
    
    for f in os.listdir('/path-to-text-files'):
        if os.path.isfile(os.path.join("/path-to-text-files",f)):
               yield f 

def get_qr_content():
    # this will print out the hex content to stdout    
    row_len = 244
    col_amt = 244
    for file_name in get_all_files():
        img = Image.new(mode = "RGB",size = (row_len+5, col_amt+5))
        pixels = img.load()
        row_pos=0
        with open(os.path.join("/path-to-text-files",file_name),"r") as qr_input:
            for line in qr_input.readlines():
               
                for col_pos,char in enumerate(line):
                    if char =="0":
                    #white is 0
                        pixels[row_pos,col_pos]= (0,0,0)            
                    else:
                    #black is 1
                        pixels[row_pos,col_pos] =(255,255,255)
                row_pos +=1
            #so either the file exenstion has to match or it doesn't like . or some kind of modifier
            img.save("/path-to-store-qrcode/"+file_name.split(".")[0],format="PNG")
            result=decode(Image.open(("/path-to-store-qrcode/"+file_name.split(".")[0])))
            print((result[0].data.decode("utf-8")[2:]))

```

I redirected  the output to stdout and then analyzed the payload in cyberchef.
![Hex-strings.png](images/Hex-strings%201.png)

After extracting all of the payloads, I was careless and didn't try to parse the output for the flag format. It wasn't until I was using [dcode](https://www.dcode.fr/) to see if the payload was a result of some cryptographic function that I discovered several occurrences of  `CTF`   and `flag`. 
`flag3{6ea6d2a4e2d3a4bd5e275401aa086d86}`



### Python Versioning
Pyzbar is supported for python3 and python2 while zbar is python2 only.

## ZipFil
```
## ZipFil

### 300

There's something wrong with this file.
```
## Attack
I didn't solve this challenge but my initial efforts suggested that  the problem was to correct several header fields in order to unzip the file with the flag.

# WEB
## Secret Service
```
S## ecret Service

### 100

Docker Container Information:  
Host: 10.10.100.200 Port: 42866/tcp
```
![Secret-serivce-example.png](images/Secret-serivce-example%201.png)
There are 8 color options that change for each attempt. Convert the  date to it's integer representation and t add the future date. Then divide by the current number of colors, decrementing when the remainder is not zero. Once the remainder is zero, the corresponding color is the answer.
`GPSCTF{952a1af38062c22b7187c97a52ac9bec}`

```
import datetime
import sys
# mod8 since there always 8 colors
#2021-08-15 15:01:59.996575
def get_date_int():
    curr_date=datetime.datetime.now().strftime("%Y-%m-%d")
    results=str(curr_date).split("-")
    print(results)
    year,month,day = results[0],results[1],results[2]
    return int(year)+int(month)+int(day)

future_date =int(sys.argv[1])
date_val=get_date_int()
mod=8
while (date_val+future_date) % mod !=0:
    mod -=1
print(mod)
    
```
