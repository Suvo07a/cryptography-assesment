# Cybersecurity Assessment Submissions

**Author:** Shubojeet Mondal


## Task 12: Explore a Cryptography Concept (SHA-256)

### 1. Explanation of the Concept
For this task, I explored cryptographic hashing. Hashing is a mathematical process that takes an input (like a password, a text message, or a file) and scrambles it into a fixed-size string of characters called a "hash." 

I focused on the **SHA-256** algorithm. Hashing is a "one-way" function, meaning you cannot look at a hash and reverse it to figure out the original input. It is mostly used to prove that data has not been tampered with. If two files have the exact same hash, they are identical. If even a single punctuation mark is changed, the hash changes completely.

### 2. Practical Demonstration (The Avalanche Effect)
To show how this works in practice, I performed a practical test using a professional software protection and hash calculator tool. 

**Testing Website Used:** [https://www.pelock.com/products/hash-calculator](https://www.pelock.com/products/hash-calculator)

I hashed a personalized sentence, and then changed just one single punctuation mark to show what happens. This massive change in the output is called the "Avalanche Effect."

**Test 1: The Original Input**
*   **Input Data:** `Hii Shubo this side.`
*   **Algorithm Used:** SHA-256
*   **Hash Result:** `F170DB8115EF31A514206D6F967B281B28871A07E0EE928DDE97FCD8C054898A`

**Test 2: The Modified Input (Changed the period to an exclamation mark)**
*   **Input Data:** `Hii Shubo this side!`
*   **Algorithm Used:** SHA-256
*   **Hash Result:** `280DB8D27789591DA309022C1FC26804E8036D34588D2AAA6D2D459BD1B155D1`

**Observation:** Even though I only changed the final punctuation mark, the resulting hash is completely unrecognizable from the first one. This proves the data was successfully altered and detected. I have also attached the screenshots for refrence.

### 3. Limitations of Hashing
While hashing is a great security tool, it is important to know what it cannot protect:
*   **It is not Encryption:** Hashing does not hide data. If you send a secret message over the internet and attach a hash, anyone who intercepts it can still read your original message. The hash only proves the message wasn't changed in transit.
*   **Vulnerable to Brute-Force:** If a website hashes simple, weak passwords (like "password123") without adding random extra data to it (called a "salt"), an attacker can simply guess common passwords, hash them, and compare them to the stolen database to easily find a match.

---
