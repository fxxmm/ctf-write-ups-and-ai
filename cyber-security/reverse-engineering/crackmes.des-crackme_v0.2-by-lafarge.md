---
description: https://crackmes.one/crackme/5ab77f5633c5d40ad448c2f0
---

# crackmes.de's crackme\_v0.2 by lafarge

Check the file type: file crackme.exe

Scan for strings: strings crackme.exe

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>



Load the crackme into a disassembler or decompiler to inspect its structure without running it.

Find the entry point: Locate the main function. This is where the program's execution begins.

&#x20;

I am trying to use OllyDBG to do a crackmepatched.exe.

Time to change the program to give me access even when I am not supposed to have it.

Load it in.

Right click. Search for > All Referenced Text Strings

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

Right click. Follow in Disassembler.

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

0040128E is the memory address of the instruction that is always going to let us in.

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

Right click. Copy to executable. All modifications.

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

Right click. Save file.

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

&#x20;

In the original program, it compares the correct key with the key that we give it.

But, the key is stored at the memory spot 00406B84.

<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

And, we have the correct register code at this memory.

So, instead of printing out the phrase “Nope, that’s not it!\n\rTry again", let’s print out the correct key or whatever is at the memory.

<figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

&#x20;

Note: Can also try 00406584.

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

Right Click. Copy to executable. All modifications.

Right click. Save file.

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

SXIW-RBET-ONIPW-YFUR

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

&#x20;
