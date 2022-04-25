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

## Tasks
1. Front-end (@junkim012)
    1. Fork Pontis-ui or clean up Jun's Next.js UI
1. Prover (@junkim012)
    1. (Optional) See if we can generate a proof using <https://github.com/nccgroup/draft-irtf-cfrg-vrf-06/blob/master/ecvrf_edwards25519_sha512_elligator2.py#L68>
1. Slides (@nashqueue)
    1. Describe motivation for project
    1. Describe how we would verify this proof in Cairo
    1. Think about questions and prepare slides for that
    1. Show in README.md example of how a Cairo contract can consume our random numbers
    1. Roadmap and partnership with ZKasino and MatchboxDAO
    1. Memes


## Links
1. https://rocky-volleyball-654.notion.site/Pontis-f5103d8ecc9d49a6844323819570c1b6
2. https://master--verdant-zuccutto-94784a.netlify.app/
