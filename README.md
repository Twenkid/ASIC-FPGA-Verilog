# ASIC-FPGA-Verilog

Two training tasks:

1. Sum Channels DSP ... by Krassimir and Todor/Twenkid
2. Data Cache Tag Mechanism by Todor Arnaudov

# ASIC, FPGA, Verilog projects and materials

# Sum Channels DSP ...

The block is used to maintain the history of symbols in a DSP system. It provides the sum of the last 4 or 8 valid values, coming to the block from 64 input channels. The sum goes to the output 5 clocks after data has arrived, including the latest valid data on data_in. The system also provides valid sum even if only one valid data item is received for a channel.

The input data is 8 bit wide and is treated as unsigned.

![image](https://user-images.githubusercontent.com/23367640/158000485-886cccb7-758b-4461-9776-41a24af29f23.png)

# Data Cache Tag Mechanism

This block is an example of logical implementation of the tag-mechanism of a 4-way set associative copyback data cache. However, it must be explicitly stated, that the system does not work with appropriate timing for a real cache design, i.e. one result at every clock. The design is done following standard methodology of splitting the logic in pipelines, in order to shorten the length of gates that the signal passes in one clock, instead of achieving extreme timing performance. 

The cache consists of 1024 tags (256 x 4), has line width of 8 words. It maintains dirty indication and least recently used (LRU) replacement policy, and is able to react on a microcontroller transaction in 6 clocks, which is what makes the design not suitable for practical use.

![image](https://user-images.githubusercontent.com/23367640/158000525-5789ddb9-baf4-4110-b974-e8759c99a4ad.png)
