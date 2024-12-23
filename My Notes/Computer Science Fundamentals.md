#study #philnits
December 24, 2024

>[!note|Learning Queries]
>How is information stored by the computer? How are decimal numbers and characters converted into binary for the computer to understand? How is information processed? And how are data structures implemented so that data processing is much efficient? What are the data processing methods?
# **Basic Theory of Information**
***

**What about it?**
Information can exist in various forms, such as characters and numerals. However, when stored in a computer, all information—regardless of its form—is represented as combinations of 1s and 0s. This representation, known as ==**binary numbers**, serves as the foundation of all digital data==. Simply put, at its core, all computer-stored information is essentially just sequences of 1s and 0s.

>[!question]
Now, I want to understand why must we understand how information is translated into the computer, why must we learn how the computer understands information and data at the lowest level.

>***Information Theory** is the mathematical study of the quantification, storage, and communication of information.*

### The Relation of Information Theory in Computer Science
Information theory and computer science are closely intertwined in several ways:

###### Data Compression
Information theory provides the foundational principles for data compression techniques. Concepts like **entropy** *(the measurement of degree in randomness)* help quantify the amount of information in a message, guiding the ==development of algorithms that **reduce the size of data** without losing essential information== (e.g., ZIP files, JPEG images).

###### Error Detection and Correction
Information theory plays a critical role in ==designing error detection and correction codes.== These codes ensure data integrity during transmission over unreliable channels. Techniques such as **Hamming codes** and **Reed-Solomon codes** are grounded in information-theoretic principles.

###### Cryptography
Information theory contributes to cryptography by analyzing the security of communication systems. Concepts like **Shannon’s entropy** are used to ==measure the uncertainty and unpredictability of keys and encrypted messages==, helping to design secure systems.

###### Network Theory
In computer networks, information theory aids in ==understanding and optimizing data transmission==. It helps in ==determining bandwidth requirements and developing protocols for efficient data flow==, ensuring that networks can handle large amounts of information effectively.

###### Machine Learning and AI
Information theory informs various aspects of machine learning, including feature selection and model evaluation. Metrics like mutual information are used ==to measure the relevance of features in predicting outcomes==, while concepts like **Kullback-Leibler divergence** help in comparing probability distributions.

###### Algorithm Analysis
Information theory provides tools for ==analyzing the efficiency of algorithms, particularly in terms of their **information content and complexity**==. It helps in understanding the limits of what can be computed and how efficiently it can be done.

###### Communication Complexity
This area ==studies the amount of communication required to solve a problem collaboratively==. It has implications for distributed computing and algorithms where multiple parties need to share information efficiently.

>[!note] Conclusion
>Overall, information theory serves as a crucial theoretical framework within computer science, influencing a wide range of **applications from data storage and transmission to security and machine learning**. Its principles help in developing efficient algorithms and systems that manage and manipulate information effectively. Basically we relate this from its primary concern with the analysis, collection, classification, manipulation, storage, retrieval, movement, dissemination, and protection of information since computer science does handle data then we should know how to handle it well and how the computer handles it as it is.

### Storing Information at Its Lowest Level
Information is stored by the computer in a number system based on two states: 1 and 0 in which is called as “Binary”. These states are the foundation of all digital processing and are represented physically within the computer by **electronic switches** or **transistors** in its memory and processing units.

We understand that the important files and data we have in our computer are stored in our physical memory such as our hard drives. However, these files are what we also refer as our information and data in which comes in various forms. Let’s try to grasp how the computer really processes and store these information at the lowest level possible. ==At the lowest level, any kind of information is represented in binary.== By combining two states of 1s and 0s into sequences, computers represent all kinds of information, from numbers and text to images and videos.

### Bits, Bytes, and Addresses
This segment is merely a quick overview on the basics of data in a computer. The ==smallest unit of data is a **bit**== (binary digit), which can have one of two values: 1 or 0 — which can also represent as ON or OFF. While a single bit is useful, it’s limited because it can only represent two states.

To be able to handle more complex information, we group ==8 bits together to form a **byte**==. A byte is often considered the standard unit of memory because it can represent 256 unique combinations ($2^8$). These combinations allow us to encode a wide range of data, such as:
- A single character in a text (e.g., the letter "A" in ASCII is `01000001` ).
- Numbers, small images, or parts of larger data.

Now that we have bits and bytes, how does the computer know where to find and store them? This is where **memory addresses** come into play. Think of memory as a ==large grid of storage locations, and each location has a unique identifier called an **address**==. These addresses work like house numbers on a street: they tell the computer exactly where to look for or place a piece of data.

For example:
- If a byte of data is stored at address **1001**, the computer knows to go to that specific "house" in memory to retrieve or modify it.
- This system ensures efficient storage and retrieval, no matter how large or small the dataset is.

### Physical Representation of Binary in Memory
Theoretically, we know that data can be represented in Binary as its lowest form. However, ==how does the computer represent this information physically in regards to hardware?== Different components of the computer are relied on to store and manage these binary states.

Here are a few components as examples:

###### Transistors: The Foundation of Digital Logic
Transistors are the smallest and most fundamental building blocks of modern electronics. They act like tiny switches:

**ON (1)**: When current flows through the transistor.
**OFF (0)**: When current doesn’t flow.

Every bit of data in a computer is essentially controlled by billions of these transistors working together.

###### Capacitors: Used in Dynamic RAM (DRAM)
Capacitors are like tiny buckets that hold electrical charge:

**1**: A charged capacitor.
**0**: A discharged capacitor. However, capacitors lose charge over time, so DRAM constantly refreshes itself to maintain data.