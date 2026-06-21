# Application Attacks

This is a general variety of different possible web attacks.

## Injection attacks

This involves adding your own code into a server's data stream usually via some form of input. This is typically enabled because of bad programming; **be very mindful** of what comes in and what comes out.

There are a lot of injection types out there; SQL, HTML, XSS, so on so forth.

## Buffer Overflow

Overwriting a buffer of memory, which usually is used for storing / handling data, spills into other memory areas. This can cause unwanted results for the server; improper output, a completely unrelated script goes off somewhere else, etc.

This is not simple to do. It takes time and effort to avoid crashing or to even make it do what you want it to do. But attackers typically look for one that is repeatable; if they can utilize this and it potentially has malicious use, the server owners might have no idea until it is too late.

## Replay attack

This is simply attackers taking real data from a victim and replaying it back to a server. Perhaps an attacker installs malware that takes session ID's from a victim. The attacker can replay that to a legit server and then act as if they're the victim.

## Privilege Escalation

This is the concept of gaining higher access to privileges that you should not usually be able to access. Guests on a network should not have admin, and absolutely should not be trusted with it. This is a very common and serious attack vector.

Although this is commonly related to going from guest --> privilege, this also includes not allowing user's to access other user's accounts.

Patching the system and fixing any known paths of escalation (cheap passwords, easy command line use, etc) is essential. Install anti-virus as well to prevent outside sources from attemptig to gain privilege escalation on a user's computer. 

## XSS Attack

Cross-site attacks trick victims into loading malicious data onto a site. This ranges from accessing a malicious site that is misspelled, an email with malicious parameters, a threat actor posting a script onto a forum that publically displays, etc. The are usually just due to human misunderstanding and how client-side servers act (running HTML and JS).

## Cross-site request forgery

CSRP (also known as session riding, one-click attack) is the concept of an attacker using the server's trust for a victim against the victim. The attacker might create a script/malware that does certain things to a web server from the victim's trust. Because the web server trust's the user, it will do those certain things.

These can be protected with CSRF tokens; they are only given to the victim's request. The attacker would not be able to know this token.

## Directory traversal

This is the concept of reading and accessing files and folders that are outside of a website's file directory. User's typically should not be able to view a web server's Windows related folders as these provide vital system information. Even worse, maybe attackers could write code to these folders through some inner server process.

Badly written code with bad parameters can cause this. Perhaps a simple GET request involve the root directory of the server, and then that directory is returned. That should not happen.