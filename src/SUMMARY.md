# Содержание

[Введение](README.md)

# Предисловие

- [О руководстве](preface.md)
- [Аудитория и соглашения](preface-audience.md)
- [Дополнительная литература](further-reading.md)

# 1. Введение

- [1.1. О контроллере UART](ch01-about.md)
  - [1.1.1. Особенности](ch01-features.md)
  - [1.1.2. Программируемые параметры](ch01-parameters.md)
  - [1.1.3. Отличия от UART 16C550](ch01-16c550.md)
- [1.2. Сведения о ревизиях продукта](ch01-revisions.md)

# 2. Функциональное описание

- [2.1. Обзор](ch02-overview.md)
  - [2.1.1. Блок IrDA SIR](ch02-irda-block.md)
- [2.2. Функциональное описание](ch02-functional.md)
  - [2.2.1. Интерфейс AMBA APB](ch02-apb.md)
  - [2.2.2. Блок регистров](ch02-register-block.md)
  - [2.2.3. Генератор скорости передачи](ch02-baud-rate.md)
  - [2.2.4. Передающий FIFO](ch02-tx-fifo.md)
  - [2.2.5. Принимающий FIFO](ch02-rx-fifo.md)
  - [2.2.6. Передающая логика](ch02-tx-logic.md)
  - [2.2.7. Принимающая логика](ch02-rx-logic.md)
  - [2.2.8. Логика формирования прерываний](ch02-interrupt-logic.md)
  - [2.2.9. Интерфейс DMA](ch02-dma.md)
  - [2.2.10. Синхронизация регистров и логики](ch02-synchronization.md)
  - [2.2.11. Тестовые регистры и логика](ch02-test-logic.md)
- [2.3. Функциональное описание IrDA SIR ENDEC](ch02-irda.md)
  - [2.3.1. Передающий кодер IrDA SIR](ch02-irda-encoder.md)
  - [2.3.2. Принимающий декодер IrDA SIR](ch02-irda-decoder.md)
- [2.4. Работа контроллера](ch02-operation.md)
  - [2.4.1. Сброс интерфейса](ch02-reset.md)
  - [2.4.2. Тактовые сигналы](ch02-clocks.md)
  - [2.4.3. Работа UART](ch02-uart-operation.md)
  - [2.4.4. Работа IrDA SIR](ch02-irda-operation.md)
  - [2.4.5. Кадр символа UART](ch02-character-frame.md)
  - [2.4.6. Модуляция данных IrDA](ch02-irda-modulation.md)
- [2.5. Работа модемных сигналов](ch02-modem.md)
- [2.6. Аппаратное управление потоком](ch02-flow-control.md)
  - [2.6.1. Управление потоком RTS](ch02-rts.md)
  - [2.6.2. Управление потоком CTS](ch02-cts.md)
- [2.7. Интерфейс DMA](ch02-dma-interface.md)

# 3. Модель программиста

- [3.1. Общие сведения](ch03-about.md)
- [3.2. Сводка регистров](ch03-summary.md)
- [3.3. Описание регистров](ch03-registers.md)
  - [3.3.1. Регистр данных UARTDR](ch03-uartdr.md)
  - [3.3.2. UARTRSR/UARTECR](ch03-uartrsr.md)
  - [3.3.3. Регистр флагов UARTFR](ch03-uartfr.md)
  - [3.3.4. Регистр IrDA UARTILPR](ch03-uartilpr.md)
  - [3.3.5. Целый делитель UARTIBRD](ch03-uartibrd.md)
  - [3.3.6. Дробный делитель UARTFBRD](ch03-uartfbrd.md)
  - [3.3.7. Регистр управления линией UARTLCR_H](ch03-uartlcr.md)
  - [3.3.8. Регистр управления UARTCR](ch03-uartcr.md)
  - [3.3.9. Выбор уровня FIFO UARTIFLS](ch03-uartifls.md)
  - [3.3.10. Маска прерываний UARTIMSC](ch03-uartimsc.md)
  - [3.3.11. Сырой статус UARTRIS](ch03-uartris.md)
  - [3.3.12. Маскированный статус UARTMIS](ch03-uartmis.md)
  - [3.3.13. Сброс прерываний UARTICR](ch03-uarticr.md)
  - [3.3.14. Управление DMA UARTDMACR](ch03-uartdmacr.md)
  - [3.3.15. Идентификация UARTPeriphID0-3](ch03-periphid.md)
  - [3.3.16. Идентификация UARTPCellID0-3](ch03-pcellid.md)
- [3.4. Прерывания](ch03-interrupts.md)
  - [3.4.1. UARTMSINTR](ch03-msintr.md)
  - [3.4.2. UARTRXINTR](ch03-rxintr.md)
  - [3.4.3. UARTTXINTR](ch03-txintr.md)
  - [3.4.4. UARTRTINTR](ch03-rtintr.md)
  - [3.4.5. UARTEINTR](ch03-eintr.md)
  - [3.4.6. UARTINTR](ch03-intr.md)

# 4. Модель программиста для тестирования

- [4.1. Обзор тестовой обвязки](ch04-overview.md)
- [4.2. Scan-тестирование](ch04-scan.md)
- [4.3. Сводка тестовых регистров](ch04-test-summary.md)
- [4.4. Описание тестовых регистров](ch04-test-registers.md)
  - [4.4.1. UARTTCR](ch04-tcr.md)
  - [4.4.2. UARTITIP](ch04-itip.md)
  - [4.4.3. UARTITOP](ch04-itop.md)
  - [4.4.4. UARTTDR](ch04-tdr.md)
- [4.5. Тестирование входов](ch04-inputs.md)
  - [4.5.1. Внутрикристальные входы](ch04-intra-inputs.md)
  - [4.5.2. Первичные входы](ch04-primary-inputs.md)
- [4.6. Тестирование выходов](ch04-outputs.md)
  - [4.6.1. Внутрикристальные выходы](ch04-intra-outputs.md)
  - [4.6.2. Первичные выходы](ch04-primary-outputs.md)
- [4.7. Итоги интеграционного тестирования](ch04-summary.md)

# Приложения

- [Приложение A. Описание сигналов](appendix-a.md)
  - [A.1. Сигналы AMBA APB](appendix-a1.md)
  - [A.2. Внутрикристальные сигналы](appendix-a2.md)
  - [A.3. Сигналы выводов](appendix-a3.md)
- [Приложение Б. Глоссарий](glossary.md)
