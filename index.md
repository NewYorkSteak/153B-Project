## Modern Tetris

Will be updated as future progress continues.


## Overview
This project will use an 8x8 LED matrix with an external analog joystick to simulate a game of tetris. The project will be done using the STM Discpvery board; matrix will be used to display the blocks and the joystick will be used to control the falling blocks. An additional peripheral, the HC-05 will be used to display game information such as user or high score on termite.

## Materials
1) 8x8 LED Matrix
2) Analog Joystick
3) HC05 Bluetooth module
4) STM32 Discovery

## Used protocols: UART & SPI

## Design
The analog joystick will be connected to the ADC of the discovery board and the ADC will convert analog movement into something the LED matrix can understand. ie moving the joystick right will move an LED to the right and when in resting position, will make the block fall. The up function on the _onboard joystick_ will be used to force to block to fall all the way it can without waiting. This will be done via interrupt.

## Goals
Control each individual LED on the matrix
Write the actual tetris code in C
Correctly read values from joystick registers


## Progress
- Both X and Y directions of the joystick have been connected to the ADC
- Successfully enabled SPI communication with MAX 7219 display driver
- Enabled UART bluetooth communication with termite
- Success with controlling single dot across LED matrix using the joystick
- Created model for 4 different blocks
- Simulated falling block effect
- Functional tetris game using only one type of block
- Pseudorandom number generator function to pick differenet blocks
- Allowed different blocks to be spawned in the same game
- Bottom row correctly clears when it is full and shifts above rows down by 1
- Scrapped blancing game since SPI is already used to communicate with the LED matrix
