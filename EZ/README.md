## Cesar Pista @₹62
**Chall**

The plaintext is in English and case sensitive. Submit the entire text wrapping it in cryptX{}. The punctuations and spaces are the same as those in the plaintext.
```
Xlmw irgvCtxih qiwweki wlepp gpevmjC lsA RSX xs irgvCtx e qiwweki xsheC! Izir mj mx Aew wyjjmgmirx efsyx 6444 Cievw eks, sv xs fi qsvi tvigmwi mr xli Ciev 88 FG, rsAeheCw mx mw rsx. XsheC iegl ws-geppih Wgvmtx Omhhmi Asyph fi efpi xs kix wirwmxmzi mrjsvqexmsr, mj xliC Aivi irgvCtxih xlmw AeC.
```

**Solution**

**Flag**
```
cryptX{This encrypted message shall clarify how NOT to encrypt a message today! Even if it was sufficient about 2000 years ago, or to be more precise in the Year 44 BC, nowadays it is not. Today each so-called Script Kiddie would be able to get sensitive information if they were encrypted this way.}
```

## BroCODE
**Chall**

Encryption Scheme:

Step1: All spaces in the plaintext are removed.

Step2: The plaintext is split into 2 parts. The left part consists of all letters that are in  even positions (0-based indexing). Rest letters on the right part.

Step3: Step2 is repeated on the resultant strings until the length of each part is less than or equal to 2 letters.

Step4: All the parts are merged to form the ciphertext.

See example.jpg for an illustrative example of encryption of plaintext```CRYPTO```.

![](./example.jpg)

The ciphertext given below is encrypted using the above scheme
```mNsnhHnrh411DD3940```

**Solution**

**Flag**
```
cryptX{m4H3nDr4s1n9hDh0N1}
```

## Key Bored
**Chall**

Uff! Due to the pandemic, I spend most of the time in my room. I was very bored. So, one fine evening I decided to visit one of my friend’s home. We were playing video games and enjoying supper. Suddenly, I remembered that I had to send an important message to my prof. So, I used her LAPTOP to send the message. But it all got messed up. Can you retrieve the correct message for my prof?
```
(( !!$ !@! !!@ !!^ ** !@# %# !)( *@ &# %% &# (% !)( %@ &* ^* &@ %@ !!) %@ !@%
```
Submit the FLAG obtained (without spaces)

**Solution**

**Flag**
```
cryptX{5mRI7I_m4NDH4n4}
```

## Rookie SA challenge
**Chall**
```
e: 1
c: 8663069917557759315104008369297528808616317
n: 245841236512478852752909734912575581815967630033049838269083
```
Submit the flag by wrapping it within cryptX{}

**Solution**

**Flag**
```
```
