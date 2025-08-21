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


 #MULTIPLICATION OF 8-BIT
 global _start
section .text

_start:
    mov al, 10     
    mov bl, 100     
    mul bl


 #MULTIPLCATION USING AAM
 global _start
section .data
    val db 0
    vah db 0

section .text
_start:
    mov al,5
    mov bl,9
    mul bl

    aam
    add al,'0'
    mov [val],al
    add ah,'0'
    mov [vah],ah

    mov eax,4
    mov ebx,1
    mov ecx,vah
    mov edx,1
    int 80h

    mov eax,4
    mov ebx,1
    mov ecx,val
    mov edx,1
    int 80h

    mov eax,1
    mov ebx,0
    int 80h
