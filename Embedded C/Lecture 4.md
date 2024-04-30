# Part 1
### Integer data types:

## integer promotion:
- when a type needed to extend its capacity, the compiler promote the small type into bigger one when using any operation on them, (short int, char) -> (int, unsigned int) as needed.
- it happens automatically while any operation, mathematically or logically ??!
- may the signed and unsigned char have the same binary representation value but when comparision value is different from signed char from (-128 to 127) so it is looped in those value, and the unsigned char form (0~255).
- it is like having representation value and actual value.

>[!tip]- clear any desired bit:
> - x &= ~(1 << required position);
>	- first you shift logical left to the one the reverse by not, it is like masking.
>	- begin from index 0 to (bit_no - 1).

>[!tip]- set any desired bit:
>- x |= (1 << required position);
> 	- you shift the one by required position then logical or and store in the same variable again.

>[!tip]- toggle any desired bit:
> - x ^= (1 << required position);
>	- you know that, المتشابة يساوي صفر والمختلف يساوي 1


==================================================================================================================

# part 3

### operators importance:
- up to down and left to right.
- ![[Pasted image 20240428203912.png]]



### important notes:
- printf function return an integer of a number of characters used.
- 