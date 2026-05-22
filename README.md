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
**Credential stuffing**. A credential is something like a username and password. Um refers to the process of an adversary having found a whole bunch of usernames and passwords, maybe online, maybe in some database that they or someone else attacked and posted for the whole world to download. Credential stuffing means not using dictionaries, not using brute force, but just literally using a list of already known usernames and passwords, maybe from some other application or website to try to stuff them into a different website to see if well maybe if David's using this username and password over here with high probability he's probably using the same username and password over here. So credential stuffing is the threat that I dare say many of you are vulnerable to.
**social engineering**
**Phishing**: Fishing is all about trying to use social engineering, in this case in a technical way to try to convince you through very convincing looking emails and even websites that it is a legitimate email from paypal.com or it is a legitimate email from a politician or it is a legitimate email or request from a teacher here at Harvard, but it's not.
Well, you should minimally be looking at the URL bar and making sure that it is gmail.com or probably google.com or whatever google.country code depending on where you live in the world. Making sure that it looks legitimate and that you've actually been there before.
**Machine in the middle attack**: if you're on the internet, there are, suffice it to say, many other machines on the internet very often between you and whatever website or app you are visiting. Often those machines might be things like routers, uh, servers that internet service providers, companies, universities, maybe even your own home owns and controls, but all of your data is passing through those machines in the middle, so to speak. If any of them are malicious and are maybe storing your data, looking at your data, it's possible that you might not be having secure communications with the other end unless you are using certain defenses.
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
You can still use a dictionary for instance of
01:30:27.280 English words or better yet a dictionary of English fruits and you could one
01:30:32.719 fruit at a time run each of those values as input into the same hash function the
01:30:38.320 library or code that you're using to achieve this and then that's going to give you one hash value after another
01:30:44.560 and you could compare each of those hash values against whatever is in the database or the file of passwords that
01:30:50.719 you the hacker in the story might have actually stolen somehow. You have to do more work though because it's no longer
01:30:57.040 as simple as just comparing apple against apple and banana against banana. You actually have to do some work. You
01:31:03.520 have to do some computational work.
**Brute Force**
the adversary re resort to brute force
01:31:28.159 attacks and you can try even the simplest of passwords like 000000
01:31:33.280 or maybe eight zeros instead. And you can hash that and see what the resulting hash value is and compare that against
01:31:39.679 what's in the database. Then you could try 000000 00001
01:31:45.360 hash that compare that against what's in the database and then move on to the next and the next. Doing this not just
01:31:50.719 for numbers but for letters as well.
**Rainbow Table**
 There's a term of art known as a rainbow table which is a very beautiful way of saying that adversaries in
01:32:22.880 advance might have already hashed all possible English words in a dictionary. adversaries might have already hashed
01:32:29.679 all possible passwords of length four or five or six or seven or eight or something else. And maybe if they have a
01:32:36.080 big enough hard drive, they are storing a big table like an Excel file or a CSV file of all of the words that they've
01:32:43.440 tried, all of the passwords they've tried and all of the hash values they've already computed. Then it's even easier.
01:32:49.920 Then they don't even need to do a brute force attack per se, hashing and hashing and hashing and hashing. Then they can
01:32:55.760 just compare, compare, compare because indeed a rainbow table simply contains all of the passwords they've tried, all
01:33:02.239 of the hash values they've generated. And so they just compare left to right whatever the user typed in against the
01:33:08.880 hash value they've already computed. Now for certain hash functions, this threat of a rainbow table is just not feasible.
01:33:16.320 You might need terabytes or pabytes of data, which means a lot of hard drives
01:33:21.679 and a lot of money. So there are potential downward pressures on this kind of an attack, but it can certainly
01:33:27.440 speed things up.
**Salting**
salt isn't something that's meant to be private or secret or secure. It's just sprinkled in there to make sure that whatever hash value comes out of this black box is a little bit different than if you had put a different salt value instead.
Different users should have different salt values just in case they choose the same passwords.
The salt is actually stored in the hash value itself according to this algorithm in the first two characters. The next time Carol logs in, she types in her username, Carol, and hits enter. The server now knows, okay, I'm expecting a password from Carol. Let's see what she types in. Suppose that she types in correctly. Cherry. Now, the system is not storing Cherry. So, it's not going to compare literally what Carol typed in. But it is going to hash Cherry. But first, the system's going to check what is Carol's salt, and it's going to infer as much by looking at Carol's hash value and looking only at the first two characters by convention. Then what the server is going to do, it's going to take whatever Carol typed in, cherry, c h e r r y, it's going to pass in 50, and then hopefully it's going to get back this same value here, this whole string in yellow. And if those are correct, then the carol will be considered authenticated. By contrast, if the username happens to be Charlie and Charlie hits enter, then what the server is going to do is look at Charlie's hash value, grab the first two characters for Charlie's salt, use that salt and cherry as the input to the hash function, and hope that the result is Charlie's value, not Carol's.

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
A key is what sort of unlocks the capabilities of this cipher, but it's a key that needs to be known and used not only by you typically, but also by the recipient. So that by having copies of the same key, you can not only encrypt messages or incipher them, but you can also decrypt or decipher those messages, too.

**Secret Key Cryptography** 
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

Common choice:
e=65537
For this small example:
e=17

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
d×e≡1(mod3120)

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
e^−1 modϕ(n)
So: d=17^−1 mod3120

**Other Key Exchange**
**Diffie Hellman** [**Diffie–Hellman itself does not encrypt data. It is a key exchange algorithm used to create a shared secret, which is then used by a symmetric encryption algorithm such as Advanced Encryption Standard to encrypt the actual messages.**]
First we take a number **g** which is the generator which can be anything like **2 for instance**and then we pick a really big prime number **p** and those are agreed upon in advance and now person **A** picks another really big prime number **a** and then we do the mathematical calculation ie., **g** to the power of **a** **mod** **p**. Meanwhile,**B** or Bob still uses the same **g**, still uses the same **p**, picks his own private key called **b** and raises **g** to the power of **b** **modulo** **p** and that gives him back this value capital **B**. And now Alice and Bob can send those values across the inetrnet **A and B** and thaxs to some modular arithmathic here too.

A = Alic's Public Key
B = Bob's Public Key
g = generator
a = A's private key
b = B's private key
p = Really big prime number

**A = g^a mod p
B = g^b mod p**

Now Alice can take bob's **B** value and raise it to the power of **a**, which effectively gives you **g** to the power of **a** times **b** **mod** **p**. Bob meanwhile can take the value **A** raise it to the power of it's own private key **b** than mod **p**

**s(A) = B^a mod p
s(B) = A^b mod p**

S = g^a*b mod p

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
Recipient recieves the message and the digital signature. Now we have to run the document through the publically available hash function to get a hash value. The document miht be long so we have to collapse it into a short hash represntation. Then we take the public key of the person who signed the document and we take that they claim is their signature and we decrypt their signature with their public key. Taht should output the same hash value that we calculated using the document and the publically available hash function.

 Message/Document - publically Available hash function(Verification Algorithm) - Hash Value1 
 Public key + Digital signature - Public Key - Hash Value2
 If Hash Value1 = Hash Value2, then it is verified
The public keys are stored in a central registry

In conclusion:
A digital signature is created by hashing a document and signing the hash with the sender's private key. The recipient verifies the signature using the sender's public key and compares the resulting hash with the hash of the received document. If both hashes match, the signature is valid and the document's integrity and authenticity are confirmed.

**Web Authentication**
**Pass keys** or more technically it's an **implementation** of a **standard** called **web authentication**. And it turns out that these pass keys which are available on certain platforms and certain websites and ever more will be available soon quite shortly. They too rely on public and private keys as follows. You don't have to memorize a hard to guess password. You don't have to even store a hard to guess password in a password manager because pass keys eliminate passwords.
When you go to website or application you awill be prompted not to add a user name or password, rather you will be asked to input your pass key. Pass key is something like a fingerprint or face scanning technology and these pass keys will be stored in a cloud storage for future use. Then the device will create a public key and private key for just that particular website, then it will send the public key and a user name or any piece of information which will sugest that it is infact you to the website. But we willnot send any password. And the private key will be stored in your own browser or some piece of software. And this private and public key will be unique to each website we log into and it will be created repeatedly but automatically for each website.
And next time we like to login to the previously logged in website. The website will send a randomly generated challenge (a word, number a liitle message) that the website would like us to sign digitally. To digitally sign it we will need the pass key, the challenge and the private key through the digital signature algorithm to get the signature. Then finally the website will use our stored public key to decrypt the signature to hopefully get the same challenge value.
It doesn't require us to remember passwords but it does require though that we don't lose the device or the devices that registered for these websites or apps. But again, increasingly is the world uh providing cloud services whether it's with Apple or Microsoft or Google or others that presumably can synchronize your pass keys across devices.

Private key + Challenge - Digital Signature Algorithm - Signature

**One-Sentence Summary**
Passkeys replace passwords by generating a unique public/private key pair for each website. The website stores only the public key, while the private key remains on the user's device and is used to digitally sign login challenges that the website verifies using the stored public key.

**Encryption In Transit**
end toend encryption. This is a stronger guarantee whereby you can trust that Alice's connection to Bob is in fact secure. Even if, not pictured here, there are one, two, three, four machines in the middle, companies in the middle, eavesdroppers in the middle.
iMessage for Apple users and WhatsApp internationally is known in particular for offering end toend encryption which if implemented truthfully and technically correctly should guarantee that even though your messages might be going through WhatsApp servers no employee at WhatsApp can actually see your messages because it's encrypted all the way from A to B even though it's going through a potential potential eavesdropper but that depends on exactly what form of encryption you're using and if it's not endtoend it might only be encrypted in transit such that ees that eavesdropper might indeed have access to the data.
somewhat older but large hard drive that can store lots and lots of files and folders or perhaps something smaller known as a solidstate drive
But when you delete a file by emptying the trash or recycle bin, the computer just eh forgets where it is. And more importantly, it frees up the space so it can be used later. So what do I mean by that? Well, suppose I do go ahead and delete a file and empty the recycle bin or trash can. And suppose that these yellow zeros and ones represent the file that I no longer care about. Well, what's actually going to happen underneath the hood, so to speak, of the computer? Well, eventually some of those yellow zeros and ones might just get reused for other files. In other words, these zeros and ones highlighted in yellow represent a file that used to be there but is not.
**Securely Delete**
So what we can do when securely deleting a file is something like this. Change all of the zeros and ones that we don't care about anymore or want. Change them all to zeros. And this will effectively securely delete the file because now the ones that were previously there that represented some piece of information are just completely gone. Or equivalently, I could change them all to ones. Or I could even change it to random zeros and ones. The point is to securely delete a file. You should change all of the zeros and ones to at least some other pattern so that the file is effectively gone. 

**Encryption at Rest**
some operating systems nowadays support what's called **full disk encryption**. And this is good for a number of reasons. One, if you enable a feature called full disk encryption, which is actually a specific incarnation of an idea known as **encryption at rest**. **Encryption in transit refers**, of course, to your data going back and forth from point A to point B. **Encryption at rest** means it's just sitting there on your device in your pocket or on your lap or on your desktop uh sitting unused, maybe on or off. So when it comes to full disc encryption or encryption at rest, you ideally want all of your data somehow encrypted on your Mac, on your PC, on your phone. And only when you log in with your password or maybe your fingerprint or your face should that data be decrypted automatically.
And this can be hap this can happen pretty darn fast nowadays with modern hardware should the data be unencrypted. So you can actually use it and interact with that device. 
 So in other words, if this is my unencrypted data, the way I want it and need it when I'm using my computer, full disk encryption at rest would change my entire computer to look random.
So, if someone steals my device, as long as i am having best pratcices, as long as i have encrypted all data and it willl only be decrypted with my face id, finger print or pin code, the data will not be stolen. Only the device may be sold. These are random zeros and ones now that I generated by using, for instance, my password or my fingerprint or my face. 
But they're smart enough thanks to software known as firmware inside of it. As soon as the device realizes, wait a minute, that those bits over there aren't working properly anymore, the device might not let you change them to all zeros or all ones or a random zeros and ones anymore. It might just leave them as is forever. Which is to say, it's even more important to start using full disc encryption, encryption at rest, when you first get a device because that way you can trust that even if parts of the device degrade over time, all of the data that's there and has been there was at least encrypted with one of your pass code passwords or one of your biometrics in the past.
**Downside: Ransomeware**
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
TLS is a protocol which works on encrypting HTTP. So what does it do? It turns ot that it lies on public key cryptography/ asymetric cryptography. And this principle that if you give two parties A and B each thier own public key and private key you can communicate securely even if in advance you dont have a shared secret. As it allows us to establish a secure connection even though we have never visited some website or app before to communicate sewcurely to a web server.
So, by using TLS it is using a digital certificate. So, the certificate means a public key which has been signed by someone else. So, the website has a public key and a private key - the private key as always stays private. But in this case the web sefrver has a public ket that has been signed by some third party(companies). These certificates are a type of CALLED X.509 (The standard formate in which the certificate lives). The certificate has - the name of the website, the public key, how long the certificate is valid for(validity of the website).

**Certificate Authority(CA)**
These are the collection of companies and etities whose sole purpose in the world is to do digital signature in these certificates. And the various browser manufacturers like apple, microsoft, google, mozilla and othrers has a list of this CAs in thier browsers like edge, firefox, chrome who they trust. So, if i trust google, microsoft, mozilla or google so in transitivity i should also trust those CAs that the browser manufacturers trust.
So, what happens when a browser visits a website/  It first downloads the certificate assuming i am using HTTPS. Now the browser calculates a hash value for that certificates by looking at certain fields within it, suing a certain hash function taht produces a fixed lenghth of represenattion of the certificate. It then looks at the signature on that certificate and it then uses the certificate authoirty (the pulic key) who signed the certificate and now in conclusion it uses the signature from that server certificate and the CAs Public key - runs it through a algorithm - then decrypting the signature with the public key, and that should produce the exact same hash value. And taht should produce the exact same hash value.











































































 


