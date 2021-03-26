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

## Roadside Adventure
**Chall**
```
ct= 7126580361511136202149310992881704708874352034844039495129478796981594363458831923608084684705284908857283363026771807079807491716306487481801803742758334898449520139860380270566510027596640909424796606053526376645098480795323284620588659251453978973228260601887666398624075688201263514008446635069503258091768533417554587946370347158439777880793035960811923479897277625095568046142887766450075187770912560112069202528487205624160427628261453531754188662497434639529741658377745694277734246061833152731092288327460418393049069295374133644935840237394202389729663536913568814833320983377446242374922782919712522594221
e= 65537
n= 25368447768323504911600571988774494107818159082103458909402378375896888147122503938518591402940401613482043710928629612450119548224453500663121617535722112844472859040198762641907836363229969155712075958868854330020410559684508712810222293531147857306199021834554435068975911739307607540505629883798642466233546635096780559373979170475222394473493457660803818950607714830510840577490628849303933022437114380092662378432401109413796410640006146844170094240232072224662551989418393330140325743682017287713705780111627575953826016488999945470058220771848171583260999599619753854835899967952821690531655365651736970047327
p-q= 13850705243110859039354321081017038361100285164728565071420492338985283998938739255457649493117185659009054998475484599174052182163568940357425209817392780314915968465598416149706099257132486744034100104272832634714470968608095808094711578599330447351992808756520378741868674695777659183569180981300608614286
```
Submit the FLAG obtained

**Solution**

**Flag**
```
cryptX{m0H4mM4d_4Zh4rUdDin}
```
