from building import *
import os

cwd = GetCurrentDir()
path = [os.path.join(cwd, 'Inc')]
src_path = os.path.join(cwd, 'Src')

CPPDEFINES = ['USE_HAL_DRIVER']

src = [
os.path.join(src_path, 'stm32h7rsxx_hal.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_cec.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_cortex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_crc.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_crc_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_cryp.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_cryp_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_dma.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_dma_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_pwr.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_pwr_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_rcc.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_rcc_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_rng.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_sram.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_gpio.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_adc.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_adc_ex.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_xspi.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_flash.c'),
os.path.join(src_path, 'stm32h7rsxx_hal_flash_ex.c'),
]

if GetDepend(['RT_USING_SERIAL']) or GetDepend(['RT_USING_NANO', 'RT_USING_CONSOLE']):
    src += [os.path.join(src_path, 'stm32h7rsxx_hal_uart.c')]
    src += [os.path.join(src_path, 'stm32h7rsxx_hal_usart.c')]
    src += [os.path.join(src_path, 'stm32h7rsxx_hal_uart_ex.c')]

    
group = DefineGroup('STM32H7RS-HAL', src, depend = ['PKG_USING_STM32H7RS_HAL_DRIVER'], CPPPATH = path, CPPDEFINES = CPPDEFINES)

Return('group')
