#study #philnits
December 24, 2024

>[!note|Learning Queries]
>How is information stored by the computer? How are decimal numbers and characters converted into binary for the computer to understand? How is information processed? And how are data structures implemented so that data processing is much efficient? What are the data processing methods?


# **Basic Theory of Information**
***
###### What about it?
Information can exist in various forms, such as characters and numerals. However, when stored in a computer, all information—regardless of its form—is represented as combinations of 1s and 0s. This representation, known as <font color="#76923c">**binary numbers**, serves as the foundation of all digital data</font>. Simply put, at its core, all computer-stored information is essentially just sequences of 1s and 0s.

>[!question]
Now, why must we understand how information is translated into the compute? Why must we learn how the computer understands information and data at the lowest level?

>**Information Theory** is the mathematical study of the quantification, storage, and communication of information.

### The Relation of Information Theory in Computer Science
Information theory and computer science are closely intertwined in several ways:

![[Pasted image 20241226193429.png]]
##### <span style="background:rgba(140, 140, 140, 0.12)">Data Compression</span>
Information theory provides the foundational principles for data compression techniques. Concepts like **entropy** *(the measurement of degree in randomness)* help quantify the amount of information in a message, <font color="#76923c">guiding the development of algorithms that **reduce the size of data** without losing essential information</font> (e.g., ZIP files, JPEG images).
##### <span style="background:rgba(140, 140, 140, 0.12)">Error Detection and Correction</span>
Information theory plays a critical role in <font color="#76923c">designing error detection and correction codes</font>. These codes ensure data integrity during transmission over unreliable channels. Techniques such as **Hamming codes** and **Reed-Solomon codes** are grounded in information-theoretic principles.
##### <span style="background:rgba(140, 140, 140, 0.12)">Cryptography</span>
Information theory contributes to cryptography by analyzing the security of communication systems. Concepts like **Shannon’s entropy** are used to <font color="#76923c">measure the uncertainty and unpredictability of keys and encrypted messages</font>, helping to design secure systems.
##### <span style="background:rgba(140, 140, 140, 0.12)">Network Theory</span>
In computer networks, information theory aids in <font color="#76923c">understanding and optimizing data transmission</font>. It helps in <font color="#76923c">determining bandwidth requirements and developing protocols for efficient data flow</font>, ensuring that networks can handle large amounts of information effectively.
##### <span style="background:rgba(140, 140, 140, 0.12)">Machine Learning and AI</span>
Information theory informs various aspects of machine learning, including feature selection and model evaluation. Metrics like mutual information are used <font color="#76923c">to measure the relevance of features in predicting outcomes</font>, while concepts like <font color="#76923c">**Kullback-Leibler divergence**</font> help in comparing probability distributions.
##### <span style="background:rgba(140, 140, 140, 0.12)">Algorithm Analysis</span>
Information theory provides tools for <font color="#76923c">analyzing the efficiency of algorithms, particularly in terms of their **information content and complexity**</font>. It helps in understanding the limits of what can be computed and how efficiently it can be done.
##### <span style="background:rgba(140, 140, 140, 0.12)">Communication Complexity</span>
This area <font color="#76923c">studies the amount of communication required to solve a problem collaboratively</font>. It has implications for distributed computing and algorithms where multiple parties need to share information efficiently.

>[!note] Conclusion
>Overall, information theory serves as a crucial theoretical framework within computer science, influencing a wide range of **applications from data storage and transmission to security and machine learning**. Its principles help in developing efficient algorithms and systems that manage and manipulate information effectively. Basically we relate this from its primary concern with the analysis, collection, classification, manipulation, storage, retrieval, movement, dissemination, and protection of information since computer science does handle data then we should know how to handle it well and how the computer handles it as it is.

### Storing Information at Its Lowest Level
Information is stored by the computer in a number system based on two states: 1 and 0 in which is called as “Binary”. These states are the foundation of all digital processing and are represented physically within the computer by <font color="#76923c">**electronic switches**</font> or <font color="#76923c">**transistors**</font> in its memory and processing units.

![[Pasted image 20241225213550.png|300]]

We understand that the important files and data we have in our computer are stored in our physical memory such as our hard drives. However, these files are what we also refer as our information and data in which comes in various forms. Let’s try to grasp how the computer really processes and store these information at the lowest level possible. <font color="#76923c">At the lowest level, any kind of information is represented in binary.</font> By combining two states of 1s and 0s into sequences, computers represent all kinds of information, from numbers and text to images and videos.

![[Pasted image 20241225214217.png]]

### Bits, Bytes, and Addresses
This segment is merely a quick overview on the basics of data in a computer. The <font color="#76923c">smallest unit of data is a **bit**</font> (binary digit), which can have one of two values: 1 or 0 — which can also represent as ON or OFF. While a single bit is useful, it’s limited because it can only represent two states.

To be able to handle more complex information, we group <font color="#76923c">8 bits together to form a **byte**</font>. A byte is often considered the standard unit of memory because it can represent 256 unique combinations ($2^8$). These combinations allow us to encode a wide range of data, such as:
- A single character in a text (e.g., the letter "A" in ASCII is `01000001` ).
- Numbers, small images, or parts of larger data.

Now that we have bits and bytes, how does the computer know where to find and store them? This is where **memory addresses** come into play. Think of memory as a <font color="#76923c">large grid of storage locations, and each location has a unique identifier called an **address**</font>. These addresses work like house numbers on a street: they tell the computer exactly where to look for or place a piece of data.

For example:
- If a byte of data is stored at address **1001**, the computer knows to go to that specific "house" in memory to retrieve or modify it.
- This system ensures efficient storage and retrieval, no matter how large or small the dataset is.

### Physical Representation of Binary in Memory
Theoretically, we know that data can be represented in Binary as its lowest form. However, <font color="#76923c">how does the computer represent this information physically in regards to hardware?</font> Different components of the computer are relied on to store and manage these binary states.

Here are a few components as examples:

![[Pasted image 20241226192937.png|400]]
##### <span style="background:rgba(140, 140, 140, 0.12)">Transistors: The Foundation of Digital Logic</span>
Transistors are the <font color="#76923c">smallest and most fundamental building blocks of modern electronics</font>. They act like tiny switches:
<font color="#76923c">**ON (1)**</font>: When current flows through the transistor.
<font color="#76923c">**OFF (0)**</font>: When current doesn’t flow.
Every bit of data in a computer is essentially controlled by billions of these transistors working together.
##### <span style="background:rgba(140, 140, 140, 0.12)">Capacitors: Used in Dynamic RAM (DRAM)</span>
Capacitors are <font color="#76923c">like tiny buckets that hold electrical charge</font>:
<font color="#76923c">**1**</font>: A charged capacitor.
<font color="#76923c">**0**</font>: A discharged capacitor. However, capacitors lose charge over time, so DRAM constantly refreshes itself to maintain data.
##### <span style="background:rgba(140, 140, 140, 0.12)">Magnetic Storage: Hard Drives</span>  
In magnetic storage devices like traditional hard drives:
<font color="#76923c">Magnetic fields are oriented in one of two directions</font> to represent 1s and 0s.
This makes data storage reliable and long-lasting but slower compared to newer technologies.
##### <span style="background:rgba(140, 140, 140, 0.12)">Flash Memory: SSDs and USB Drives </span> 
Flash memory uses <font color="#76923c">**floating-gate transistors** to trap electrical charges</font>:
<font color="#76923c">**High Charge**</font>: Represents 1.
<font color="#76923c">**Low Charge**</font>: Represents 0.  
This method is faster and more durable than magnetic storage, which is why it’s used in solid-state drives (SSDs) and USB flash drives.

> [!question]
> When do other base numbers other than binary step into the computer? Why is it so important for computer science students to learn about base conversion?

Sure, we've mentioned how significant binary number is at the hardware level, but what about the other base numbers? Well, in order for the computer to store data and information, the **user** (the human) shall give it data and information first. The data being talked about may come in different forms such as the following:

##### <span style="background:rgba(140, 140, 140, 0.12)">Decimal (base 10)</span>
Humans naturally work with base 10 for everyday calculations and communication. Decimal numbers are <font color="#76923c">used in user input/output, calculations, and financial applications</font>. 

##### <span style="background:rgba(140, 140, 140, 0.12)">Hexadecimal (base 16)</span>
Hexadecimal is a compact representation of binary, making it essential for:
- <font color="#76923c">**Debugging**</font>: Memory addresses, error codes, and machine instructions are often represented in hexadecimal for readability.
- <font color="#76923c">**Color Representation**</font>: Web design uses hexadecimal to represent colors (e.g., `#FF5733`).
- <font color="#76923c">**Low-Level Programming**</font>: Hexadecimal simplifies reading and writing binary-encoded data.

##### <span style="background:rgba(140, 140, 140, 0.12)">Octal (base 8)</span>
Although <font color="#76923c">**less common**</font>, octal was historically used in computing (e.g., permissions in Unix/Linux systems like `chmod 755` for file access rights) because it’s easier to interpret than binary in some contexts.

##### <span style="background:rgba(140, 140, 140, 0.12)">Base 64 and other bases</span>
Base 64 is often used in <font color="#76923c">encoding schemes for data transfer</font> (e.g., email attachments, image encoding). Similarly, bases like 3 (ternary) are explored in specialized computing systems.

These numeral systems illustrate the adaptability of computing to diverse applications, bridging human logic and machine efficiency.

> [!note]
> So far we have went over the following:
> **Information Theory** -> **Primary Unit of Information** -> ~~**Radix Conversion**~~

***
##### What is a Number System?
A number system is a writing system for expressing numbers in a consistent manner using a set of symbols or digits. This defines how a number must be represented and how arithmetic operations are performed on those representations.

Each number system has its **base** *(also referred to as "radix")*, which determines the number of unique symbols used in the system.

**Key Components**
1. <font color="#76923c">**Base**</font> -  the radix and represented as *"base n"* where n shall be the number of digits. 
2. <font color="#76923c"> **Digits**</font>
3. <font color="#76923c">**Positional Value**</font> - the position of a digit within its number determines its value, based on the base of the system. 

Example:
Suppose that given the base number <font color="#d99694">**n**</font>, its <font color="#d99694">**positional weight**</font> shall be <font color="#d99694">**n<sup>a</sup>**</font>, wherein a shall the the <font color="#d99694">**positional value**</font>.
<center>2<sup>7</sup>  2<sup>6</sup>  2<sup>5</sup>  2<sup>4</sup>    2<sup>3</sup>  2<sup>2</sup>  2<sup>1</sup>  2<sup>0</sup>
</center>

<font color="#76923c">![[Pasted image 20241225234022.png|200]]</font><center>128 64 32 16 8 4 2 1</center>
<center><font color="#7f7f7f">(each digit w/ its corresponding positional weight)</font></center>
One number system can often be converted to another by using specific rules. For example, binary numbers can be converted to decimal, octal, or hexadecimal.

---

# Radix Conversion
We've went over how computers physically represent binary states in hardware and how significant is it for grasping how they process and store information. While computers inherently work in binary, humans typically use other numerical systems like decimal, octal, or hexadecimal in various applications. <font color="#76923c">Radix conversion simply acts as a **bridge between number systems**, enabling seamless interaction between human and machine-readable formats.</font> 

![[Pasted image 20241225215100.png|400]]
<center><font color="#7f7f7f">(conversion shortcut)</font></center>

For any base number,  
##### <span style="background:rgba(140, 140, 140, 0.12)">Binary to Octal</span>
Process:
1. Given a binary number, **group the bits into three** from right to left.
2. Add leading zeros to the leftmost group if necessary.
3. Convert each group into octal.

![[Pasted image 20241226194702.png|200]]

| Binary | Octal |
| :----: | :---: |
|  000   |   0   |
|  001   |   1   |
|  010   |   2   |
|  011   |   3   |
|  100   |   4   |
|  101   |   5   |
|  110   |   6   |
|  111   |   7   |

**Practice Problems**

|     Binary      |   Octal   |
| :-------------: | :-------: |
|     101 010     |  **52**   |
|     110 101     |  **65**   |
| 110 011 110 111 | **6 367** |
|     111 110     |  **76**   |
|   10 101 101    |  **255**  |
|    1 001 010    |  **112**  |
|   111 011 100   |  **734**  |
| 10 001 100 101  | **2 145** |
|   101 110 011   |  **563**  |
|    1 001 011    |  **113**  |

##### <span style="background:rgba(140, 140, 140, 0.12)">Octal to Binary</span>
Process:
1. For each digit in the given octal number, convert it into binary of three bits.
2. Combine the binary groups.

![[Pasted image 20241226194555.png|200]]

**Practice Problems**

| Octal |     **Binary**      |
| :---: | :-------------: |
| 7 643 | **111 110 100 011** |
| 3 152 | **011 001 101 010** |
| 4 075 | **100 000 111 101** |
| 6 251 | **110 010 101 001** |
| 7 324 | **111 011 010 100** |
| 5 670 | **101 110 111 000** |
| 1 777 | **001 111 111 111** |
| 2 465 | **010 100 110 101** |
| 7 016 | **111 000 001 110** |
| 5 123 | **101 001 010 011** |

##### <span style="background:rgba(140, 140, 140, 0.12)">Binary to Decimal</span>

##### <span style="background:rgba(140, 140, 140, 0.12)">Decimal to Binary</span>

##### <span style="background:rgba(140, 140, 140, 0.12)">Binary to Hexadecimal</span>

##### <span style="background:rgba(140, 140, 140, 0.12)">Hexadecimal to Binary</span>