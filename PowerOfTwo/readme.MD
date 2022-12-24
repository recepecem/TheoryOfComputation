## A Turing Machine (TM) M that decides L = { 0^(2^𝑛) | n >= 0 } which is the language consisting of all strings of 0s whose length is a power of 2.

First, turn First 0 to 'blank symbol'. It will help us to accept 2^0 which is one '0', also it will be necessary later.
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/PowerOfTwo/part1.png)

Then, accept if input string is '0'. Also this state will be used later.
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/PowerOfTwo/part2.png)

After, turn every other 0 to x.
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/PowerOfTwo/part3.png)

Now, get back to the beginning.
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/PowerOfTwo/part4.png)

Finally, If no zeros left then accept it. Otherwise, repeat the process.
![answer](https://raw.githubusercontent.com/recepecem/TheoryOfComputation/main/PowerOfTwo/part5.png)

If your input is even but not power of 2 then you will be left with one 0 so it will be impossible to accept the input. For example if your input is 6*'0'<br>1) 000000<br>2) x0x0x<br>3) xxx0x<br>4) your machine will stuck in state q4 and will be rejected.
