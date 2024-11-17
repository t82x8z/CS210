java c
CS210 Fall 2024: PS4A
Multiple Choice
1.  (1 point)  An executable created by the C toolchain    ⃝  requires preprocessing before it can be run ⃝  can be run on any operating system
⃝  is composed of C statements ⃝  can be run on any computer
⃝  all of the above     ⃝  none of the above
2.  (1 point)  What must be passed to printf to send bytes to standard output ⃝  a format specifier⃝  a char pointer to a format string   ⃝  file descriptor of standard output ⃝  size of bytes you want to send
⃝  all of the above     ⃝  none of the above
3.  (1 point)  By the C calling conventions,  if more than 6 arguments are passed into a C function, the remaining ones, that could not be assigned to registers, are pushed onto the stack
⃝  True  ⃝  False
4.  (1 point)  Two’s complement⃝  is convention that allows positive and negative quantities to be represented using a binary vector
⃝  does not support additive inverses
⃝  defines both a positive and negative zero value using a single binary vector ⃝  defines the same amount of positive and negative values
⃝  all of the above     ⃝  none of the above
5.  (1 point)  When using the C language the only way to send a sequence of ASCII encoded data to stan- dard out is printf.
⃝  True  ⃝  False
6.  (1 point)  The indirection operator, in C,
⃝  provides access to the value that a pointer is pointing to ⃝  provides the address of a value
⃝  provides the type of a value ⃝  provides the size of a value
⃝  all of the above     ⃝  none of the above
7.  (1 point)  On Linux the heap is
⃝  automatically created an added to every process
⃝  is established using an system call ⃝  is of a fixed size
⃝  is used for all initialized data ⃝  all of the above
⃝  none of the above
8.  (1 point)  A function can be defined in many files ⃝  True
⃝  False
9.  (1 point)  In a C function, a local variable
⃝  will be placed in the heap if there are no available registers or space on the stack ⃝  will be assigned to a register or placed on the stack
⃝  must be place on the stack
⃝  must be assigned to a register ⃝  none of the above
10.  Provide the following value of the C expressions ”as a 32bit hexadecimal value.
DO NOT SKIP LEADING ZEROS:
Eg. a value of 0 should be written as 00000000 and 1 as 00000001.Assume a 64 bit computer that uses 2’s complement representation, INT MAX and INT MIN are de- fined as the computer’s signed 32 bit integer representation maximum and minimum value respectively, and:
int  x  = INT MIN, y = 0xdecafbad, z  = INT MAX, i = (sizeof(char *)  +  sizeof ( int   *));
(a)  (1 point)  x : 0x                                                                                         
(b)  (1 point)  y : 0x                                                                                         
(c)  (1 point)  z : 0x                                                                                          
(d)  (1 point)  i : 0x                                                                                         
(e)  (1 point)  z<<3 : 0x                                                                                         
(f)  (1 point)  z<<((i>>1)−1 ) : 0x                                                                                         
(g)  (1 point)  ˜0  == (z  + INT MIN) : 0x                                                                                        
(h)  (1 point)  y   0 xffff  : 0x                                                                                         
(i)  (1 point)  y  >> 16 : 0x                                                                                      
(j)  (1 point)  (y>>16) |  0 xffff : 0x                                                                                       
(k)  (1 point)  (˜(0 x10>>2)+1) == −(i>>2) : 0x                                                                                         
(l)  (1 point)   (˜ z+1) + −1 : 0x                                                                                         
(m)  (1 point)   (˜((˜ x)<<1))  y : 0x                                                                                      
(n)  (1 point)  (( y<<3)+INT MIN) ˆ ((y<<3)+INT MIN) : 0x                                                                                         
11.  (5 points)  Given the  assembly code on the left fill in the blanks in the C code on the right that it corresponds to.
1 . i n t e l s y n t a x n o p r e f i x
2 . t e x t
3 . g l o b l fu n c
4 fu n c :
5 xor eax , eax
6 xor r8d , r8d
7 .L2 :
8 add r8d , DWORD PTR A[0+ r a x *4]
9 i n c r a x
10 cmp rax , 10
11 jne .L2
12 mov eax , r8d
13 r e t
1
2 # d e f i n e B
3
4 # d e f i n e T
5
6 T A[B ] ;
7
8 T fu n c ( )
9 {
10 i n t i ;
11 T s = 0 ;
12
13 f o r ( ;
14
15 i < B ;
16
17 ) {
18
19
20 s = ;
21 }
22 return s ;
23 }


12.  (6 points)  Given the  assembly code on the left fill in the blanks in the C code on the right that it corresponds to.
1 . i n t e l s y n t a x n o p r e f i x
2 . t e x t
3 . g l o b l fu n c


4 fu n c :
5 xor rax , r a x
6 .L2 :
7 t e s t r d i , r d i
8 j e .L7
9 mov rcx , DWORD PTR [ r d i +8]
10 mov rdx , DWORD PTR [ r d i +16]
11 cmp r s i , 12
12 jg .L3
13 add rax , DWORD PTR [ r d i ]
14 mov r d i , r c x
15 jmp .L2
16 .L3 :
17 add rax , DWORD PTR [ r d i +4]
18 mov r d i , rdx
19 jmp .L2
20 .L7 :
21 r e t
1 s t r u c t S {
2 i n t x ;
3 i n t y ;
4 s t r u c t S * f ;
5 s t r u c t S *b ;
6 } ;
7
8 i n t
9 fu n c ( s t r u c t S *h ,
10 long long v )
11 {
12 i n t r = 0 ;
13
14 while ( h != ) {
15 i f ( v > ) {
16
17 r = r + ;
18
19 h = ;
20 } e l s e {
21
22 r = r + ;
23
24 h = ;
25 }
26 }
27 return r ;
28 }
13.  (4 points)  Given the  assembly code on the left fill in the blanks in the C code on the right that it corresponds to.
14.  Present the output for each line from the below program. Assuming that it is compiled and executed on
a 64 bit, little endian computer that uses 2’s complement representation.
#include  
typedef  unsigned  char  *byte_pointer ;
void  show_bytes (byte_pointer  start ,  int  len)  { int  i ;
for (i=0;  iprintf ( "  % .2x " ,  start [i]);
printf ("\n " ); }
int  main (void) {
unsigned  int  ux  =  0xfffffff8; int  x  =  ux ;
long  long  unsigned  uy  =  ux ; long  long  y  =  x ;
ux  =  ux  >>  1; x    =  x  >>  1;
printf ( "%lu  %lu\n " ,  sizeof (ux),  sizeof (uy )); show_bytes ((byte_pointer)uy ,  sizeof (uy ));
printf ( " 0x%x  0x%llx\n " ,  x ,  y ); printf ( "%d  %lld\n " ,  x ,  y );
return  0; }
(a)  (2 points)                                                                                                                                               
(b)  (2 points)                                                                                                                                               
(c)  (2 points)                                                                                                                                               
(d)  (2 points)                                                                                                                                               15.  Assume that the code below is compiled for and executed on a 64-bit little endian computer.  Pleaseprovide the hex byte value and name of the variable that each address indicated corresponds to.  For addresses that correspond to arrays please indicate the array name and index the address belongs to.  Eg.  str[4].  If an address does not correspond to a variable leave the name blank empty. For char variables the value should be provide as an ASCII character. Eg.  ’a’  . For all other variables the values should be provide as a two digit hex value.
char    foo []  =  "DEADBEEF " ; int       j    =  0xDEADBEEF;
short  s    =  0xDEED;
short  *  sp  =  s ;
char    *  cp  =  (foo [12]);
void  func () {
*cp  =  ’D ’ ;
cp  =   (char  *)s ; cp  =  cp  -  2;
*cp  =  0xea ;
*sp  =  0x4224; }VariableAddress of Variable
foo
0x0000555555558010
j
0x000055555555801c
s
0x0000555555558020
sp
0x0000555555558028
cp
0x0000555555558030
Given the above fill in the following
(1)  0x0000555555558010: Value:                            Name:                          
(2)  0x0000555555558011: Value:                            Name:                          
(3)  0x0000555555558012: Value:                            Name:                          
(4)  0x0000555555558013: Value:                            Name:                          
(5)  0x0000555555558014: Value:                            Name:                          
(6)  0x0000555555558015: Value:                            Name:                          
(7)  0x0000555555558016: Value:                            Name:                          
(8)  0x0000555555558017: Value:                            Name:                          
(9)  0x0000555555558018: Value:                            Name:                          
(10)  0x0000555555558019: Value:                            Name:                          
(11)  0x000055555555801a: Value:                            Name:                          
(12)  0x000055555555801b: Value:                            Name:                          
(13)  0x000055555555801c: Value:                            Name:                          
(14)  0x000055555555801d: Value:                            Name:                          
(15)  0x000055555555801e: Value:                            Name:                          
(20)  0x0000555555558023: Value:                            Name:                          
(21)  0x0000555555558024: Value:                            Name:                          
(22)  0x0000555555558025: Value:                            Name:                          
(23)  0x0000555555558026: Value:                            Name:                          
(24)  0x0000555555558027: Value:                            Name:                          
(25)  0x0000555555558028: Value:                            Name:                          
(26)  0x0000555555558029: Value:                            Name:                          
(27)  0x000055555555802a: Value:                            Name:                          
(28)  0x000055555555802b: Value:                            Name:                          
(29)  0x000055555555802c: Value:                            Name:                          
(30)  0x000055555555802d: Value:                            Name:                          
(31)  0x000055555555802e: Value:                            Name:                          
(32)  0x000055555555802f: Value:                          Name:                          
(33)  0x0000555555558030: Value:                            Name:                          
(34)  0x0000555555558031: Value:                            Name:                          
16.  (12 points)  Given the following code complete the diagram on the next page assuming main runs to completion. Fill in all blank boxes, either with an arrow or value as needed. A
# in c lud e  < s t d lib . h>
s tru c t   my Struct   {s tru c t   my Struct   *p0 ; s tru c t   my Struct   *p1 ; s tru c t   my Struct   *p2 ; ch ar                              *cp ;
in t                                    v al ; } ;
s tru c t   my Struct   *  new ( ) {
s tru c t   my Struct   * sp   =   mall oc ( s iz e o f ( s tru c t   my Struct ) ) ; sp −>p0  =   0 ;   sp −>p1 = 0 ;   sp −>p2 = 0 ;   sp −>cp = 0 ;   sp −>v al = 0 ;
r e turn   s p ;
}s tru c t   my Struct   * r ; s tru c t   my Struct   * s ; s tru c t   my Struct   * t ;
in t   main ( in t   ar gc ,   ch ar   ** arg v ) {
s   =  new ( ) ;
s −>p0  =  new ( ) ;
s −>p0−>p2  =  new ( ) ;
s −>p0−>p2−>p1  =  new ( ) ; s −>p0−>p2−>p0  =   s −>p0 ;
r =s −>p0−>p2−>p1 ; s −>p1  =  new ( ) ;
r −>p0  =  new ( ) ;
r −>p0−>p2  =  new ( ) ;
r −>p0−>p2−>p2  =  new ( ) ; t   =  new ( ) ;
s −>p0−>p2−>p1−>p0−>p2−>v al   =   2 1 ; t −>v al   =   4 2 ;
s −>p2  =   t ;
s −>p0−>p2−>p0−>p2−>p1−>p0−>p2−>v al   =   3 ; r e turn   0 ;
}


         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
