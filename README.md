# RC_Radio_Transceiver_with_SX1278
 Radio Transceiver for RC ,Base on stm32f051k8 & SX1278 ,Support PPI,PWM,SBUS & Uart .

 This Radio Transceiver design for my 1/14 remote car. Base on STM32F051K8U6 MCU and Semtech SX1278 radio module. 


## Hardware 1.0

 Hardware 1.0 named " Remote_CAR_Reciver 1.0" . you can find out gaber files and schematic files at <\Hardware\gaber files >. MCU SPI1 connect to SX1278, TIM1 channel 1-4 connect to futaba header for user purpose.

Radio module using AS32-S433A20S2a(build by ashining) and working on 433MHz, module have low noising amplifier and a frequency switch, so module have Rx_EN and Tx_EN PIN for frequency switch.

Radio connection:
 	PA3:GPIO_IN		->	RF_DIO0\\\\
 	PA4:SPI1_NSS	->	RF_NSS\\\\
 	PA5:SPI1_SCK	->	RF_SCK\\\\
 	PA6:SPI1_MISO	->	RF_MISO\\\\
 	PA7:SPI1_MOSI	->	RF_MOSI\\\\
 	PB0:GPIO_OUT	->	RF_RXEN\\\\
 	PB1:GPIO_OUT	->	RF_TXEN\\\\
 	PB2:GPIO_OUT	->	RF_NRST\\\\

User PIN out:
 	PA8		->		TIM1_CH1\\\\
 	PA9		->		TIM1_CH2
 	PA10	->		TIM1_CH3
 	PA11	->		TIM1_CH4
 	PA15	->		GPIO_OUT1
 	PB3		->		GPIO_OUT2


## Hardware 1.2

Hardware 1.2 base on Hardware 1.0, add on a voltage regulator(FPDK12SR8004PSV).