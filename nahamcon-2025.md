# NahamCon 2025

## What A Game that was!

<figure><img src=".gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Go to the website and finish the game.

View page source.

<figure><img src=".gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

\u007B is Unicode Left Curly Bracket.

\u007D is Unicode Right Curly Bracket.

The flag is {whatacrazygamethatwas}.

## NahamCon Day 1

<figure><img src=".gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

The flag is ctf{day\_1\_lets\_g00}.

## Read The Rules

<figure><img src=".gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

The flag is flag{90bc54705794a62015369fd8e86e557b}.

## Quartet

<figure><img src=".gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Download the files and place them into one folder.

┌──(kali㉿kali)-\[\~/Downloads]

└─$ file quartet.z01

quartet.z01: Zip multi-volume archive data, at least PKZIP v2.50 to extract

┌──(kali㉿kali)-\[\~/Downloads]

└─$ mkdir quartet

┌──(kali㉿kali)-\[\~/Downloads]

└─$ mv quartet.z01 quartet.z02 quartet.z03 quartet.z04 quartet

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ sudo apt-get install p7zip-full

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ 7z x quartet.z01

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ 7z x quartet.z02

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ 7z x quartet.z03

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ 7z x quartet.z04

┌──(kali㉿kali)-\[\~/Downloads/quartet]

└─$ strings quartet.jpeg

![](<.gitbook/assets/unknown (22).png>)

Important Notes:

Order matters: You must start the extraction with the .z01 file, not .zip, as .z01 is the first part of the archive.

Complete archive: Ensure all parts of the archive are present in the same directory before extracting.

The flag is flag{8f667b09d0e821f4e14d59a8037eb376}.

## Technical Support

<figure><img src=".gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

Go to the Discord and look for the #ctf-support channel.

<figure><img src=".gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

The flag is flag{a98373a74abb8c5ebb8f5192e034a91c}.

## The Mission – Start Here

<figure><img src=".gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

The flag is flag{}.

## Flagdle

<figure><img src=".gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

POST /guess HTTP/1.1

Host: challenge.nahamcon.com:32105

Accept-Language: en-US,en;q=0.9

Upgrade-Insecure-Requests: 1

User-Agent: Mozilla/5.0 (X11; Linux x86\_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/136.0.0.0 Safari/537.36

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,_/_;q=0.8,application/signed-exchange;v=b3;q=0.7

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

Request: POST /guess HTTP/1.1

Host: challenge.nahamcon.com:32105

Content-Type: application/json

Accept: application/json

User-Agent: Mozilla/5.0 (X11; Linux x86\_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/136.0.0.0 Safari/537.36

Content-Length: 63

{

```
"guess": "flag{deadbeefdeadbeefdeadbeefdeadbeef}"
```

}

Response: HTTP/1.1 200 OK

Server: Werkzeug/3.1.3 Python/3.11.12

Date: Sat, 24 May 2025 13:28:11 GMT

Content-Type: application/json

Content-Length: 272

Connection: close

{"result":"\ud83d\udfe8\ud83d\udfe9\ud83d\udfe8\ud83d\udfe8\ud83d\udfe8\u2b1b\u2b1b\u2b1b\u2b1b\u2b1b\ud83d\udfe8\u2b1b\ud83d\udfe9\u2b1b\u2b1b\u2b1b\u2b1b\u2b1b\u2b1b\u2b1b\ud83d\udfe8\u2b1b\ud83d\udfe9\u2b1b\u2b1b\ud83d\udfe9\u2b1b\u2b1b\ud83d\udfe8\u2b1b\u2b1b\u2b1b"}

\ud83d\udfe8🟨 (🟨 - correct letter, wrong position)

\uD83D\uDFE9🟩 (🟩 - correct letter, correct position)

\u2b1b⬛ (⬛ - incorrect letter)

Just aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa until 00000000000000000000000000000000.

The flag is flag{bec42475a614b9c9ba80d0eb7ed258c5}.

## TMCB

<figure><img src=".gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

[Online Python - IDE, Editor, Compiler, Interpreter](https://www.online-python.com/)

print(\*(range(1, 1000000)), sep=',')

print(\*(range(1000000, 2000001)), sep=',')

<figure><img src=".gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

The flag appeared after I refreshed the page. This was while I was playing around with the console and put $0=true. ALL\_CHECKED=true. I also edited the html as such: \<form id="checkbox-form"> before the \<div id='grid-container'>.

<figure><img src=".gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

<figure><img src=".gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

The flag is flag{7d798903eb2a1823803a243dde6e9d5b}.
