## Terrorist Attack
**Chall**

Evil Master Xandred wants to attack someone. So, he sends the details to his allies Dayu and Serrator through encrypted mail. However, Jayden, the saviour, eavesdropped on the message. Based on the public certificates of Dayu and Serrator, Jayden extracted their public keys (N, e1) and (N,e2). Raise the flag to stop the attack.

Encryption Scheme: Jayden knows that Xandred communicated using RSA, where message m is encrypted such that c = me mod N.
The RSA message m is constructed from the plaintext by the following method:
First, the message is encoded in base64. Then, the ASCII values (in hexadecimal base. ASCII of Z = 5a) of each character of the base64 encoded string is taken and concatenated to form a hexadecimal string. The decimal value of this hexadecimal string is the RSA message m (m is less than N).

Example: 
Plain text: “Beispieltext”

Base64(Plaintext) = “QmVpc3BpZWx0ZXh0”

Converting each character into ASCII values in the hexadecimal base and concatenating them, we get “516d5670633342705a5778305a586830”
This corresponds to the integer
108235181207639582495826983402300008496
So, the ciphertext is
c = 108235181207639582495826983402300008496e mod N

```
Jayden.txt
n=402394248802762560784459411647796431108620322919897426002417858465984510150839043308712123310510922610690378085519407742502585978563438101321191019034005392771936629869360205383247721026151449660543966528254014636648532640397857580791648563954248342700568953634713286153354659774351731627683020456167612375777
e1=3
e2=0x10001
c1=67090645181632709695909298617353138782473392303835333880763035023398399986102522696207286994028014029479955043913066845767219313073168226921458651197268124266204694732369429212400077185147687076698999058253541539181075009601524169290102789307319784203160878830115189236220647878370932124691829160238166884507
c2=320619849161592602976577061113061848506725544626934206904193730593575376891316859724098919371817228348187363536514796561697241275831333616877986761327123283643554751189999114073665767746826416394998880017351368095327983542692476081042891563760767627156393835619028739103574351913497376152704326725037693741418
```

**Solution**

The same message was encrypted with different public exponent but same modulus
we can efficiently calculate the message if GCD(e1, e2) = 1

Using extended euclid's algorithm we can find a and b such that
a*e1 + b*e2 = 1

Let
c1 = pow(m, e1, n)
c2 = pow(m, e2, n)

then

```python
m = (pow(c1, a, n)*pow(c2, b, n)) % n
```

**Flag**
```
cryptX{SuN1l_9AVaskAR}
```

## Chill Maaro
**Chall**
```
key_lelo.txt
p = 103962645086144458394690392333320463500176877592139194126565897252699227389054752050860916642155272976067269318854290849706050750024964367506243628724742178891177469067035094968932705968778096858802301049224190400062964931585852844156067570881650783099922374023185643146939610733140914730176277036929861453893
ct = 7744856707038003173555106357176651001929262082331911859281384984
e = 3
```
```
cipher_text.txt
B0 : b'1CL8'
B1 : b'\x1al\x16_'
B2 : b'\x11Y\x01\x1a'
B3 : b'_kXf'
B4 : b'r\x03_f'
B5 : b'\x7fh]/'
```

[encrypt.zip file](./encrypt.zip)

Submit the FLAG obtained

**Solution**

key-lelo.txt: suggests an RSA encryption but with only one prime though the message was small just taking cube root was just fine. this gives the encryption key for rar file.

we get encrypt.py file the logic was simple
data was divided into of 4 bytes block and the cipher array is given by

cipher[n] = XOR(plaintext[n], plaintext[n+2])

since we know the first two blocks cryptX{k thus we can find rest

```python

XOR = lambda a, b: bytes([x^y for x,y in zip(a, b)])


cipher = [b'1CL8', b'\x1al\x16_', b'\x11Y\x01\x1a', b'_kXf', b'r\x03_f', b'\x7fh]/']
plaintext = [b'cryp', b'tX{k']

for i in range(6):
    plaintext.append(XOR(cipher[i], plaintext[i]))
```

**Flag**
```
cryptX{kR15Hn4m4Ch4R1 5R1kk4N7h}
```
## Jack n Jill
**Chall**
```
Jack and Jill went up the hill. So, that they could get a better network to attend the CryptX workshop. In the workshop, they learnt that it is possible to create truly unbreakable ciphertexts if you link a stream of true random numbers to the plaintext. The link operation can be created bytewise when using the Vigenère cipher (for example addition of the corresponding numerical values modulo 26) or by using XOR (exclusive OR of the individual bits).
Since then Jack and Jill have encrypted their messages to each other using the Vigenère cipher to combine the different characters. Their plaintexts only consist of the 26 capital letters of the alphabet. As random numbers, they use a random number sequence.
For this challenge, A = 0, B = 1,......, Z = 25
Example-
Plaintext - TEST = (19 4 23 19)
Key Stream = 16, 8, 17, 23, 0, 56,.........
Sample ciphertext:
(19+16) mod 26 = 9 = J
(4+8) mod 26 = 12 = M
(23+17) mod 26 = 14 = O
(19+23) mod 26 = 16 = Q
Ciphertext - J M O Q

This method is very easy, but the difficulty lies in generating a truly random key-stream. So, Jack and Jill decided to keep things simple and used Pi = 3.14159265358979323846……… as the infinite, random number sequence. They also agreed to use the offset in the keystream as key. 
For example, offset 7 is the digit “6” (bolded).
From then on they took the following keystream and always grouped 2 digits as one number for the random number sequence. With an offset of 7, the keystream would be 53, 58, 97, 93, 23, …
Also, to ensure that the method did not become too complex, they mutually agreed that the offset will not be greater than 200, and also they will change the key often.

You know the method, but not the key. Can you still find the flag?
Submit the flag by wrapping it within cryptX{}. The Flag is a single word in UPPERCASE without space.
```
> jack_n_jill.txt
```
Y W E X D Z S H Q G E G A J B V H X M W B O T X E D C H P U C M T W L P Z I E H H K N O G D M E D B H N N E P J T E I K X V A B F R R P C P K U Z W Q U Y H P C D U G J B I K C A U X G Z A W S Q V L J V Z X J K N N U Z R A U X B H F Q W X Y Q Z
```

**Solution**

the stream cipher is not secure as it is using the digits of pi which are known moreover the offset is only 200 so just need to brute force the 200 offsets and manually search for the plaintext

```python
digits = '14159265358979323846264338327950288419716939937510582097494459230781640628620899862803482534211706798214808651328230664709384460955058223172535940812848111745028410270193852110555964462294895493038196442881097566593344612847564823378678316527120190914564856692346034861045432664821339360726024914127372458700660631558817488152092096282925409171536436789259036001133053054882046652138414695194151160943305727036575959195309218611738193261179310511854807446237996274956735188575272489122793818301194912'
cipher = ['Y', 'W', 'E', 'X', 'D', 'Z', 'S', 'H', 'Q', 'G', 'E', 'G', 'A', 'J', 'B', 'V', 'H', 'X', 'M', 'W', 'B', 'O', 'T', 'X', 'E', 'D', 'C', 'H', 'P', 'U', 'C', 'M', 'T', 'W', 'L', 'P', 'Z', 'I', 'E', 'H', 'H', 'K', 'N', 'O', 'G', 'D', 'M', 'E', 'D', 'B', 'H', 'N', 'N', 'E', 'P', 'J', 'T', 'E', 'I', 'K', 'X', 'V', 'A', 'B', 'F', 'R', 'R', 'P', 'C', 'P', 'K', 'U', 'Z', 'W', 'Q', 'U', 'Y', 'H', 'P', 'C', 'D', 'U', 'G', 'J', 'B', 'I', 'K', 'C', 'A', 'U', 'X', 'G', 'Z', 'A', 'W', 'S', 'Q', 'V', 'L', 'J', 'V', 'Z', 'X', 'J', 'K', 'N', 'N', 'U', 'Z', 'R', 'A', 'U', 'X', 'B', 'H', 'F', 'Q', 'W', 'X', 'Y', 'Q', 'Z']

for offset in range(201):
    out = ''
    for i, c in enumerate(cipher):
        out += chr((((ord(c)-65)-int(digits[offset+2*i:offset+2*i+2]))%26) + 65)
    print(out)
```
at offset 163 we get `WELLDONEYOUDESERVEAGREATROUNDOFAPPLAUSEONREACHINGHEREANDFINDINGTHECORRECTOFFSETSOASAREWARDIWILLTELLYOUTHATTHEFLAGISGANGULY`

**Flag**
```
cryptX{GANGULY}
```
