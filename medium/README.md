## G@WD
**Chall**

Encryption Scheme:

Step1: All spaces in the message are removed.

Step2: The message is divided into blocks of the same length as that of the key.

Step3: Finally each block is encrypted according to the below example.

Example- The plaintext is "one messenger". The key, for this example, is "3142". After diving it blocks of size equal to that of the size of the key, i.e., 4, the message becomes “onem esse nger”. Key 3142 implies that the 1st letter is moved to the 3rd position, the 2nd letter is moved to the 1st position and so on. So, the message becomes “nmoe sees grne”. Finally, the ciphertext is “nmoeseesgrne”.

The below message is decrypted using a key of length 7. Analysis by inspection might save you from brute-forcing.
```
kietrcCnstraiweudtdcoinabIdotrisBiylaorsihhne1itsehnttc8nydtraurfsteihkietrccwuaslbcbtlisaeien1hdsa2ti9N7carinloteeaktcnfdioImniotddaiatslyptrTeisftmchtaslt25niu1n93ueJotrdaL2oemibcsetsighnehamttxgbraoetteestdncrkecitttussat1o93rmFinahId2wtaidoainl1utto2ri5f9rfstsitvsicetTIrnioytrfstsitayrs0e5tierfnootnaaincrkecilinawIdteoofsnaeeakhwtatmsreeinnginw3l5onyofhirtef61Tet9stmchtaspilastehdefeTysg73ailku4RDLn
```
Submit the flag by wrapping within cryptX{}

**Solution**


**Flag**
```
cryptX{73nDuLk4R}
```

## MODesty is an art
**Chall**

English alphabet consists of 26 letters. Each letter is represented as {A=0, B=1,  C=2,......., Z=25}.
The rule to encrypt a plaintext letter x to a ciphertext letter y is y = (17*x + 7) mod 26.
The ciphertext given below is encrypted using the above scheme
```
WHKDHUCKXXS
```

Submit the obtained plaintext in CAPITAL LETTERS by wrapping within cryptX{}

**Solution**

**Flag**
```
cryptX{HARMANPREET}
```
