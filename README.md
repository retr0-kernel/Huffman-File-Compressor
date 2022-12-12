- C++ programs which can compress and extract the file using Huffman Coding - A lossless data compression using variable length codes. It is the most efficient algorithm for data compression.

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

Refer encode.cpp to see what is done by each segment of code.

The reason why this approach is currently the most effecient is because it reduces the overall tree length by almost 4 times in average cases and worst case is near to average case of Huffman cide.

The characterID alloted to each character in a message is dependant on the length of the tree formed and for the same number message, the tree height of conventional Huffman encoding is higher than our proposed idea.

The same can be seen in the tree below

    CONVENTIONAL HUFFMAN TREE
![image](https://user-images.githubusercontent.com/87553028/206996350-a27a3908-ea7e-4caa-bad6-244c32757403.png)


    0-7 HUFFMAN TREE
