#### Description

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)
**Solucion**



Y vamos a usar una pista que nos da la cual es 
After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

despues de descargarlo lo vamos a descomprimir
y luego le vamos a dar cd y los tabs hasta que no de más, le damos un ls para ver los arvchivos y ahi le damos un cat al archivo para ver que contine y entre todo el texto esta nuestra bandera

Luiscat02-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
8#TT 1tt$DN: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
0)@creat(;Luiscat02-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
Luiscat02-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
Luiscat02-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
Luiscat02-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ cat fang-of-haynekhtnamet 
 HH/lib64/ld-linux-x86-64.so.2GNUGNU_
'
 Ϲn= 
       H "libc.so.6puts__cxa_finalize__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMCloneTable__gmon_start___ITM_registerTMCloneTableui   1
 Ht5
 %
 @%
 h%
H=1I^HHPTLH
 DH=
 UH
 H9HtHZ
]f.]@f.H=i
 H5b
 UH)HHHH?HHtH!
 Ht
   ]f]@f.=
 u/H=    UHt
H        ]fDUH]fUHH=]f.DAWAVIAUATL%F UH-F SAIL)HWHt 1LLDAHH9u[]A\A]A^A_Ðf.*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}X"H0zRx
                                                                                                                               Rx
                                                                                                                                 FJ
R                                                                                                                                  ?;*3$"D\RAC
D|XeBBE B(H0H8M@r8A0A(B BB0
o`

 GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt`


    
  $ z  @R Yx  `e ~0+ :  "
                         crtstuff.cderegister_tm_clones__do_global_dtors_auxcompleted.7698__do_global_dtors_aux_fini_array_entryframe_dummy__frame_dummy_init_array_entryfang-of-haynekhtnamet.c__FRAME_END_init_array_end_DYNAMIC__init_array_start__GNU_EH_FRAME_HDR_GLOBAL_OFFSET_TABLE___libc_csu_fini_ITM_deregisterTMCloneTableputs@@GLIBC_2.2.5_edata__libc_s
                         
                         
                         art_main@@GLIBC_2.2.5__data_start__gmon_start____dso_handle_IO_stdin_used__libc_csu_init__bss_startmain__TMC_END___ITM_registerTMCloneTable__cxa_finalize@@GLIBC_2.2.5.symtab.strtab.shstrtab.interp.note.ABI-tag.note.gnu.build-id.gnu.hash.dynsym.dynstr.gnu.version.gnu.version_r.rela.dyn.rela.plt.init.plt.got.text.fini.rodata.eh_frame_hdr.eh_frame.init_array.fini_array.dynamic.data.bss.comment
**NOTAS ADICIONALES:**

- Comando `wget`: Permite descargar archivos desde la web.
- Comando `unzip`: Descomprime archivos `.zip`.
- Comando `cd`: Cambia de directorio.
- Comando `ls`: Muestra los archivos en un directorio.
- Comando `cat`: Muestra el contenido de un archivo.
- La clave de este reto fue utilizar la función de Tab-completion para navegar rápidamente por una estructura de directorios larga y compleja.
BANDERA
==picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}==


referencias
https://www.youtube.com/watch?v=2-8lETOcLBM&pp=ygUYVGFiLCBUYWIsIEF0dGFjayBwaWNvY3Rm