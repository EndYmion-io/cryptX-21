# cryptX 21

Write-ups for 24-hour Capture The Flag event by Department of Electrical Engineering, IIT (BHU) Varanasi

## Overview
```
Title                          Points   Flag
------------------------------ ------   -----------------------------
WELCOME:
Sanity Check                   100      cryptX{}

EZ:
Cesar Pista @₹62               /        cryptX{This encrypted message shall clarify how NOT to encrypt a message today! Even if it was sufficient about 2000 years ago, or to be more precise in the Year 44 BC, nowadays it is not. Today each so-called Script Kiddie would be able to get sensitive information if they were encrypted this way.}
BroCODE                        /        cryptX{m4H3nDr4s1n9hDh0N1}
Key Bored                      /        cryptX{5mRI7I_m4NDH4n4}
Rookie SA challenge            /        cryptX{}

MEDIUM:
G@WD                           /        cryptX{73nDuLk4R}
MODesty is an art              /        cryptX{HARMANPREET}

HARD:
Terrorist Attack               /        cryptX{SuN1l_9AVaskAR}
Chill Maaro                    /        cryptX{kR15Hn4m4Ch4R1 5R1kk4N7h}
```

##Sanity Check
**Chall**

**Solution**

**Flag**
```
cryptX{}
```

##Cesar Pista @₹62
**Chall**
```Xlmw irgvCtxih qiwweki wlepp gpevmjC lsA RSX xs irgvCtx e qiwweki xsheC! Izir mj mx Aew wyjjmgmirx efsyx 6444 Cievw eks, sv xs fi qsvi tvigmwi mr xli Ciev 88 FG, rsAeheCw mx mw rsx. XsheC iegl ws-geppih Wgvmtx Omhhmi Asyph fi efpi xs kix wirwmxmzi mrjsvqexmsr, mj xliC Aivi irgvCtxih xlmw AeC.```
The plaintext is in English and case sensitive. Submit the entire text wrapping it in cryptX{}. The punctuations and spaces are the same as those in the plaintext.
**Solution**

**Flag**
```cryptX{This encrypted message shall clarify how NOT to encrypt a message today! Even if it was sufficient about 2000 years ago, or to be more precise in the Year 44 BC, nowadays it is not. Today each so-called Script Kiddie would be able to get sensitive information if they were encrypted this way.}```

##BroCODE
**Chall**
Encryption Scheme:
Step1: All spaces in the plaintext are removed.
Step2: The plaintext is split into 2 parts. The left part consists of all letters that are in  even positions (0-based indexing). Rest letters on the right part.
Step3: Step2 is repeated on the resultant strings until the length of each part is less than or equal to 2 letters.
Step4: All the parts are merged to form the ciphertext.
See example.jpg for an illustrative example of encryption of plaintext “CRYPTO”.
![](

The ciphertext given below is encrypted using the above scheme
```mNsnhHnrh411DD3940```

Enter the plaintext in without spaces, wrapped up in cryptX{}.

**Solution**

**Flag**
```cryptX{m4H3nDr4s1n9hDh0N1}```
