# Bloom-Filters
Probablistic Data Structure

🌸 Bloom Filters by Example

A Bloom Filter is a space-efficient probabilistic data structure used to test whether an element is a present or available  in a set.

There is also another aspect to consider about bloom filters which is,
It can tell you:
✅ if possibly in the set/ possibly not in the set

But it cannot provide: 
❌ Definitely not in the set/ Definetely in the set

❗The trade-off for speed and memory efficiency is that false positives are possible, but false negatives are not.
  it tells us that the element either definitely is not in the set or may be in the set.

📌 Why Bloom Filters?

Bloom filters are used when:

➡️ You need very fast membership checks without scanning of entire Databases.
➡️ Memory usage must be minimal.
➡️ Occasional false positives are acceptable.

They are commonly used in:

➡️ Databases.
➡️ Caches.
➡️ Distributed systems.


📊 Base Data Structure for a Bloom Filter is mainly a Bit Vector/a Bit Array (or BitSet)
🧠 Bit arrays use only 1 bit per entry, offering massive memory savings compared to storing actual elements in a hash table.

⚛️ How a Bloom Filter Works

A Bloom filter consists of:
A bit array of size **M**
**K** independent hash functions


Networking

Big data systems
