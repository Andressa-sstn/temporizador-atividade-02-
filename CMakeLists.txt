cmake_minimum_required(VERSION 3.12)

# Define o projeto e o tipo de projeto
project(led_button)

# Defina onde está o Pico SDK
set(PICO_SDK_PATH "/path/to/pico-sdk")  # Alterar para o caminho correto

# Inclui o Pico SDK
include($ENV{PICO_SDK_PATH}/external/pico_sdk_import.cmake)

# Cria o executável
add_executable(led_button main.c)

# Linka o SDK necessário
target_link_libraries(led_button pico_stdlib hardware_irq)

# Cria o arquivo .uf2 para o Raspberry Pi Pico
pico_add_extra_outputs(led_button)
