# Signed-and-Unsigned-Carry-Save-Multiplier

Implementation of a 4-Bit Carry Save Multiplier for both Signed and Unsigned Integers.

## Introduction

A carry-save multiplier is a type of digital multiplier circuit commonly used in computer arithmetic and digital signal processing applications. It performs high-speed multiplication of two binary numbers, typically represented as multi-bit binary words.

The carry-save multiplier architecture involves three main components: partial product generation stage, partial product accumulation stage, and final addition stage. It minimizes the critical path delay by postponing carry propagation until the final stage, enabling faster multiplication operations compared to traditional multiplier designs.

However, carry-save multipliers require additional hardware complexity and resources, leading to higher circuit area and power consumption.

## Block Diagrams

The carry-save multiplier implementation considers carry propagation to preceding stages instead of rippling the carry within the same stage. This involves parallel computation using half adders and full adders.

### Unsigned vs. Signed

In signed numbers, both the multiplier and multiplicand are represented in 2's complement format. The MSB of both contains the sign, where 1 indicates a negative number. Partial products associated with the MSB of both must be 2's complemented during addition. 

## Results

Test cases are provided for both signed and unsigned multipliers to compare their differences. These test cases cover all possible multiplication scenarios, including positive × positive, negative × negative, and mixed signs.

### Unsigned Multiplier

![Unsigned Multiplier Output](assets/unsigned_multiplier_output.png)

#### Signed and Unsigned Notation Comparison in Waveform

![Waveform Comparison](assets/waveform_comparison.png)

### Signed Multiplier

![Signed Multiplier Output](assets/signed_multiplier_output.png)

#### Signed Notation in Waveform

![Signed Waveform](assets/signed_waveform.png)

The signed notation implementation has a range from +7 to -8 (2^n-1 to -2^n), while the unsigned notation has a range from 15 to 0 (2^n-1 to 0).

## Conclusion

The implementation demonstrates the differences between signed and unsigned multiplication using carry-save multipliers. While unsigned multiplication yields valid results, signed multiplication requires careful handling of sign extension and 2's complement operations.

For further details, refer to the provided source code and accompanying documentation.

