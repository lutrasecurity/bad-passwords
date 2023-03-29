# Bad passwords

Not every password is equally good. For this reason, [NIST SP 800-63B](https://pages.nist.gov/800-63-3/sp800-63b.html#sec5) recommends checking passwords against a list of commonly-used, expected, or compromised passwords:

> When processing requests to establish and change memorized secrets, verifiers SHALL compare the prospective secrets against a list that contains values known to be commonly-used, expected, or compromised. For example, the list MAY include, but is not limited to:
> 
> * Passwords obtained from previous breach corpuses.
> * Dictionary words.
> * Repetitive or sequential characters (e.g. ‘aaaaaa’, ‘1234abcd’).
> * Context-specific words, such as the name of the service, the username, and derivatives thereof.
> 
> If the chosen secret is found in the list, the CSP or verifier SHALL advise the subscriber that they need to select a different secret, SHALL provide the reason for rejection, and SHALL require the subscriber to choose a different value.

To answer the question of the most commonly used passwords, we monitor login attempts on various honeypots and aggregate the credentials into a list of passwords that are actively used by attackers.

The file [bottom_1000.txt](bottom_1000.txt) contains the 1000 most commonly encountered passwords, and therefore worst passwords that can be used on any system accessible from the internet. A user who uses one of these passwords can expect to be compromised within a matter of hours.

The article [Known Weak Passwords](https://lutrasecurity.com/en/articles/common-passwords/) explains how to use this data to protect your applications and provides access to an even more comprehensive dataset.
