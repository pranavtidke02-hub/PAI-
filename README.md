# PAIL-Ubantu
PAIL assignment
 # ASM code for hello world
 global _start

section .data
    hello db "Hello, World!", 10
    length equ $ - hello

section .text
_start:
    mov eax, 4
    mov ebx, 1
    mov ecx, hello
    mov edx, length
    int 0x80

    xor ebx, ebx
    mov eax, 1
    int 0x80






    # Print Name
    global _start

section .data
    firstName db "Harsh", 10
    firstLen  equ $ - firstName

    lastName  db "Walia", 10
    lastLen   equ $ - lastName

section .text
_start:
    mov eax, 4
    mov ebx, 1
    mov ecx, firstName
    mov edx, firstLen
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, lastName
    mov edx, lastLen
    int 0x80

    mov eax, 1
    xor ebx, ebx
    int 0x80








# GDB use
(gdb) break _start
(gdb) run
(gdb) set disassembly-flavor intel
(gdb) disassemble _start
(gdb) layout asm
(gdb) layout regs
(gdb) nexti

#BASIC AIRTHEMETIC OPERATIONS

section .data

result db 0 

section .bss
section .text
global _start 

_start:

mov eax, num1 4A
mov ebx, num2 6B


add al, bl 


mov [result], al 


mov eax, 1 
xor ebx, ebx 
int 0x80

#ADDITION OF 16-BIT 
global _start:
section .text
_start:
	mov ax , 30FAH
	MOV bx , 595BH
	add ax, bx
