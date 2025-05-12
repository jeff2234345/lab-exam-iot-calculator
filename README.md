Dawson College 
Electrical Engineering Technology Department 
Introduction to Internet of Things 
  
                           Project name: Arduino calculator 
                                
 
                               Antonio Lastoria – 2335234 
                              Jefferson Valdez – 2133663 
 
                                   
 
                                    Date of submission:  
                                          2025-05-11 
 	 







                                    2. Project description 
Meet this user, James, he is a student that is always busy doing homework, He always forgets where he puts his calculator, that’s why we made this smart calculator. A simple project that will let you do basic maths with a keypad and a small screen. 
How it works:  
-	The keypad will let you calculate numbers with the different operators (addition, substraction, multiplication and division) 
 
-	Depending on the operator you use, a certain color on the LED will light up 
                          
Figure 1 – Project diagram 	 

                                      


                                      3. Circuit Diagram 
Inputs: 
-	Arduino 4x4 keypad 
Outputs: 
-	RGB LED 
-	Arduino 16x2 LCD 
Table 1 – circuit connection 
Part 	Arduino uno pin 
keypad 	R1 - A0 
R2 - A1 
R3 - A2 
R4 - A3 
C1 - D4 
C2 - D5 
C3 - D6 
C4 - D7 
LED 	Red - D2 
Cathode - GND 
Blue - A5 
Green - A4 
LCD 	LED Cathode – 
Ground (-) 
LED Anode - (+5V) 
DB7 - D13 
DB6 - D12 
DB5 - D11 
DB4 - D10 
E - D9 
RW – Ground (-) 
RS - D8 
VCC - (+5V) 
GRD – Ground (-) 
 
Figure 2 – Circuit connection diagram 	 
                                   






                                  4. Code Documentation 
Library used: 
  
Global constants & pins: 
Constant/pin 	Purpose 
rowPins 	The rows in the keypad 
colPins 	The columns in the keypad 
 
Function responsibilities: 
Functions 	Responsibilities 
char keys([ROWS][COLS]) 	Maps the 4x4 keypad 
Void setRGB (bool r, bool g, bool b) 	The function to set the intensity of the colors red, green and blue. 
void handleKeyPress() 	It handles the key inputs from the keypad 
void calculateResult() 	Performs the calculation based on which operation is pressed on the keypad 
void displayResult() 	Shows the current result on the LCD display 
    
 



Code explanation: 
1.	Display message – On the LCD, we can see in the void setup(), lcd.print(“By Antonio,Jefferson”), which is the initiation. Then, there is a delay of 2 second before we can start using the calculator. 
 
2.	The keypad – with the numbers and the letters on the keypad, you can choose what equation you want to do 
 
3.	The RGB LED – In the code, there is multiple cases where, when you choose an operator, the LED light up. For example, pressing B, which is a substraction, will then call the function setRGB() to light the LED red. 
 
4.	Calculations – By pressing the equal sign key, “#”, It will return a value and with void displayResult(), it will display the answer on the LCD. 
 
5.	Restart – By clicking the clear sign, “*”, the LCD will clear the screen so it will be ready for the next equation. 





               Ethics, privacy, or security disclaimer 

This calculator is made for learning or personal use. It is not made to use during an exam. Please use it responsibly. 
Our project does not save or send data. Everything you do, stays on the device and disappears when you turn it off. No personal information will be collected. 
