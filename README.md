# filecoin-notes
A compilation of various notes, articles, and additional curated media related to Filecoin

## resources
https://filecoin.io/blog/posts/what-sets-us-apart-filecoin-s-proof-system/

### glossary

* Proofs of Storge - are simple proving systems to prove that I have possession of some data. A Proof of Data Possession example is: I can prove to you that I have data X, either without revealing data X or if the data is several GB large, in some more succinct way. Then there’s Proof of Retrievability where, not only am I going to prove that I have X, but also that these proofs can be used to reconstruct X in case I’m malicious and want to withhold X from you.

* Proofs of Space - are a different type of group where I can guarantee to you that I’m spending a certain amount of storage. If I commit to storing 1 GB, and I generate a random GB then I can prove to you that I’m storing that random GB and not storing some other thing. That lets you use storage space as a Proof of Work.

* Proofs of Replication - In Proof of Replication we take the source data, a large amount like 32GB, and apply a very slow encoding that produces these lattice-like graphs in layers where a node might be a 32 byte segment. There’s a sequential process going on producing a graph and for each node hashing sequentially. It has to be done one after the other, because of the hash function.

* SNARKS - 

* DRG (Depth-Robust-Graph)

#### notes
The interesting part is combining a Proof of Space with a normal Proof of data possession, where I would like X to be useful, not just a random string. The hard part of this was to create a Proof of Space that was also being used to store useful data. So that’s what Proofs of Replication are as foundational primitives in the Filecoin network’s cryptographic protocol.

I think no other network is using Proof of Replication, it’s an advantage we have that we created that field. So that’s one differentiating factor. We are also the only one with this fluid market structure that is meant to be optimized based on an ask and bid structure where miners and clients are able to reason about prices together and then form deals out of that. I think we are also the only ones doing consensus backed by useful storage. With other networks it may be a consensus backed by a Proof of Space, but in our case it’s useful. Those are the three biggest differentiating factors of Filecoin.
