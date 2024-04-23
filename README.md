# reverse-bit
public class Solution {
    // you need treat n as an unsigned value
    public int reverseBits(int n) {
        int reversed = 0;
        int bitLength = 32; // Assuming 32-bit integers
        
        for (int i = 0; i < bitLength; i++) {
            // Shift the reversed bits to the left
            reversed <<= 1;
            
            // Extract the least significant bit of n and add it to reversed
            reversed |= (n & 1);
            
            // Shift n to the right to process the next bit
            n >>>= 1; // Unsigned right shift
        }
        
        return reversed;
    }
}
