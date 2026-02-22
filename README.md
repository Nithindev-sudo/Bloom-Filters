# Bloom-Filters
Probablistic Data Structure

🌸 Bloom Filters by Example

A Bloom Filter is a space-efficient probabilistic data structure used to test whether an element is a present or available in a set.

There is also another aspect to consider about bloom filters which is, It can tell you:

✅ if possibly in the set / possibly not in the set

But it cannot provide:

❌ Definitely not in the set / Definetely in the set

❗ The trade-off for speed and memory efficiency is that false positives are possible, but false negatives are not. It tells us that the element either definitely is not in the set or may be in the set.

📌 Why Bloom Filters?

Bloom filters are used when:

➡️ You need very fast membership checks without scanning of entire Databases.

➡️ Memory usage must be minimal.

➡️ Occasional false positives are acceptable.

They are commonly used in:

➡️ Databases.

➡️ Caches.

➡️ Distributed systems.

📊 Base Data Structure

Base Data Structure for a Bloom Filter is mainly a Bit Vector / a Bit Array (or BitSet).

🧠 Bit arrays use only 1 bit per entry, offering massive memory savings compared to storing actual elements in a hash table.

⏱️ Time Complexity : 

Both inserting elements and querying membership are (O(**k**)) operations, where **k** is the number of hash functions. Since **k** is a small constant, this is essentially (O(1)).

⚛️ How a Bloom Filter Works

 A Bloom filter consists of:

1) A bit array of size **M**.

2) **K** independent hash functions.

3)  **N** no if insesrtions to be made into the Bloom filter.

   1️⃣ **Bit Array/ Bit vector :**

   To add a element to the Bloom filter, we simply hash it a **k** times and set the bits in the bit vector at the **n** th index of those hashes to 1(turn ON).

   2️⃣ ****K** independent hash functions** **:**

   The hash functions used in a Bloom filter should be independent and uniformly distributed(outputs the same hash value when same input is provided any number of times this reduces false positives). They should     also be as fast as possible (cryptographic hashes such as sha1, is not very good choices).

   Best hash functions that can be used for bloom filters are murmur




