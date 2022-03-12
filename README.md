# ASIC-FPGA-Verilog

ASIC, FPGA, Verilog projects and materials

# Sum Channels DSP ...

![image](https://user-images.githubusercontent.com/23367640/158000485-886cccb7-758b-4461-9776-41a24af29f23.png)

# DataCacheTagMechanism

![image](https://user-images.githubusercontent.com/23367640/158000525-5789ddb9-baf4-4110-b974-e8759c99a4ad.png)

1. Functionality

	This block is an example of logical implementation of the tag-mechanism of a 4-way set associative copyback data cache. However, it must be explicitly stated, that the system does not work with appropriate timing for a real cache design, i.e. one result at every clock. The design is done following standard methodology of splitting the logic in pipelines, in order to shorten the length of gates that the signal passes in one clock, instead of achieving extreme timing performance. 

	The cache consists of 1024 tags (256 x 4), has line width of 8 words. It maintains dirty indication and least recently used (LRU) replacement policy, and is able to react on a microcontroller transaction in 6 clocks, which is what makes the design not suitable for practical use.
