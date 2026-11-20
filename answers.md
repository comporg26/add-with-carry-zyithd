# Answers — second 6502 lab

Please write your answers below each question.

1. What did the program return when it calculated 255 + 1? Why was the answer not 256?

   Answer: 0 because it can only store 8 bits

2. In the trace of 255 + 1, what was the value of A after `ADC`? Was the carry flag set or clear? How could you tell?

   Answer: the value of A was 0, and the flag was set, i can tell because we wanted to store 9 bits

3. How do `i_low` and `i_high` together represent the number 11969? Why do we need two bytes?

   Answer: i low contains $C1 and i high contains $2E and together it is $2EC1 which is the hex for 11969, we need two bytes to be able to store such a big number

4. Why must we **not** clear the carry flag between adding the low bytes and the high bytes?

   Answer: clearing would discard of the bit we might need

5. What values did your program store in `result_low` and `result_high`? What did the trace show about the carry after the low-byte addition?

   Answer: $58 which is 88 and $46 which is 70

6. What happened when you temporarily inserted `CLC` before the high-byte addition? Why?

   Answer: the first one turned into $45 because one byte was cleared and the second one didnt change because no byte was removed

7. (Optional) What happened when you added `$00FF` and `$0001`? What were the two result bytes?

   Answer: $0100 where first 2 are low, and 00 is high, a carry was produced and was added to the high byte
