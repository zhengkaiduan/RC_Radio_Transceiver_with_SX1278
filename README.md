# RC_Radio_Transceiver_with_SX1278
 Radio Transceiver for RC ,Base on stm32f051k8 & SX1278 ,Support PPI,PWM,SBUS & Uart .

 This Radio Transceiver design for my 1/14 remote car. Base on STM32F051K8U6 MCU and Semtech SX1278 radio module. 


## Hardware 1.0

 Hardware 1.0 named " Remote_CAR_Reciver 1.0" . you can find out gaber files and schematic files at <\Hardware\gaber files >. MCU SPI1 connect to SX1278, TIM1 channel 1-4 connect to futaba header for user purpose.

Radio module using AS32-S433A20S2a(build by ashining) and working on 433MHz, module have low noising amplifier and a frequency switch, so module have Rx_EN and Tx_EN PIN for frequency switch.

Radio connection:
 	PA3:GPIO_IN		->	RF_DIO0
 	PA4:SPI1_NSS	->	RF_NSS
 	PA5:SPI1_SCK	->	RF_SCK
 	PA6:SPI1_MISO	->	RF_MISO
 	PA7:SPI1_MOSI	->	RF_MOSI
 	PB0:GPIO_OUT	->	RF_RXEN
 	PB1:GPIO_OUT	->	RF_TXEN
 	PB2:GPIO_OUT	->	RF_NRST

User PIN out 1:
 	PA8		->		PWM_CH1:	TIM1_CH1		->		
 	PA9		->		PWM_CH2:	TIM1_CH2		->		USART1_TX
 	PA10	->		PWM_CH3:	TIM1_CH3		->		USART1_TX
 	PA11	->		PWM_CH4:	TIM1_CH4		->		
 	PA15	->		IO_CH5:		GPIO_OUT1		->		
 	PB3		->		IO_CH6:		GPIO_OUT2		->		

For Reciver,Hardware 1.0 can offer 4 channel PWM output and 2 channel on-off output, and also can offer PPM(TIM1 input capture mode), sbus(USART1 Half-Duplex mode，TX pin internal inversion) or uart output.

For transmitter,Hardware 1.0 can offer  PWM input, sbus input or uart input.

User PIN out 2:
	PB6		->		I2C1_SCL
	PB7		->		I2C1_SDA

## Hardware 1.2

Hardware 1.2 base on Hardware 1.0, add on a external voltage regulator(FPDK12SR8004PSV) to help debug .