## Modern Tetris

Will be updated as future progress continues.


## Overview

This project will implement two games playable on an 8x8 LED matrix. One will be a game of tetris and the other will be a simple balancing game.  This project will be done using the STM Discovery board and will use an external analog joystick to control falling tetris blocks. An additional peripheral, the HC-05 will be used to enter user commands via termite such as selecting what game to play.

## Materials
1) 8x8 LED Matrix
2) Analog Joystick
3) HC05 Bluetooth module
4) STM32 Discovery

## Used protocols: UART & SPI

## Design
The analog joystick will be connected to the ADC of the discovery board and the ADC will convert analog movement into something the LED matrix can understand. ie moving the joystick right will move an LED to the right. The up function will be reserved for rotating the piece clockwise 90 degrees. Moving the joystick generates an interrupt and that is how the board will know what direction to move the piece/LED in. For the balancing game, we will use SPI to have a visual representation of the gyroscope on the matrix. The movements on the gyroscope will correspond to movements on the LED matrix and the goal is to hold the LED steady for some amount of time. 


## Goals
Control each individual LED on the matrix
Write the actual tetris code in C
Correctly read values from joystick registers
