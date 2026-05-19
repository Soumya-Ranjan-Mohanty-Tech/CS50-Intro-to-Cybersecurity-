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
