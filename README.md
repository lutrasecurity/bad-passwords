# Bad passwords

Not every password is equally good. For this reason, [NIST SP 800-63B](https://pages.nist.gov/800-63-3/sp800-63b.html#sec5) recommends checking passwords against a list of compromised or commonly-used passwords:

> When processing requests to establish and change memorized secrets, verifiers SHALL compare the prospective secrets against a list that contains values known to be commonly-used, expected, or compromised. For example, the list MAY include, but is not limited to:
> 
> * Passwords obtained from previous breach corpuses.
> * Dictionary words.
> * Repetitive or sequential characters (e.g. ‘aaaaaa’, ‘1234abcd’).
> * Context-specific words, such as the name of the service, the username, and derivatives thereof.
> 
> If the chosen secret is found in the list, the CSP or verifier SHALL advise the subscriber that they need to select a different secret, SHALL provide the reason for rejection, and SHALL require the subscriber to choose a different value.

This repository attempts to answer the question of the most commonly used passwords: Which passwords are actively abused by attackers? To do this, we observe login attempts on various honey pots and have aggregated the used credentials.

The file [bottom_1000.txt](bottom_1000.txt) contains the 1000 worst passwords that can be used on any system accessible from the internet. A user who uses one of these passwords can expect to be compromised within a matter of hours.
