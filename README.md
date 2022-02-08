# Interplanetary File System

![](https://i.imgur.com/fyuuSjW.png)

## Internet

Current internet as we all know and use runs on centralized servers which has both advantages and disadvantages.

- Advantages include high speed of delivery of content
- Disadvantages include several single points of failure and the risk of censorship. One example of censorship is [China blocking Youtube](https://www.theguardian.com/world/2009/mar/25/china-blocks-youtube)

## IPFS

IPFS stands for InterPlanetary File system. It is a decentralized protocol for storing content like files, images etc in an immutable way(data cannot be changed once written)

## How does it work?

Referencing it from the [IPFS website](https://ipfs.io/) directly:

Here is how `IPFS` stores your content:

- When you add new content to IPFS, the content is split into smaller chunks which are cryptographically hashed and your content is given a unique identifier known as a `CID`(content identifier).
- This CID acts as a permetant record of your content.
- You can consider CID equivalent to a `primary key` in a database table. Similar to how each row in the table has a different key which acts like a unique identifier for that row, CID acts as an unique indentifier for your content
- There are many IPFS nodes running at a given point of time.
- When other nodes look up for your content, they ask their peer nodes who's storing the content refrenced by the file's CID.
- When they view or download your content, they cache a copy - and become another provider of your content until the cache is cleared. So now your data is avaible on multiple nodes and has backup.
- But its important to note that a node can [pin your content](https://docs.ipfs.io/concepts/persistence/) in order to keep it forever, However it can also choose to disregard it.
- This means that each node in the network only stores content they are intrested in and some indexing information that helps figure out which node is storing what
- Every new version of file on IPFS generates a new cryptographic hash and has a new CID, this prevents tampering of data
- Common chunks across files can be reused in order to minimize storage costs

## Conclusion

IPFS has now become an important part of the blockchain ecosystem and in the upcoming modules we would learn how to use IPFS in our dApps.

Stay tuned 🚀
