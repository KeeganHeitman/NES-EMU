Our understanding and usage of computers is highly benefitted by levels of abtraction. Abstraction in computer science is the way by which we
group together wires into gates and groupings of gates into CPU's and other components. Emulation is the process of working back several steps and creating "Emulations" of often more simple or different abstractions.

Emulating the NES will require programs mimicking the data highways or "Buses", the 6502 microprocessor, the cartridge processor, the mapping
functionality through the mapper. the PPU or picture processing unit, another "Bus" for the pictures, virtual screen, and the controller.

The 6502 uses assembly code which cannot be compiled natively an assembler program entitled CC65 must be used. The 6502 uses 6 registers
which are all 8 bit with the exception of the 16 bit program counter. 
the (A) accumulator which will handle arithmetic and logic it can also read and write to memory
the (X) index which can read and write to memory, it is primarily used as the counter in loops, or for addressing memory, but can temporarily store
data
the (Y) index very similar but not interchangable with the X index. the X and Y registers have their own respective operations that are not
mutually inclusive
the (P) for flag which are 7 bits representing the status of the processor
the (S) for stack pointer which holds the address to the current location on the stack. The stack is a way to store data by pushing or popping data
from a section of memory
the (PC) for program counter which keeps track of the processors current location within a program.

STACK
the stack is a set of data structures used to store values and retrieve them in reverse order. CPUs use stacks in subroutines which call other
subroutines and programs use them to store data for later use and pass arguments to subroutines. Stacks have two operations including PUSH
which will add a value, and pull or pop to retrieve and remove a value. Stacks may also support peek, or retrieve a value n number of positions
from the top without removing it. Stacks can be placed on top of an array or linked list. some elements will be used and others unused, an array
index called the STACK POINTER sets the boundary between used and unused elements. Two types of stacks can be placed on top of an array or linked list a descending stack or one growing downward OR an ascending stack or one that grows upward. The 6502 will use a DESCEDING stack 

the NES PPU or picture processing unit generates a composite video signal with 240 lines of pixels. It has its own address space which contains
10 kB of memory, 8 kB of ROM or RAM on the Game Pak to store the shapes of background and sprite tiles plus 2 kB of RAM in the console to store a map or two. two seperate smaller addresses will contain a pallette which controls what colors are assocaited to varuous indices and OAM object attribute memory which stores position, orientation, shape, and color of the sprites or independent moving objects. These are internal to the PPU itself and while the pallette is made of static memory the OAM uses dynamic memory which will slowly decay if the PPU is not rendering data.
