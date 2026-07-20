# FreeRTOS on STM32 — Hands-On RTOS Labs

A progressive set of nine labs for learning real-time concepts with FreeRTOS on the
STM32 NUCLEO-F411RE, with scheduling behavior verified in SEGGER SystemView.

![Language](https://img.shields.io/badge/C-97%25-00599C?logo=c&logoColor=white)
![RTOS](https://img.shields.io/badge/RTOS-FreeRTOS-009900?logo=freertos&logoColor=white)
![MCU](https://img.shields.io/badge/MCU-STM32F411RE-03234B?logo=stmicroelectronics&logoColor=white)

## The idea

Each folder is a small, self-contained lab that introduces exactly one RTOS concept, so the
progression is easy to follow: start with a single task, then add scheduling, then
inter-task communication and synchronization. Where timing matters, I used SEGGER
SystemView to actually watch the scheduler and interrupts on a timeline rather than
guessing.

## Labs

| # | Folder | Concept |
|---|---|---|
| 001 | `001Tasks` | Task creation and the scheduler |
| 002 | `002LED_Tasks` | Driving hardware from a task |
| 003 | `003LED_Block_Tasks` | Blocking versus busy-waiting |
| 004 | `004LED_Periodic_Tasks` | Periodic scheduling with `vTaskDelayUntil` |
| 005 | `005LED_Task_Notify` | Lightweight task notifications |
| 006 | `006LED_Btn_ISR` | Signaling a task from an ISR |
| 007 | `007Task_Priorities` | Priorities and preemption |
| 008 | `008Queues_Timers` | Queues and software timers |
| 009 | `009Binary_Semaphore` | Semaphore-based synchronization |

## Hardware and tools

- Board: STM32 NUCLEO-F411RE (ARM Cortex-M4)
- IDE: STM32CubeIDE, on Ubuntu 20.04
- Tracing: SEGGER SystemView for the real-time task and ISR timeline

## Build and run

1. Open the lab folder you want in STM32CubeIDE.
2. Build and flash it to the NUCLEO board.
3. Optionally attach SEGGER SystemView to watch the scheduling live.

## Skills demonstrated

FreeRTOS, RTOS scheduling, tasks and priorities, queues, semaphores, software timers,
ISR design, ARM Cortex-M, and SEGGER SystemView.
