# randomfeedooooor

randomfeedooooor is a [Pontis](
https://github.com/42labs/Pontis) publish for random numbers.

Basic random number generator:

1. hash(x)
2. hash(hash(x))
3. hash(hash(hash(x)))

In block 0, we publish 3. Some time later, we publish block 2. Users of the system can verify that 2 is indeed a random number because they can hash 2 and get 3.

Users must trust us (the random number publisher) to not leak the series of hashes or x (the initial seed) because if x is leaked, a malicious actor can brute force the series of random numbers.


## Consuming the Random Feed from Pontis 

1. Get the 'key' using str_to_felt("random") from pontis.core.utils 
2. Get aggregated value using get_value(key), or get multiple values from all of our random number generators using get_entries_for_key(key) 

## Links
1. https://rocky-volleyball-654.notion.site/Pontis-f5103d8ecc9d49a6844323819570c1b6
2. https://master--verdant-zuccutto-94784a.netlify.app/
