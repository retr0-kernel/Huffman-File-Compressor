        FILE COMPRESSION USING HUFFMAN ADAPTED ENCODING

- C++ programs which can compress and extract the file using ADAPTED HUFFMAN CODING : A lossless data compression using variable length codes. It is the most efficient algorithm for data compression.

- The program encode.cpp needs the name of file as an argument. It will the compress the file using Huffman encoding algorithm and generate a new compressed file with .huf extension.

- The program decode.cpp needs the name of compressed file with extension .huf. Optionally you can also give a second argument specifying the name of the decoded output file.

- The compression ratios depend on the type of the input file.

- For small files(order of bytes) it is not recommended to compress, because of fractional compression ratio. The compressed file occupies more space than input file.

- In general, larger the input file sizes, better is the compression ratios. The compression ratios depend on the probabilities of source's data.

- Here's the approach our method use:
    1. Sort the frequencies and group it into groups of 8.
    2. Label each connection as 0,1,2,3,4,5,6,7 and create a tree structure just like in Huffman Coding.
    3. Retrieve the modified ID for each componant of the message.
    4. Create a Reference Table for the new alloted values to the characters.

Refer encode.cpp[a link](https://github.com/user/repo/blob/branch/other_file.md) to see what is done by each segment of code.

The reason why this approach is currently the most effecient is because it reduces the overall tree length by almost 4 times in average cases and worst case is near to average case of Huffman cide.

The characterID alloted to each character in a message is dependant on the length of the tree formed and for the same number message, the tree height of conventional Huffman encoding is higher than our proposed idea.

The same can be seen in the tree below

    CONVENTIONAL HUFFMAN TREE
![image](https://user-images.githubusercontent.com/87553028/206996350-a27a3908-ea7e-4caa-bad6-244c32757403.png)


    0-7 HUFFMAN TREE
 ![image](https://user-images.githubusercontent.com/87553028/206997765-20c36be3-514b-4e4b-bc30-371efee3deba.png)

As visible in the tree, the hieght is 8-bits, whereas in the 0-7 Huffman Code, it is 3-bits. This reduces overall size by almost half.

        IMPLEMENTING THE CODE IN TERMINAL
 ![WhatsApp Image 2022-12-12 at 14 07 53](https://user-images.githubusercontent.com/87553028/207003246-d2f889d7-d5b9-4a31-9c94-39eb43993746.jpg)

This is what the input and output will look like in the terminal and all the files will be read or created locally on the system in the background.
