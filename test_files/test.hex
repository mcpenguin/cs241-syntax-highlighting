; $1 starting address of array (never changed)
; $2 number of elements in the array (preserved)
; $3 result (not preserved)
; $4 and $5 are used as temporary registers
; push all registers we change
; could have been more efficient and only pushed as needed
sw $2, -4($30)
sw $4, -8($30)
sw $5, -12($30)
sw $31,-16($30)
lis $4
.word 16
sub $30, $30, $4
add $3,$0,$0 ; clear $3 the result
beq $2, $0, end ; N = 0 so done
slt $4, $2, $0 ; $4 is 1 if N < 0
lis $5
.word 1
beq $5, $4, end ; N < 0 so done

; if we get here we need a recursive call
sub $2, $2, $5 ; N = N - 1
lis $5
.word Sum
jalr $5 ; result of call will be in $3
lis $4 ; retrieve a[N-1], recall $2 is already N-1
.word 4
mult $2, $4
mflo $5 ; 4(N-1)
add $5, $1, $5 ; address of a[N-1]
lw $5, 0($5) ; a[N-1]
add $3, $3, $5 ; Sum(a,N-1) + a[N-1]
end:
; pop all registers we pushed
lis $4
.word 16
add $30, $30, $4
lw $2, -4($30)
lw $4, -8($30)
lw $5, -12($30)
lw $31,-16($30)
jr $31

