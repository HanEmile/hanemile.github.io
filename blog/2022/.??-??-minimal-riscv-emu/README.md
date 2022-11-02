# minimal riscv emu

::: toc

## primitives

### Error enum

### VM struct

- regs (32 * u32)
- pc (1 * u32)
- memory (MEMSIZE * u32)

## main

- define vm
- load elf
- exec vm
   - fetch instr.
   - parse opcode
   - match opcode and adjust registers accordingly
   - inc pc