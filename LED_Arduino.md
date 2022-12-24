# Designing an interface circuit to control LED light by push button switch using <ins>Arduino UNO</ins>.
## Requirements:- 
1) Arduino UNO board
2) LED
3) Arduino software
4) USB Cable

Here is a simple program for the working of the LED without a switch:- 
```C
void setup()
{
pinMode(15,OUTPUT); //LED
}
void loop()
{
digitalWrite(15,HIGH); // Make LED ON
delay(1000); // tells us for how much time(in milliseconds) the LED must be ON
digitalWrite(15,LOW); // Make LED OFF
delay(1000); // tells us for how much time the LED must be OFF
}
```
</br>

- Setup code will be executed only once whereas the loop code(main code) will run repeatedly.
- Making one delay value as zero, say for ON state, the LED will be OFF the whole time. If we do the same for OFF state, the LED will be ON the whole time.
- If we want different patterns to be displayed in LED, then we can use 'for' loop . For example:- Each time a for loop is executed, i can decrease/ increase the delay value by a factor. This will create a non-monotonous pattern.
- This <ins>Arduino software</ins> runs on C programming language. 
