# Save on CPX/CPB as code.py
# Blinks the top right RED LED
import board
import digitalio
import time

led = digitalio.DigitalInOut(board.LED)
led.direction = digitalio.Direction.OUTPUT

button = digitalio.DigitalInOut(board.BUTTON_B)
button.direction = digitalio.Direction.INPUT
button.pull = digitalio.Pull.DOWN

def main():
    
   print(dir(digitalio))

   print(dir(digitalio.DigitalInOut))

   print(dir(board))

   print(dir(led))

   print (dir(button))
   
   print(dir(digitalio.Direction))

   print(dir(digitalio.Pull))

   while True:

    led.value = button.value
    print(button.value)
    time.sleep(.2)
    
main()

