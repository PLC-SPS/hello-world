# include "KORD-Shield"  
volatile bool Merker = 0;  

void setup() {  
pinMode(BUTTON0, INPUT_PULLUP);  
attachInterrupt(digitalPinToInterrupt(BUTTON0), pushwait, LOW); //1.Argument: Unser Eingangs-PIN/Taster, 2. Argument: Funktion siehe unten, 3. Argument: beim wechseln auf LOW-Zustand beim drücken  

void pushwait(){  
Merker++;  
}
