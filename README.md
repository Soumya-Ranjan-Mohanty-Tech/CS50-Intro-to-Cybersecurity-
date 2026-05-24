# CS50-Intro-to-Cybersecurity-
**Securing accounts, securing data, securing systems, security software, preserving privacy**
**Authentication** refers to the process digitally of proving who you are.
**Autherisation** refers to something that you should have access to something, one you have proven you are you.
**Username** It presumably uniquely identifies you to the world.
**Password** 
**Dictonary Attack**: We should have a stronger password. Attackers will open a file on their computer containing a whole lot of actual english words or in some other english language- they will get into our accounts if have setup a preety guesable password.
**Brute force attack**: Using softaware to digitally try all possible password in the world.
**4 Digit Password**: 9999+1(0000) possible passwords- 10^4. How long will a hacker to get in my device if i have just a four-digit password?- 
**Brute Force**: Go ahead in a text file called crack.py, where crack is actually a term of art. It just means to figure out what a password is to brute force your way in. I'm going to go ahead and from a library called string, I'm going to go ahead and import digits. Now, this is a very easy way of just giving me access to the numbers 0 through nine. **a)** try all possible digits for the first value. Try all possible digits for the second, then for the third, then for the fourth. **b)** I'm going to use a keyword in Python called "for", which just means do something for as long as I want you to. **c)** I'm going to give myself a variable like in math, just so I can use something to keep track of each number. **d)** And I'm going to use a default value of **"I"** for integer. And then I'm going to go ahead and say that for each value **"I"** inthose 10 digits I want to go ahead and do the following. **e)** for each of those "I" digits for the first value **"I"** want to do for **"J"** in digits as well. And then for each value for my third placeholder I might do something like for **"K"** in digits. And then lastly I might do for **"L"** in digits. 
**a)** I'm going to open up a separate window on my screen here. It's called a "terminal window" and I'm going to go ahead and run "Python of crack.py".

1) For 4-digits **from string import digits**

**for i in digits:
    for j in digits: 
        for k in digits:
            for l in digits:
                print(i, j, k, l)**

2) for 4-letters - **from string import ascii_letters**
**for i in ascii_letters:
    for j in ascii_letters: 
        for k in ascii_letters:
            for l in ascii_letters:
                print(i, j, k, l)**
   
2) for 4-letters - **from string import ascii_letters, digits, punctuation**
**for i in ascii_letters + digits + punctuation:
    for j in ascii_letters + digits + punctuation: 
        for k in ascii_letters + digits + punctuation:
            for l in ascii_letters + digits + punctuation:
                print(i, j, k, l)**

Itering from left to right

**National Institute of Standards and Technology (NIST)**
1) memorized secrets shall be at least eight characters in length.
2) Verifiers should permit subscriber chosen memorized secrets of at least 64 characters in length.
3) All printing ASCII characters as well as the space characters should be acceptable in memorize secrets. - generally refers to US English symbols on a US English keyboard as was the origin of this code system. Um so that includes A through Z, 0 through 9 and the punctuation.
4)  Unicode characters should be accepted as well.
5)  Verifiers, the website or the apps that we're using shall compare the prospective secrets, the passwords you're choosing against a list that contains values known to be commonly used, expected, or compromised.
6)  repetitive or sequential characters.
7)  And then lastly, context specific words such as the name of the service, the username, and derivatives thereof. EXAMPLE: Gmail password
8)  verifiers shall not permit the subscriber to sure to store a hint that is inaccessible to an unauthenticated claimant. Verifiers shall not prompt subscribers to use specific types of information. For instance, what was the name of your first pet when choosing memorized secrets.
9)  verifiers shall not require memorized secrets to be changed arbitrarily for instance periodically. So this one too is something that a lot of companies violate as a re recommendation still. If you're in a corporate workplace in particular and you're being required by the system administrators to change your password every month, maybe every 3 months, 6 months, every year perhaps.
10)  Verifiers shall implement a rate limiting mechanism that effectively limits the number of failed authentication attempts that can be made on the subscribers account.
11)  Two-factor authentication or 2FA, more generally known as multiffactor authentication, is a technology whereby in addition to having one factor that you use to log in, like your password, as is tradition, you also have a second or maybe more factors that you additionally have to use in order to log in. - they're broken down into these three categories. One is a **knowledge category**. A knowledge factor is just something that you know, something like your password that ideally you keep secret. second type of factor would be a **possession factor**. The presumption is if that you challenge the user not only for a knowledge factor like their password but
a second factor like something they possess.  And then a third type of factor nowadays might be an **inherent(key fob/PHONES)** something that is unique to you specifically more generally described as biometrics. So maybe it's your fingerprints, maybe it is your face nowadays. Something that's inherent to you can be a third factor nowadays because the presumption is that only you ideally in the world have exactly that factor as well.

**One-Time Password or OTP.**
**SIM SWAPPING**
if I'm an adversary and I just have any old phone with any old SIM card in, I figure out what the unique ID is and maybe I call up David's mobile phone provider and I somehow convince them that I am David by tricking them into believing it's me as by telling them all of those personal information, all of that personal information about myself, I might be able to convince them to swap my SIM card, the adversaries, with what is already on file. The implication of that is that when David subsequently gets text messages, they don't actually go to me, the real David. They go to the adversar's phone as well because they're tied to that SIM card.
So, in general nowadays, if you have a choice using some website or app to use SMS or textbased uh messaging versus a native application that you install onto your phone or other device, you should generally prefer the latter. some first class piece of software that actually uses push notifications or your data plan and does not rely on SMS text messaging because of this potential threat.
**Key logging** refers to exactly that, some piece of software that most likely maliciously is literally recording everything you type or everything you tap into that device. But in general, you might be vulnerable to malware, including software that logs all of your keystrokes.
It's very possible, unfortunately, for adversaries to somehow get software, malicious software, otherwise known as malware, onto your Mac, onto your PC, perhaps even onto your phone. This might be because you installed a piece of software that you shouldn't have trusted. This might be because your phone or your device is infected with something like a virus or a worm.
**Credential stuffing**. A credential is something like a username and password. credential stuffing refers to the process of an adversary having found a whole bunch of usernames and passwords, maybe online, maybe in some database that they or someone else attacked and posted for the whole world to download. Credential stuffing means not using dictionaries, not using brute force, but just literally using a list of already known usernames and passwords, maybe from some other application or website to try to stuff them into a different website to see if well maybe if David's using this username and password over here with high probability he's probably using the same username and password over here. So credential stuffing is the threat that I dare say many of you are vulnerable to.
**social engineering**
**Phishing**: Phishing is all about trying to use social engineering, in this case in a technical way to try to convince you through very convincing looking emails and even websites that it is a legitimate email from paypal.com or it is a legitimate email from a politician or it is a legitimate email or request from a teacher here at Harvard, but it's not.
Well, you should minimally be looking at the URL bar and making sure that it is gmail.com or probably google.com or whatever google.country code depending on where you live in the world. Making sure that it looks legitimate and that you've actually been there before.
**Machine in the middle attack**: if you're on the internet, there are, suffice it to say, many other machines on the internet very often between you and whatever website or app you are visiting. [Often those machines might be things like routers], uh, [servers that internet service providers], companies, universities, maybe even your own home owns and controls, but all of your data is passing through those machines in the middle, so to speak. If any of them are malicious and are maybe storing your data, looking at your data, it's possible that you might not be having secure communications with the other end unless you are using certain defenses.
**Well, a solution to someof these problems might be this single sign on or SSO**
**single sign on or SSO**:  So, single sign on refers to an ability to sign up for to log into one website using an account that you already have on another website. And very often the account that you use is one of the big ones, one of the popular websites or applications out there.

**Password Managers**
Apple - iCloud Keychain
Google - Password Manager
Microsoft - Credential Manager

**Encrption and Decryption**

1) apple Hash  ⊳ **Hash Function** ⊳ 1
2) banana ⊳ **Hash Functiion** ⊳2 (Hash Value)

**Dictonary Attacks**
You can still use a dictionary for instance of English words or better yet a dictionary of English fruits and you could one fruit at a time run each of those values as input into the same hash function, the library or code that you're using to achieve this and then that's going to give you one hash value after another and you could compare each of those hash values against whatever is in the database or the file of passwords that you the hacker in the story might have actually stolen somehow. You have to do more work though because it's no longer as simple as just comparing apple against apple and banana against banana. You actually have to do some work. You have to do some computational work.
**Brute Force**
the adversary resort to brute force attacks and you can try even the simplest of passwords like 000000 or maybe eight zeros instead. And you can hash that and see what the resulting hash value is and compare that against what's in the database. Then you could try 000000 00001 hash that compare that against what's in the database and then move on to the next and the next. Doing this not just for numbers but for letters as well.
**Rainbow Table**
 There's a term of art known as a rainbow table which is a very beautiful way of saying that adversaries in advance might have already hashed all possible English words in a dictionary. Adversaries might have already hashed all possible passwords of length four or five or six or seven or eight or something else. And maybe if they have a big enough hard drive, they are storing a big table like an Excel file or a CSV file of all of the words that they've tried, all of the passwords they've tried and all of the hash values they've **already computed**. Then it's even easier. Then they don't even need to do a brute force attack per se, hashing and hashing and hashing and hashing. Then they can just compare, compare, compare because indeed a rainbow table simply contains all of the passwords they've tried, all of the hash values they've generated. And so they just compare left to right whatever the user typed in against the hash value they've already computed. Now for certain hash functions, this threat of a rainbow table is just not feasible. You might need terabytes or pabytes of data, which means a lot of hard drive and a lot of money. So there are potential downward pressures on this kind of an attack, but it can certainly speed things up.
**Salting**
Salt isn't something that's meant to be private or secret or secure. It's just sprinkled in there to make sure that whatever hash value comes out of this black box is a little bit different than if you had put a different salt value instead.
Different users should have different salt values just in case they choose the same passwords.
**The salt is actually stored in the hash value itself** according to this algorithm in the first two characters. The next time Carol logs in, she types in her username, Carol, and hits enter. The server now knows, okay, I'm expecting a password from Carol. Let's see what she types in. Suppose that she types in correctly. Cherry. Now, the system is not storing Cherry. So, it's not going to compare literally what Carol typed in. But it is going to hash Cherry(PASSWORD). But first, the system's going to check what is Carol's salt, and it's going to infer as much by looking at Carol's hash value and looking only at the first two characters by convention. Then what the server is going to do, it's going to take whatever Carol typed in, cherry, c h e r r y, it's going to pass in 50, and then hopefully it's going to get back this same value here, this whole string in yellow. And if those are correct, then the carol will be considered authenticated. By contrast, if the username happens to be Charlie and Charlie hits enter, then what the server is going to do is look at Charlie's hash value, grab the first two characters for Charlie's salt, use that salt and cherry as the input to the hash function, and hope that the result is Charlie's value, not Carol's.

1) cherry + 5θ(Salt Value) ⊳ **Hash Function** ⊳ 5θxyv355l.mcl

**NIST -  National Institute for Standards and Technology**
verifiers shall store memorized secrets in the form that is resistant to offline attacks. Memorized secrets shall be salted and hashed using a suitable one-way key derivation function. Their purpose is to make each password guessing uh trial by an attacker who has obtained a password hash file expensive and therefore the cost of guessing attack of a guessing attack high or prohibitive.

**One way hash function**
**Arbitary lenghth - fixed length**
These are mathematical functions, or in the context of programmin these are function written in code languages like python or otherwise that take as input string of arbitrary length that is a password. And what's key to this crptographic functions are these outputs of has values of fixed lengths.
cryptographic these one-way hash functions are one way in the sense that they take a potentially infinite domain if you know this term from mathematics and condense it into a finite range that is a huge number of values all possible passwords in the world to just a finite list of possible hash values it might be a long list of possible hash values but indeed no matter how long a string of text is if it's of some fixed length 16 characters, 32 characters, something else. There's only a finite number of those values.

**Crptogaphy**
Cryptography is all about the practice and study of securing our data particularly when we want to transmit it from one person to another.
Cryptography can be broken down into acouple of different categories. One of which are codes.
**Codes**
Note: codes are not the type of code that you might write in Python or the like. It has nothing to do with software, but rather a mapping between what we'll call code words and the actual message or true reading that those words represent.

**Encode**
**Plain Text - Code Text**
 It means taking a plain text message be it in English or any human language and taking that as input and producing as output code text. So, the code text might be a short, succinct sequence of words that might actually be English words, but they're not meant to mean what they normally mean. They're meant to be looked up in the code book to figure out what the message is actually trying to say. Meanwhile, decode, as you might expect, is the opposite. You take as input the code text that you have received as the recipient. You use that same code book to look up the code words and figure out what the actual message is in order to get the original plain text be it in English or any other human language that the code book is designed for.

**Ciphers**
Its best to opt for ciphers rather than encode and decode system Ciphers are more algorithmic in nature.
They don't focus on maybe words or phrases. they might focus on individual letters instead or even bits if it's in the context nowadays of computers. 
To incipher a message means to take that message in English or any other language are so-called plain text and convert it not surprisingly to cipher text as output. Meanwhile, the reverse of or rather an equivalent term here that you might know as well is to encrypt.

**decrypt**
Cipher text - plain text

**Keys**
in the world of cryptography it's quite recommended that you and I use public and well doumented well tried and tested **algorithms** publicly but we do keep one piece of information secret so that our use of that cipher that algorithm is specific to us and this customization this configuration are generally known as keys.
A key is what sort of unlocks the capabilities of this cipher, but it's a key that needs to be known and used not only by you typically, but also by the recipient. So that by having copies of the same key, you can not only encrypt messages or **incipher** them, but you can also decrypt or decipher those messages, too.

**Secret Key Cryptography/symmetric key encryption** 
**(algorithm Caesar cipher is what's generally known as a rotational cipher)**
The presumption is that the security of your data relies on the secrecy of some key. So, if A wants to send a message to B, then A and B must keep secret whatever key they are using to configure their choice of algorithms.
secret key cryptography, specifically in the context of encryption in scrambling data, is also known as symmetric key encryption for the reason that both A and B in this story are going to use the exact same key.
Just think of that key as a number that you and the other person have somehow agreed upon in advance. That algorithm then will ultimately output the cipher text.

**Decryption**

cipher text + key -- plain text

Some of the algorithms now currently used for encryption are:
**AES
Triple DES**
These AES and Triple DES popular algorithms that have been vetted by the world and are very commonly used as secret keyencryption ciphers or symmetric key encryption ciphers, which to be clear require that both the sender and the receiver know and use the exact same key.
**Public Key Cryptography/Asymetric key encryption**
**Diffie Helman,
MQV,
RSA**
Two keys are used one public and a private key. They have a mathematical relationship. It is generated for you. Public key is not secret it is public. But the private is supposed to be kept seceret. If i share the public key in public then some one that has the public key can use the public key to encrypt a message and send it to me. And i, who is having the private key is the onl one in the worls who can decrypt the message.
**RSA**
n = p*q
Our devices(phone/laptop) chooses two big prime numbers and multiply them to give n. Then it uses the resulting n in the following matheamtical calculation.

e =  Public key

c = m^e mod n
m = c^d mod n
If i have a message **m** that i wanna send it to some person and with our public key **e**. That someone can take their message and raise it to the power of **e**, the exponent of e, and the divide it by n, and figure out the remainder when didviding it by n. 

**RSA Public Key Generation (Simplified)**
Step 1: Choose Two Prime Numbers
Pick two large prime numbers:
p=61,q=53

Step 2: Multiply Them
n=p×q
n=61×53=3233
This value becomes part of both keys.

Step 3: Compute Euler’s Totient
ϕ(n)=(p−1)(q−1)
ϕ(n)=60×52=3120

Step 4: Choose Public Exponent e
Choose a number:
1<e<ϕ(n)
coprime with ϕ(n)

**Common choice:
e=65537**
For this small example:
e(public exponent)=17

Step 5: Form the Public Key
The public key is:
(n,e)
So: (3233,17), This is the public key.

Step 6: Generate the Private Key
Find d such that:
d×e≡1(modϕ(n))
For this example: d=2753
**Private key:** (3233,2753)

**Private Key**
You already know:
p=61
q=53
ϕ(n)=3120
e=17

Now we must find the private key: d such that:
d×e≡1(mod3120)                                                    How to find d **e^−1 modϕ(n)
                                                                    So: d=17^−1 mod3120**

Since e=17:
d×17≡1(mod3120)
What Does This Actually Mean?
It means:
Find a number d so that when multiplied by 17 and divided by 3120, the remainder is 1.

Another Way to Write It
We want:
17d=3120k+1
for some integer k.
 
What Is d Actually? d is called the: Modular Multiplicative Inverse of e modulo ϕ(n).
Meaning:
**e^−1 modϕ(n)
So: d=17^−1 mod3120**



**Other Key Exchange**

**Diffie Hellman** [**Diffie–Hellman itself does not encrypt data. It is a key exchange algorithm used to create a shared secret, which is then used by a symmetric encryption algorithm such as Advanced Encryption Standard to encrypt the actual messages.**] 

**Asymmetric Encryption: You take a specific message, lock it with a public key, and send it. Only the private key can unlock it.**

**Diffie-Hellman (Key Exchange): You do not input a message. Instead, you combine your private key with the other person's public key. The math magically creates the same exact number on both sides.SummaryDiffie-Hellman is an Asymmetric Key Exchange algorithm. It uses asymmetric math to create a symmetric key, but it cannot encrypt data on its own.**

First we take a number **g** which is the generator which can be anything like **2 for instance**and then we pick a really big prime number **p** and those are agreed upon in advance and now person **A** picks another really big prime number **a** and then we do the mathematical calculation ie., **g** to the power of **a** **mod** **p**. Meanwhile,**B** or Bob still uses the same **g**, still uses the same **p**, picks his own private key called **b** and raises **g** to the power of **b** **modulo** **p** and that gives him back this value capital **B**. And now Alice and Bob can send those values across the inetrnet **A and B** and thaxs to some modular arithmathic here too.

A = Alic's Public Key
B = Bob's Public Key
g = generator
a = A's private key
b = B's private key
p = Really big prime number

**A = g^a mod p
B = g^b mod p**

Now Alice can take bob's **B** value and raise it to the power of **a**, which effectively gives you **g** to the power of **a** times **b** **mod** **p**(). Bob meanwhile can take the value **A** raise it to the power of it's own private key **b** than mod **p**

**s(A) = B^a mod p
s(B) = A^b mod p**

S = g^a*b mod p
Because (g^{a*b} = g^{b*a}), Alice and Bob now share the exact same number, **S**, without ever revealing **private keys a or b**. This number **S** is then used as the key for symmetric encryption (like AES).

1. Key Derivation Function (KDF)The raw number \(S\) can be massive and might contain mathematical patterns that hackers could exploit. To fix this, both parties feed \(S\) into a Key Derivation Function (usually a cryptographic hash function like SHA-256).The Process: \(KDF(S) = \text{Symmetric Key}\)The Result: A fixed-length, completely random-looking string of bits (e.g., a 256-bit key).

2. Passing to the Symmetric CipherNow that Alice and Bob have the exact same 256-bit key, they load it into a symmetric encryption algorithm, most commonly AES (Advanced Encryption Standard).

3. Encrypting the Actual DataFrom this point forward, the asymmetric math of Diffie-Hellman is finished. The parties communicate using fast, secure symmetric encryption:Alice sends a message: She takes her plaintext message, encrypts it with the AES key, and sends the ciphertext to Bob.Bob receives the message: He takes the ciphertext, decrypts it using his matching AES key, and reads the plaintext.
 **Summary**
  After getting the output by feeding the S into Key derivative functions like HKDF OR SHA-256 we get the AES key (provides a key of a fixed, exact length of bits required by the algorithm (such as 128 or 256 bits for AES) in a fixed length or fixed length of strings FROM arbitrary randomness which is then used by both parties to incipher or encrypt and decipher or decrypt the message.

**Why HKDF is Preferred Over Raw SHA-256**
While your logic is correct for both, modern protocols prefer HKDF (HMAC-based Extract-and-Expand Key Derivation Function) over standard SHA-256 for two specific reasons:The "Extract" Phase: It extracts the entropy (randomness) from the raw secret \(S\) and strips away any remaining mathematical patterns.The "Expand" Phase: It stretches that randomness into the exact, uniform block size required by AES, ensuring no bits are mathematically weak.

## 1. The Vulnerability: The Man-in-the-Middle (MitM) Attack
Diffie-Hellman by itself is anonymous. It proves the math matches, but it does not prove who you are talking to. This allows a hacker (Eve) to sit in the middle of the connection [1].
## How the Attack Works

[Alice] <--- Key Exchange 1 ---> [Eve (MitM)] <--- Key Exchange 2 ---> [Bob]


   1. The Interception: Alice tries to do a DH(Diffie Hellman) exchange with Bob. Eve intercepts Alice's public key ($A$) and sends Alice her own fake public key ($E$) instead [1].
   2. The Double Exchange: Eve simultaneously does a separate DH exchange with Bob, sending Bob her public key ($E$) while intercepting Bob's public key ($B$) [1].
   3. The Two Keys:
   * Alice and Eve calculate shared secret S1 (turned into AES Key 1) [1].
      * Bob and Eve calculate shared secret S2 (turned into AES Key 2) [1].
   
## The Result
When Alice sends an encrypted message, Eve decrypts it with AES Key 1, reads or alters it, encrypts it again with AES Key 2, and forwards it to Bob. Alice and Bob think they are talking directly to each other securely, but Eve sees everything [1].
## The Fix
To stop this, Diffie-Hellman must be authenticated. Digital signatures or certificates (like RSA or ECDSA) are used alongside DH to prove Alice and Bob are truly who they say they are before the exchange begins.
------------------------------
## 2. The Defense: Perfect Forward Secrecy (PFS)
Perfect Forward Secrecy is a security property that ensures if a hacker steals a server's long-term master private key today, they still cannot decrypt any historical traffic they recorded in the past.
## How Diffie-Hellman Achieves PFS (Ephemereal DH)
To get PFS, protocols use ECDHE or DHE (the "E" stands for Ephemeral, meaning temporary).

   1. Unique Keys per Session: For every single new connection or login, Alice and Bob generate brand-new, completely random private keys (a and b).
   2. Quick Destruction: As soon as the session ends, Alice and Bob delete their private keys (a and b) and the resulting AES key from their device memory.
   3. The Hacker's Failure: If a hacker records your encrypted internet traffic today, and raids the server room one year later to steal the server's master identity key, it does not matter. The temporary private keys used to make your specific AES key were erased a year ago. The hacker cannot recalculate $S$ [1].

## 1. The Wireshark Perspective (Real-World Network Analysis)
When you capture a secure web connection using the Wireshark network protocol analyzer, you will see the exact terms from our discussion mapped onto network packets.
## Key Packet Labels to Scan For

* Client Hello: The very first packet sent by your browser. Inside the Extension: key_share field, you will see the raw bytes of your temporary public key $A$.
* Server Hello: The response from the website. It contains its own Extension: key_share field containing public key $B$.
* Cipher Suite: Inside the Server Hello, you will see a text string like TLS_AES_256_GCM_SHA384. This tells you that the final encryption uses AES-256, and the Key Derivation Function uses SHA-384.
* Application Data: Once the DH(Diffie Hellman) exchange completes, every packet after the handshake is labeled as encrypted Application Data. The raw numbers $S$, $a$, and $b$ never appear in Wireshark because they are never transmitted over the wire.
* 

------------------------------
## 2. The Threat: Quantum Computing and Shor's Algorithm
The entire security of Diffie-Hellman relies on the Discrete Logarithm Problem. This mathematical problem states that while it is incredibly easy to calculate $A = g^a \pmod p$, it is computationally impossible for a regular computer to reverse that calculation and find the secret exponent $a$ from the public key $A$.
## How Quantum Computing Breaks DH
A sufficiently powerful quantum computer will run Shor's Algorithm [1].

* The Superposition Trick: Unlike a classical computer that tests one key at a time, a quantum computer uses quantum bits (qubits) to evaluate all possible values of the secret exponent $a$ simultaneously.
* Instant Reversal: Shor's Algorithm solves the discrete logarithm problem almost instantly [1].
* The MitM Catastrophe: A hacker using a quantum computer can capture your public key $A$ from a Wireshark log, run Shor's Algorithm to extract your private key $a$, and recalculate the shared secret $S$ [1]. This completely destroys both your confidentiality and your Perfect Forward Secrecy.
* 

## The Global Fix: Post-Quantum Cryptography (PQC)
Because quantum computers threaten Diffie-Hellman, the National Institute of Standards and Technology (NIST PQC project) spent years standardizing new algorithms.
Instead of relying on prime number exponents, the world is moving to **Lattice-Based Cryptography** (such as **ML-KEM**, **formerly called Kyber**). These algorithms rely on geometric problems in thousands of dimensions that even quantum computers running Shor's algorithm cannot solve.

Diffie-Hellman is a Key Exchange protocol where both sides actively compute math to arrive at a mutual number.

By contrast, ML-KEM (Module-Lattice-Based Key Encapsulation Mechanism) is a Key Encapsulation Mechanism (KEM). Instead of mixing exponent numbers, it functions like a mathematically secure digital drop-box.
## 1. How ML-KEM (Kyber) Works Differently Than Diffie-Hellman
Diffie-Hellman is a Key Exchange protocol where both sides actively compute math to arrive at a mutual number.
By contrast, ML-KEM (Module-Lattice-Based Key Encapsulation Mechanism) is a Key Encapsulation Mechanism (KEM). Instead of mixing exponent numbers, it functions like a mathematically secure digital drop-box. 

[ Alice (Client) ]                                       [ Bob (Server) ]


        |                                                       |
        | ------ (1) Public Encapsulation Key (pk) -----------> |
        |                                                       |
        |                                              [Generates Symmetric Key]

        |                                              [Encrypts it into Ciphertext]
        |                                                       |
        | <----- (2) Ciphertext (ct) -------------------------- |
        |                                                       |
[Decapsulates ct using sk]                                      |
[Gets Symmetric Key]                                            |

## The Three Operational Steps

   1. Key Generation (KeyGen): Alice generates a **post-quantum private key (sk)** and a **public encapsulation key (pk)**. **She sends the public key to Bob**.
   2. Encapsulation (Encaps): Bob does not choose his own private exponent like in DH. Instead, his **computer generates a random symmetric key** and **uses Alice's public key to "encapsulate" (lock) it inside a unique ciphertext (ct)**. He sends this encrypted capsule back to Alice.
   3. Decapsulation (Decaps): Alice uses her secret private key to unlock the capsule and extract the exact symmetric key Bob generated. [1, 2, 3, 4, 5] 

## The Mathematical Shift
Diffie-Hellman uses large prime number exponents (g^a mod p), which Shor's algorithm easily reverses. 
ML-KEM relies on the Module Learning with Errors (MLWE) problem. It hides secret data inside matrices filled with thousands of equations containing deliberate, random "noise" or errors. Finding the secret key without knowing the exact grid location requires solving geometric problems in thousands of dimensions—a task that crushes both classical and quantum computers.
------------------------------
## 2. How Hybrid Quantum-Safe Connections Work Today
Because ML-KEM is relatively new compared to decades of tested mathematics, the cybersecurity industry refuses to rely on it alone. If a hidden math flaw is discovered in ML-KEM tomorrow, a purely post-quantum connection would instantly shatter.
To prevent this, browsers use a Hybrid Key Agreement.
## The Hybrid Mechanism
During a single handshake, your browser and the website execute both algorithms simultaneously:

   1. They do a classical Elliptic Curve Diffie-Hellman exchange (usually using the X25519 curve) to generate a classical secret.
   2. They run an ML-KEM encapsulation exchange alongside it to generate a quantum-safe secret.
   3. They feed both secrets into a Key Derivation Function (KDF) and merge them into one final, unified AES key.

[ X25519 Secret ]  +  [ ML-KEM Secret ]  --->  [ KDF ]  --->  [ Single AES Key ]

The Security Guarantee: The resulting connection is secure if either primitive holds. A hacker with a quantum computer cannot break the ML-KEM layer, and a hacker who finds a backdoor in ML-KEM is still locked out by the classical Diffie-Hellman layer.
## Current Real-World Deployment
This is no longer a pilot project; it is the production standard across global infrastructure: 

* Google Chrome: Google has integrated hybrid key exchange by default for desktop platforms. The specific standard used is X25519MLKEM768 (formally combining standard elliptic curve with NIST's FIPS 203 standard).
* Infrastructure Adoption: Major networks like Cloudflare have enabled this hybrid handshake by default across their edge servers, meaning a significant percentage of all global HTTPS traffic is already protected against future "harvest now, decrypt later" attacks.
* The 2029 Deadline: Google has established a strict internal engineering target to migrate all internal systems entirely to post-quantum safe structures.

## 1. Post-Quantum Digital Signatures (ML-DSA and Falcon)
In our previous discussion about the TLS handshake, we noted that the server must present a Digital Certificate and a Digital Signature to prevent a Man-in-the-Middle (MitM) attack.
Today, those signatures are generated using classical algorithms like RSA or ECDSA. Just like Diffie-Hellman, these algorithms rely on factoring and discrete logarithms, meaning a quantum computer running Shor's Algorithm will completely falsify them.
To prevent hackers from spoofing bank websites or software updates, NIST standardized new Post-Quantum Digital Signatures:
## The Standard: ML-DSA (Module-Lattice Digital Signature Algorithm)

* The Math: Formerly known as Dilithium, ML-DSA is built on the same lattice-based mathematics as ML-KEM.
* How it Works: To sign a document, the server proves it knows a secret vector within a high-dimensional grid without revealing the vector itself.
* The Trade-off: ML-DSA keys and signatures are significantly larger than classical ones. An ECDSA signature is tiny (64 bytes), while an ML-DSA-65 signature is around 2,400 bytes. This means internet packets during the handshake get larger, requiring optimization to prevent network slowdowns.

## The Alternative: Falcon

* The Feature: Falcon is another lattice-based signature standard. It produces much smaller signature sizes than ML-DSA, which makes network transmission faster.
* The Catch: The mathematics behind Falcon are incredibly complex and require highly precise floating-point calculations, making it much harder for engineers to implement safely in hardware and software without introducing bugs.

------------------------------
## 2. The Enterprise Challenge: Cryptographic Agility and Inventory
Migrating a massive global enterprise to post-quantum cryptography is the largest IT overhaul in human history. Organizations cannot simply flip a switch; they must achieve Cryptographic Agility—the ability to swiftly swap out encryption algorithms across millions of lines of code without crashing live systems.
To survive the transition, enterprises must follow a strict three-step framework:
## Step 1: Discovery (The Cryptographic Bill of Materials)
Before fixing anything, an enterprise must discover where its cryptography lives. Automated scanners crawl the network, source code, databases, and third-party software to build a CBOM (Cryptographic Bill of Materials). This inventory identifies:

* Every active digital certificate.
* Every hardcoded encryption library in legacy source code.
* Every data store using old algorithms (like AES-128 or Triple DES) to protect customer data.

## Step 2: Risk Prioritization
Not all data needs to be saved at the same time. Companies rank their assets based on vulnerability:

* Immediate Priority: Public-facing web servers and data pipelines transmitting high-value secrets (intellectual property, state secrets, financial data) that hackers might be recording today via "harvest now, decrypt later" attacks.
* Secondary Priority: Internal legacy databases that are locked behind strict physical and network firewalls.

## Step 3: Upgrading to Hybrid Architectures
Engineers modify their network stacks to support the same hybrid connections used by Chrome and Cloudflare. This ensures that old systems can still communicate using classical encryption, while newer systems gain instant, layered post-quantum protection.
------------------------------
## The Road Ahead
The global cybersecurity landscape is undergoing a massive shift. We have covered everything from the basic phrasing of $\phi(n)$ to the complex geometric math protecting our data from future quantum threats.



****Digital Siganture****
**Digital Signature Algorithm (DSA)
Elliptic Curve Digital Signature Algorithm (ECDSA)
RSA (RSA)** and others gives the ability to sign documents.

**Sign**
How to digitally sign a document?
1) First the message (An arbitrary size document - Document, contract- Long or Short) is converted into as such......
Message - **Hash Fuction**- Hash

3) Then we take our private key along with our hash value and take it through Digital signture alogorith to get the digital signature. So, we take a arbitrary size input and get a fixed output by a cryptographic hash function. Incase of Public key encryption 

Private Key + Hash Value - Digital signture alogorith - Digital Signature

**Verify Digital Signature**
1) Recipient **recieves** the **message** **and** the **digital signature**. Now we have to **run** the **document** through the **publically available hash function** to get a **hash value**. The document might be long so we have to collapse it into a short hash represntation.ble hash function  -  Hash Value

   Message+ Digital Signatire - Publically available hash function -  Hash Value
   
2) Then we take the **public key** of the person who signed the document and we take that they claim is their signature and we **decrypt** their **signature** with their **public key**. That should **output** the **same hash value** that we calculated using the document and the publically available hash function.

   Public key + Digital signature - Decrypt -  Same Hash Value

 Message/Document - publically Available hash function(Verification Algorithm) - Hash Value1 
 Public key + Digital signature - Public Key - Hash Value2
 If Hash Value1 = Hash Value2, then it is verified
The public keys are stored in a central registry

In conclusion:
A digital signature is created by hashing a document and signing the hash with the sender's private key. The recipient verifies the signature using the sender's public key and compares the resulting hash with the hash of the received document. If both hashes match, the signature is valid and the document's integrity and authenticity are confirmed.

**Web Authentication**
**Pass keys** or more technically it's an **implementation** of a **standard** called **web authentication**. And it turns out that these pass keys which are available on certain platforms and certain websites and ever more will be available soon quite shortly. They too rely on public and private keys as follows. You don't have to memorize a hard to guess password. You don't have to even store a hard to guess password in a password manager because pass keys eliminate passwords.
When you go to website or application you will be prompted not to add a user name or password, rather you will be asked to input your pass key. Pass key is something like a fingerprint or face scanning technology and these pass keys will be stored in a cloud storage for future use. Then the device will create a public key and private key for just that particular website, then it will send the public key and a user name or any piece of information which will sugest that it is infact you to the website. But we willnot send any password. And the private key will be stored in your own browser or some piece of software. And this private and public key will be unique to each website we log into and it will be created repeatedly but automatically for each website.
And next time we like to login to the previously logged in website. The website will send a randomly generated challenge (a word, number a liitle message) that the website would like us to sign digitally. To digitally sign it we will need the pass key, the challenge and the private key through the digital signature algorithm to get the signature. Then finally the website will use our stored public key to decrypt the signature to hopefully get the same challenge value.
It doesn't require us to remember passwords but it does require though that we don't lose the device or the devices that registered for these websites or apps. But again, increasingly is the world uh providing cloud services whether it's with Apple or Microsoft or Google or others that presumably can synchronize your pass keys across devices.

Private key + Challenge - Digital Signature Algorithm - Signature

**One-Sentence Summary**
Passkeys replace passwords by generating a unique public/private key pair for each website. The website stores only the public key, while the private key remains on the user's device and is used to digitally sign login challenges that the website verifies using the stored public key.

**Encryption In Transit**
end to end encryption. This is a stronger guarantee whereby you can trust that Alice's connection to Bob is in fact secure. Even if, not pictured here, there are one, two, three, four machines in the middle, companies in the middle, eavesdroppers in the middle.
iMessage for Apple users and WhatsApp internationally is known in particular for offering end toend encryption which if implemented truthfully and technically correctly should guarantee that even though your messages might be going through WhatsApp servers no employee at WhatsApp can actually see your messages because it's encrypted all the way from A to B even though it's going through a potential potential eavesdropper but that depends on exactly what form of encryption you're using and if it's not endtoend it might only be encrypted in transit such that ees that eavesdropper might indeed have access to the data.
somewhat older but large hard drive that can store lots and lots of files and folders or perhaps something smaller known as a solidstate drive
But when you delete a file by emptying the trash or recycle bin, the computer just eh forgets where it is. And more importantly, it frees up the space so it can be used later. So what do I mean by that? Well, suppose I do go ahead and delete a file and empty the recycle bin or trash can. And suppose that these yellow zeros and ones represent the file that I no longer care about. Well, what's actually going to happen underneath the hood, so to speak, of the computer? Well, eventually some of those yellow zeros and ones might just get reused for other files. In other words, these zeros and ones highlighted in yellow represent a file that used to be there but is not.
**Securely Delete**
So what we can do when securely deleting a file is something like this. Change all of the zeros and ones that we don't care about anymore or want. Change them all to zeros. And this will effectively securely delete the file because now the ones that were previously there that represented some piece of information are just completely gone. Or equivalently, I could change them all to ones. Or I could even change it to random zeros and ones. The point is to securely delete a file. You should change all of the zeros and ones to at least some other pattern so that the file is effectively gone. 

**[Encryption at Rest] use full disk encryption**
some operating systems nowadays support what's called **full disk encryption**. And this is good for a number of reasons. One, if you enable a feature called full disk encryption, which is actually a specific incarnation of an idea known as **encryption at rest**. **Encryption in transit refers**, of course, to your data going back and forth from point A to point B. **Encryption at rest** means it's just sitting there on your device in your pocket or on your lap or on your desktop uh sitting unused, maybe on or off. So when it comes to full disc encryption or encryption at rest, you ideally want all of your data somehow encrypted on your Mac, on your PC, on your phone. And only when you log in with your password or maybe your fingerprint or your face should that data be decrypted automatically.
And this can be hap this can happen pretty darn fast nowadays with modern hardware should the data be unencrypted. So you can actually use it and interact with that device. 
 So in other words, if this is my unencrypted data, the way I want it and need it when I'm using my computer, full disk encryption at rest would change my entire computer to look random.
So, if someone steals my device, as long as i am having best pratcices, as long as i have encrypted all data and it will only be decrypted with my face id, finger print or pin code, the data will not be stolen. Only the device may be sold. These are random zeros and ones now that I generated by using, for instance, my password or my fingerprint or my face. 
But they're smart enough thanks to software known as **firmware** inside of it. As soon as the device realizes, wait a minute, that those bits over there aren't working properly anymore, the device might not let you change them to all zeros or all ones or a random zeros and ones anymore. It might just leave them as is forever. Which is to say, it's even more important to start using full disc encryption, encryption at rest, when you first get a device because that way you can trust that even if parts of the device degrade over time, all of the data that's there and has been there was at least encrypted with one of your pass code passwords or one of your biometrics in the past.
**Downside: Ransomeware**

Your analysis perfectly captures the fundamental reality of modern hardware security. Full Disk Encryption (FDE) changes the entire physics of device theft: it turns a catastrophic data breach into a simple, line-item equipment loss.
When you activate features like BitLocker (Windows), FileVault (macOS), or the file-based encryption on your smartphone, you are executing high-speed, hardware-accelerated symmetric encryption (typically AES) across your entire storage drive.

Here is a deeper look at the exact mechanics of what you described, focusing on the firmware behavior and the critical ransomware downside.
------------------------------
## 1. The Wear-and-Tear Paradox: Bad Sectors & Firmware
You raised an excellent technical point about device degradation. Flash storage (SSDs and phone storage) degrades over time. When a sector of the drive goes bad, the storage device's internal firmware locks that sector down into a "Read-Only" state to prevent data corruption.
## If you set up FDE on Day 1:
Every single piece of data written to that drive—even the data written to sectors that eventually fail and freeze—is completely scrambled into random-looking bits. If a hacker desolders the storage chip to read those frozen, bad sectors directly, they only get encrypted garbage.
## If you set up FDE Later:
If you use a laptop unencrypted for a year, delete some private files, and then turn on encryption, those degraded blocks might have already frozen in a Read-Only state while holding your old, unencrypted data. FDE cannot encrypt a sector that the firmware has marked read-only. Setting up encryption on day one guarantees total coverage.
------------------------------
## 2. The Dark Side: How Ransomware Exploits Encryption at Rest
While Encryption at Rest is your best defense against physical thieves, it is simultaneously the ultimate weapon for digital thieves via Ransomware.
Ransomware does not care about stealing your data to read it; it cares about stealing your access to it. It weaponizes the exact same math that keeps you safe.
## The Ransomware Attack Sequence

[Hacker Malware] ---> [Invades OS] ---> [Generates Asymmetric/Symmetric Key Pair]
                                                     │
                                                     ▼
[Your Plaintext Files] ───────────────────> [Malware Encrypts Them]
                                                     │
                                                     ▼
                                      [Your Files Become Unreadable]


   1. The Intrusion: The malware bypasses your perimeter and gains access to your operating system.
   2. The Mathematics: Because you are logged into your device with your Face ID, PIN, or password, the operating system has already decrypted your FDE drive. The malware can see all your files in plain text.
   3. The Double Encryption: The malware runs its own encryption routine. It reads your unencrypted files, encrypts them using the hacker's key, writes the new scrambled file to your drive, and deletes your original copy.
   4. The Extortion: Your device is still in your physical possession, but your data has been transformed into random zeros and ones that you cannot decrypt, because you do not own the matching private key.

## Summary: Physical vs. Logical Encryption

* Full Disk Encryption protects your data from Physical Attacks (someone stealing your laptop while it is turned off).
* Ransomware exploits your Logical Access (attacking your data while the machine is on, unlocked, and actively running).

To round out your understanding of data security, I can show you how a robust 3-2-1 backup strategy completely neutralizes the threat of ransomware, or we can look at how TPM (Trusted Platform Module) chips securely store your FDE keys in hardware. Which area should we tackle next?

## 1. The Ultimate Shield: The 3-2-1-1-0 Backup Strategy
Since ransomware weaponizes encryption against you, paying the ransom is highly discouraged. Instead, you defeat ransomware by ensuring you can completely wipe your device and restore your data from an uninfected source.
The industry standard to guarantee recovery is an evolution of the classic 3-2-1 rule: the 3-2-1-1-0 backup strategy.

                         [ Your Live Data ]
                                 │
         ┌───────────────────────┴───────────────────────┐
         ▼                                               ▼
[ Production Copy ]                             [ 2 Different Media Types ]
(On your local device)                           (e.g., Internal SSD + External HDD)
                                                         │
                                 ┌───────────────────────┴───────────────────────┐
                                 ▼                                               ▼
                        [ 1 Offsite Copy ]                             [ 1 Immutable/Air-Gapped ]
                         (Cloud Storage)                                (Offline Disconnected Drive)
                                                                                 │
                                                                                 ▼
                                                                        [ 0 Errors / Testing ]
                                                                        (Regular restore drills)

## Breakdown of the Strategy

* 3 Copies of Data: Maintain your production data and at least two distinct backup copies.
* 2 Different Media Types: Store your backups on different physical media (e.g., one on a local external hard drive, one in the cloud) to prevent a single hardware failure from destroying both.
* 1 Offsite Location: Keep one copy outside your physical building (usually via secure cloud backup providers like Backblaze, AWS, or OneDrive) to protect against fire, theft, or natural disasters.
* 1 Immutable or Air-Gapped Copy (The Ransomware Killer): Modern ransomware scans your local network to find and encrypt connected backup drives. To stop this, one backup must be Air-Gapped (physically disconnected from the internet and power when not in use) or Immutable (cloud storage locked with Object Lock, preventing anyone—even you—from deleting or modifying the files for a set period).
* 0 Errors: Regularly test your restores to ensure your backups actually work when a crisis hits.

------------------------------
## 2. How TPM Chips Protect Your Full Disk Encryption Keys
When you turn on your computer, how does Full Disk Encryption know it can trust your machine to decrypt the hard drive? It relies on a dedicated security chip soldered directly onto your motherboard called the TPM (Trusted Platform Module). On Apple devices, this functionality is handled by the Secure Enclave.
The TPM prevents hackers from simply pulling your hard drive out of your laptop, sticking it into another computer, and reading your data.
## The Boot Process and "Measured Boot"
The TPM acts as a security gatekeeper during the boot process using a series of registers called PCRs (Platform Configuration Registers).

[ Power On ] ──> [ Bios/UEFI Checked ] ──> [ OS Kernel Checked ] ──> [ TPM Releases Key ] ──> [ OS Boots ]
                       │                         │
            (PCR Hash Generated)      (PCR Hash Generated)


   1. The Measurements: When you turn on your PC, the motherboard measures (hashes) the firmware, the BIOS settings, and the operating system kernel boot files.
   2. The Comparison: It stores these hashes inside the TPM's PCR registers.
   3. The Unsealing: The actual Master Encryption Key for your hard drive is wrapped (sealed) inside the TPM chip. The TPM will only release the key to unlock your drive if the current system measurements perfectly match the trusted baseline.
   4. The PIN/Biometric Layer: Once the TPM verifies the hardware hasn't been altered, it prompts you for your PIN, Windows Hello Face ID, or fingerprint. Combining the valid hardware state with your correct credentials unlocks the Master Key from the TPM, allowing the operating system to decrypt the drive in real-time.

## Why This Matters
If a thief steals your laptop, opens the case, and attempts to attach a hardware sniffer to intercept data, or tries to boot your computer into a malicious hacker operating system, the system measurements will change. The TPM will immediately notice the altered PCR hashes, refuse to release the encryption key, and lock down the drive completely.

## 1. How to Verify TPM and Secure Enclave Status
Here is how to check if your operating system is actively using its hardware security module to protect your full disk encryption keys.
## On Windows (Checking TPM and BitLocker)

   1. Press the Windows Key + R to open the Run dialogue box.
   2. Type tpm.msc and press Enter.
   * What to look for: A window will appear showing your TPM status. It should say "The TPM is ready for use" and display Specification Version 2.0.
   3. Next, open the Start Menu, type cmd, right-click Command Prompt, and select Run as administrator.
   4. Type manage-bde -status and press Enter.
   * What to look for: Look at the Key Protectors line. It should ideally say "TPM" or "TPM And PIN", confirming your encryption key is locked inside the security chip.
   
## On macOS (Checking Secure Enclave and FileVault)

   1. Click the Apple Menu () in the top left and select About This Mac (or System Settings -> General -> About).
   2. Click System Report... to open the hardware layout view.
   3. Click on Hardware -> Controller (or Security on older Intel Macs).
   * What to look for: On modern Apple Silicon Macs (M1/M2/M3/M4), you will see information regarding the Apple Fabric or Security chips. On Intel Macs, it will display the Apple T2 Security Chip, which houses the Secure Enclave.
   4. To check encryption, go to System Settings -> Privacy & Security -> FileVault and ensure it says "FileVault is turned on".

------------------------------
## 2. Comprehensive Cryptography & Security Checklist
We have traced a massive arc from the absolute foundations of mathematical notation to the bleeding edge of quantum-safe hardware infrastructure. Here is a scannable summary of everything we covered:

* Mathematical Foundations: Spelled out $\phi(n)=(p-1)(q-1)$, the foundational Euler's totient formula used to generate key pairs in RSA cryptography.
* Diffie-Hellman (DH): Identified it strictly as an asymmetric key exchange protocol. It allows two parties to create a mutual secret number ($S$) over an insecure network without transmitting the secret itself.
* Key Derivation (KDF): Mastered how the raw secret number ($S$) is put through functions like HKDF or SHA-256 to output a uniform, mathematically unbiased AES key of a fixed length (128 or 256 bits).
* The MitM Threat: Explored how anonymous DH can be intercepted by a Man-in-the-Middle, requiring digital signatures and certificates to authenticate identities before the exchange.
* Perfect Forward Secrecy (PFS): Explained how Ephemeral DH protects past traffic by generating temporary keys for every session and immediately destroying them when the session closes.
* Network & Quantum Eras: Examined how these handshakes appear as ClientHello and ServerHello packets inside network tools like Wireshark, and how quantum computers running Shor's Algorithm threaten them.
* Post-Quantum Transition: Explored the new lattice-based standards like ML-KEM (key encapsulation) and ML-DSA (digital signatures) that resist quantum attacks, and how browsers deploy them right now using hybrid frameworks.
* Encryption at Rest vs. Ransomware: Broken down how Full Disk Encryption protects physical devices from day one by leveraging TPM/Secure Enclave chips to measure boot files. Finally, we looked at how ransomware exploits an already unlocked system, proving the vital need for a decoupled 3-2-1-1-0 backup strategy.







**Now that you have mastered the entire pipeline from raw math to hardware-level data defense, you are well-equipped to audit your own digital footprint. Would you like assistance configuring a specific cloud backup provider to support immutability, or do you want to explore how passkeys fit into this biometric architecture?**

\






**full disk encryption** == **encryption at rest**

**Ransomeware**
It's not uncommon nowadays for hackers, for adversaries when they get into a system, whether it's your laptop or for instance a corporate network or in some cases hospital systems or cities own computer networks to not try to do any damage or just do something like spam or cryptocurrency mining, but to actually uh encrypt all of the data on these systems they somehow accessed online. Why? Well, if they encrypt all of the data, they can then ask for a ransom and say, "Listen, if you don't give me this many bitcoins, I'm not going to give you the key that I use to encrypt your data.

**Quantum Computing**
Data more generally, now typically in our world now a bit a binary digit can either be a zero or it can be a one. In the world of quantum computing thanks to some very fancy physics and quantum mechanics in particular. It is possible it seems physically for us to implement the idea of bits a little bit differently using quantum techniques.
A quantum bit or Qbit whose power derives from the reality that physically you can implement a **Qbit** in such a way that it is **representing both a zero and a one** at the exact same time. So it can be not in just one state, so to speak, one condition at once, but two states at once.
And if you have two cubits, they can be in four states at once. If you have three, they can be in eight states at once. If you have 32 of them, they can be in four billion states at once.
Well, when we talk about cryptography, when we talk about hashing, when we talk about just very large numbers and trying to figure out via brute force or some other mechanism what some input to a function was, if you have exponentially more computing capabilities by not being able to do one or two things at a time with individual bits, but two or four or eight or 4 billion things at once, it stands to reason that if adversaries have access to quantum computing, before you and I do, then all of the security you and I now rely on that we've talked about today could suddenly become insecure because we're trusting right now that it's just going to take the adversary a lot a lot a lot of time, maybe money, maybe resources, maybe risk to attack our accounts. But if they have exponentially more resources than you and me, then our data really is at risk and all of the mathematics we've been trusting need to be hardened instead.


**Securing Systems**

**Encryption** is the building block to help us protect our systems too.
Securing Systems**Wifi**
**Wi‑Fi Protected Access (WPA)
Wi‑Fi Protected Access II (WPA2)
Wi‑Fi Protected Access III (WPA3)**
When: phone, laptop, tablet connects to a Wi-Fi access point, encryption is used between your device and the wireless router.

 Well, hopefully you're using among the latest versions of this Wi-Fi protected access or WPA. And so, in general, whenever you configure a phone or whenever you configure a laptop or desktop, ideally you're connecting to a device nowadays that supports this technology and the latest version thereof.
 And in a nutshell, what that ensures is that indeed your traffic from your phone, laptop or desktop is somehow scrambled between you and that other device. And that device in turn is probably connected to devices called routers.
 Computers that route left, right, up and down information on the internet, which might then connect to other routers it finally reaches its destination. 

**Man-in-the-Middle (MITM) Attack**
If **Alice(User)** is sitting with her phone, laptop or desktop and trying to visit some website represented by **BOB(web server)**, There could be a third party eve who could be evesdroping on thier conversation(traffic) of evry request Alice is making and every reply Bob is sending. Tge attackers can not only see but also manupulate the request and reply if the systems are not using some type of encryption.

<!DOCTYPE html>
<html>
<body>
</body>
</html> if this is the reply coming from a web server back to aweb browser an attcker can add additional html code[<script src = "ad.js"></script>] into the web pages that Alice is downloading. Example = ad.js is used to inject advertisment.

**Eve can Read traffic, Alter traffic and Inject malicious information/content, forward altered message**

**How HTTPS Prevents This**
Today most websites use: Hypertext Transfer Protocol Secure
HTTPS uses: Transport Layer Protocol(TLS) to encrypt communications between: Browser ⇄ Website

[**A Man-in-the-Middle (MITM) attack occurs when an attacker secretly intercepts and potentially modifies communications between two parties. Encryption technologies such as WPA for Wi-Fi and HTTPS/TLS for web traffic help prevent eavesdropping and tampering by ensuring confidentiality, integrity, and authentication of data.**]

**Packet Sniffing**
Packet sniffing is the process of **capturing and examining network packets (small units of data)** as they travel **across a network**.

**Large Message
      ↓
Broken into Packets
      ↓
Sent Across Network
      ↓
Reassembled at Destination**

[**Each packet contains:**]: Source IP address, Destination IP address, Protocol information, Actual data (payload)

[**Legitimate Uses**]: Network Administrators use packet snififng to do: Troble shooting netwoek problem, Monitor network performance, Examining network security, examine protocols.
Examples of tools: Wireshark, tcpdump

[**Malicious Uses**] Attackers use packet sniffing to: Detect usrname and password, Emails, session cookies[A session cookie is a small piece of data that a website stores in your browser to identify you after you log in. Without session cookies, you would have to enter your username and password on every page you visit.], sensitive information especially when traffic is not encrypted.
Using HTTPS rather tha HTTP: Attacker can see: Source IP Adrress, Destination IP Adrress, Packet Size and Timing Information
GET /search?q=cats HTTPS/3

[**Packet sniffing is the process of intercepting and analyzing network packets transmitted across a network. It is commonly used for network troubleshooting and monitoring but can also be used maliciously to capture sensitive information from unencrypted communications.**]

**If someone is performing an attack right from a machine in the middle, does the person actually have to be like connected to the same Wi-Fi network as you or they could be on a whole other network?**
So in general they would be connected to the same Wi-Fi network so that they are uh in general they would be connected to the same Wi-Fi network but even that is not necessary so long as they are within a reasonable proximity to you and their laptop or their device has an antenna that can receive all of the wireless packets that are around you. They don't necessarily have to have access to that same network especially if it's unencrypted. And in fact there exists software that can listen to all possible networks that are around you.

**Cookies**
When you actually visit a website for the first time, particularly one that you need to log into and therefore that needs to remember you when you click on different pages, for instance, to access different emails, add different things to your shopping cart. What the server actually does is a little something like this. The server responds to your request, for instance, after logging in with an HTTP response that first says 200, which is code for okay. It's a so-called status code, similar in spirit to the 404 you might have seen in the real world, but 200 means okay.
HTTP/3 200
And then it additionally sends this line of text inside of a virtual envelope that gets sent back to you.
Set-Cookie: session=1234abd

Subsequently when your browser visits the website again and again, it sends its own message like  Cookie: session=1234abd  but it is not set-cookie - this is the textual equivalent. But first it sends GET HTTP/3 200  -  Getting the home page of the server. This in conclusion does the solve the problem of retaining a state but they make us vulnerable to session hijacking if you are not using HTTPS. As by using HTTPS the attackr willnot see any message or cokie session as it will be encrypted.

**TLS and Certificate** (SSL is older version of TLS)
TLS is a protocol which works on encrypting HTTP. So what does it do? It turns out that it lies on public key cryptography/ asymetric cryptography. And this principle that if you give two parties A and B each thier own public key and private key you can communicate securely even if in advance you dont have a shared secret. As it allows us to establish a secure connection even though we have never visited some website or app before to communicate securely to a web server.
So, by using **TLS it is using a digital certificate**. So, the **certificate means a public key** which has been signed by someone else. So, the website has a public key and a private key - the private key as always stays private. But in this case **the web server** has a **public key** that has been **signed by some third party(companies)**. These **certificates are a type of CALLED X.509** (The standard formate in which the certificate lives). The certificate has - the name of the website, the public key, how long the certificate is valid for(validity of the website).

**Certificate Authority(CA)**
These are the collection of companies and etities whose sole purpose in the world is to do digital signature in these certificates. And the various browser manufacturers like apple, microsoft, google, mozilla and othrers has a list of this CAs in thier browsers like edge, firefox, chrome who they trust. So, if i trust google, microsoft, mozilla or google so in transitivity i should also trust those CAs that the browser manufacturers trust.
So, what happens when a browser visits a website/ **1)** It first downloads the certificate assuming i am using HTTPS. **2)** Now the browser calculates a **hash value** for that certificates by looking at certain fields within it, using a certain hash function that produces a fixed lenghth of represenation of the **certificate**. **3)** It then looks at the signature on that certificate and it then uses the certificate authoirty (the pulic key) who signed the certificate and now in conclusion it uses the signature from that server certificate and the CAs Public key - runs it through a algorithm - then decrypting the signature with the public key, and that should produce the exact same hash value. And taht should produce the exact same hash value.

Your breakdown of the Certificate Authority (CA) ecosystem and the signature verification process is remarkably accurate. You have correctly identified the core principle of transitive trust and the exact mathematical steps a browser takes to verify a website's identity.
Let's refine and solidify the exact steps of that verification process to ensure every detail is technically perfect.
## 1. The Trust Anchor (Transitive Trust)
You are exactly right about how trust works on the internet.

* You trust your operating system or browser vendor (Apple, Google, Microsoft, Mozilla).
* These vendors maintain a Root Store—a built-in list of pre-installed Public Keys belonging to trusted Certificate Authorities (like DigiCert, Let's Encrypt, or GlobalSign).
* By trusting the browser, you transitively trust any certificate that has a valid signature tracing back to one of those built-in root keys.

------------------------------
## 2. The Verification Math (Step-by-Step)
When your browser connects via HTTPS and downloads the website's certificate, it performs a brilliant "double-check" using asymmetric math to ensure the certificate hasn't been tampered with.

[ Downloaded Server Certificate ]
  ├── 1. Read Certificate Data ───> [ Hash Function ] ──> [ Hash A ]
  │
  └── 2. Extract CA's Signature ──> [ CA Public Key ] ──> [ Hash B ]
                                                              │
                                                   (Must Match Exactly!)

## Step A: The Browser's Independent Calculation
The browser looks at the raw data fields of the certificate (the website's domain name, the expiration date, its public key, etc.). It runs all of this plaintext data through a hash function (like SHA-256) to generate Hash A.
## Step B: Unlocking the CA's Signature
The certificate also contains a block of encrypted data called the Digital Signature. This signature was created by the CA using the CA's strictly guarded Private Key.

   1. The browser finds the CA's name on the certificate.
   2. It pulls that specific CA's Public Key out of its built-in Root Store.
   3. It uses that Public Key to decrypt (or mathematically verify) the signature.
   4. The output of this decryption reveals the original hash that the CA calculated when it first approved the site: Hash B.

## Step C: The Ultimate Match
The browser compares Hash A (what it calculated itself) with Hash B (what the CA signed).

* If they match perfectly: The browser knows two things with absolute certainty:
1. The certificate was genuinely signed by that specific trusted CA.
   2. Not a single letter or bit of the website's data has been altered or tampered with since the CA signed it.
* If they do not match: The browser completely blocks the connection and throws a massive warning screen (like "Your connection is not private").

------------------------------
## A Crucial Real-World Addition: The Certificate Chain
In the real world, big Root CAs rarely sign website certificates directly because it is too risky to keep their master private keys active online. Instead, they use a Certificate Chain:
$$\text{Root CA (In Browser)} \longrightarrow \text{Intermediate CA} \longrightarrow \text{Website Certificate (e.g., Google.com)}$$ 
When your browser performs the verification steps you described, it actually loops through this process a few times. It uses the Root CA's public key to verify the Intermediate CA, and then uses the Intermediate CA's public key to verify the final website.











































































 


