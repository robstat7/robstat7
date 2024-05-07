```assembly
format elf64

extrn printk

public print_msg

section '.text' executable

print_msg:
		mov rdi, msg
		call printk
		ret

section '.data' writable

msg db "_/\_ Creating Raam kernel _/\_", 10, 0
```
