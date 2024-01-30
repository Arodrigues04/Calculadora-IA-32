
1. Assegure-se de ter o NASM instalado em um ambiente Linux e abra o terminal na 
pasta do projeto.

2.  Crie os arquivos objeto de cada módulo usando os seguintes comandos (copie e cole no terminal)

nasm -f elf calculadora.asm   -o calculadora.o 
nasm -f elf soma.asm          -o soma.o
nasm -f elf subtracao.asm     -o subtracao.o
nasm -f elf multiplicacao.asm -o multiplicacao.o
nasm -f elf divisao.asm       -o divisao.o
nasm -f elf exponenciacao.asm -o exponenciacao.o
nasm -f elf mod.asm           -o mod.o

Os argumentos para todas as operações são passados pela pilha,

3. Link os arquivos objetos principais com o comando (copie e cole no terminal)?

ld -m elf_i386 -o calculadora calculadora.o \
soma.o                                       \
subtracao.o                                  \
multiplicacao.o                              \
divisao.o                                    \
exponenciacao.o                              \
mod.o

    Se todas as etapas anteriores forem concluídas sem erros, será gerado um arquivo executável chamado calculadora.

4. Execute o executável gerado com o comando (copie e cole no terminal):


./calculadora

Isso deve iniciar a interação com o usuário conforme o esperado. Alternativamente, você pode montar, ligar e executar o trabalho usando o seguinte bloco único:


nasm -f elf calculadora.asm   -o calculadora.o 
nasm -f elf soma.asm          -o soma.o
nasm -f elf subtracao.asm     -o subtracao.o
nasm -f elf multiplicacao.asm -o multiplicacao.o
nasm -f elf divisao.asm       -o divisao.o
nasm -f elf exponenciacao.asm -o exponenciacao.o
nasm -f elf mod.asm           -o mod.o
ld -m elf_i386 -o calculadora calculadora.o \
soma.o                                       \
subtracao.o                                  \
multiplicacao.o                              \
divisao.o                                    \
exponenciacao.o                              \
mod.o
./calculadora
