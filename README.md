COMPANY: CODTECH IT SOLUTIONS

NAME: Farida Sayyad

INTERN ID: :CT6WJJR

*DOMAIN*: VLSI

DURATION: 6 WEEEKS

MENTOR: NEELA SANTOSH

This repository contains a comprehensive Verilog implementation of a digital FIR (Finite Impulse Response) filter along with a testbench to simulate and verify its operation. The FIR filter designed here is a 4-tap filter that demonstrates the fundamental concepts of digital filtering in hardware. By using fixed coefficients and a simple multiply–accumulate structure, the design serves as an excellent starting point for those learning about digital signal processing (DSP) in FPGAs or ASICs.

The FIR filter operates by convolving the input signal with a set of predetermined coefficients. In our design, the coefficients are chosen as h₀ = 1, h₁ = 2, h₂ = 2, and h₃ = 1, which form a symmetric impulse response. This symmetry is common in many low-pass filter designs, ensuring linear phase characteristics. The filter's output, computed as y[n] = h₀·x[n] + h₁·x[n–1] + h₂·x[n–2] + h₃·x[n–3], is generated every clock cycle using a shift register that stores the most recent input samples. The multiply–accumulate operation is performed synchronously on the rising edge of the clock, ensuring predictable behavior that is easy to analyze and simulate.

Key features of the design include parameterized data width and tap count. By modifying these parameters, the filter can be easily scaled to meet various application requirements. The module is written in synthesizable Verilog and includes an asynchronous reset for initialization. This makes it suitable for integration into larger digital systems where digital filtering is required.

The repository is organized into clearly defined sections. The source code is located in the main directory, with the FIR filter module (fir_filter.v) and the accompanying testbench (fir_filter_tb.v) provided. Extensive inline comments explain the function of each part of the design, from the shift register operations to the final multiply–accumulate computation. This documentation is aimed at helping beginners understand the inner workings of digital filters, while also offering enough detail for experienced designers to adapt and extend the design.

The testbench applies an impulse to the filter and then sets the input to zero, allowing users to observe the filter’s impulse response over time. Simulation waveforms will show the gradual build-up and decay of the output as the filter “remembers” the input impulse across its taps. This behavior is critical in understanding how FIR filters process transient signals and can be used to design more complex filtering algorithms.

Potential future enhancements for this project include expanding the filter to support a larger number of taps, implementing coefficient loading for dynamic filter design, or even porting the design to MATLAB for algorithm verification. Contributions are welcome, and users are encouraged to fork the repository, suggest improvements, or adapt the design for specific DSP applications.

Output:
![Image](https://github.com/user-attachments/assets/ae2b81a1-9f05-41bb-9b3b-27080b4908bf)
