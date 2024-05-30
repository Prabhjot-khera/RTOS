# Real-Time Operating System (RTOS) for STM32 Nucleo-64 F401RE

## Project Overview
This project is aimed at developing a Real-Time Operating System (RTOS) for multi-threading on an STM32 Nucleo-64 F401RE board. The RTOS provides a framework to manage multiple tasks, ensuring that critical tasks meet their deadlines while efficiently utilizing the processor's resources.

## Project Structure

```
Real-Time Operating System/
│
├── .settings/
│
├── Core/
│ ├── Inc/
│ └── Src/
│ ├── asmDump.s
│ ├── main.c
│ ├── stm32f4xx_hal_msp.c
│ ├── stm32f4xx_it.c
│ ├── syscalls.c
│ ├── sysmem.c
│ └── system_stm32f4xx.c
│
├── Startup/
│
├── Drivers/
│
├── .cproject
├── .gitignore
├── .mxproject
├── .project
├── FirstProject Debug.launch
├── Real-Time Operating System.ioc
├── STM32F401RETX_FLASH.ld
├── STM32F401RETX_RAM.ld
└── README.md
```

### Directory and File Descriptions

- **.settings/**: Contains project-specific settings.
- **Core/**: Contains the core files and source code for the RTOS.
  - **Inc/**: Header files.
  - **Src/**: Source files.
    - **asmDump.s**: Assembly dump file.
    - **main.c**: Main program body.
    - **stm32f4xx_hal_msp.c**: HAL MSP initialization file.
    - **stm32f4xx_it.c**: Interrupt handlers.
    - **syscalls.c**: System call interface.
    - **sysmem.c**: Memory management.
    - **system_stm32f4xx.c**: System initialization.
- **Startup/**: Contains startup files.
- **Drivers/**: Contains the drivers required for the hardware peripherals.
- **.cproject**: Eclipse CDT project file.
- **.gitignore**: Specifies files and directories to be ignored by Git.
- **.mxproject**: STM32CubeMX project file.
- **.project**: Eclipse project file.
- **FirstProject Debug.launch**: Debug configuration file.
- **Real-Time Operating System.ioc**: STM32CubeMX configuration file.
- **STM32F401RETX_FLASH.ld**: Linker script for flash memory.
- **STM32F401RETX_RAM.ld**: Linker script for RAM.
- **README.md**: Project documentation file.

## Getting Started

### Prerequisites
- **Hardware**: STM32 Nucleo-64 F401RE board.
- **Software**:
  - [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
  - [STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html)
  - [GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm)

### Installation

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/your-username/rtos-stm32.git
Open the Project in STM32CubeIDE:

Launch STM32CubeIDE.
Open the cloned repository as an existing project.
Configure the Project:

Open the .ioc file in STM32CubeMX to configure the peripherals and generate code.
Build and Debug:

Build the project in STM32CubeIDE.
Connect your STM32 Nucleo-64 F401RE board.
Debug the project using the provided debug configuration.
Usage
Multi-threading: The RTOS allows creating multiple threads/tasks. You can define tasks in the Core/Src directory.
Task Management: Use the provided API to manage tasks, including task creation, deletion, and scheduling.
Inter-task Communication: Utilize message queues, semaphores, and mutexes for inter-task communication.
