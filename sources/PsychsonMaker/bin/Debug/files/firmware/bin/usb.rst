                                      1 ;--------------------------------------------------------
                                      2 ; File Created by SDCC : free open source ANSI-C Compiler
                                      3 ; Version 3.5.0 #9253 (Jun 20 2015) (MINGW64)
                                      4 ; This file was generated Sat Jun 04 12:50:10 2016
                                      5 ;--------------------------------------------------------
                                      6 	.module usb
                                      7 	.optsdcc -mmcs51 --model-small
                                      8 	
                                      9 ;--------------------------------------------------------
                                     10 ; Public variables in this module
                                     11 ;--------------------------------------------------------
                                     12 	.globl _SetDMA_PARM_3
                                     13 	.globl _SetDMA_PARM_2
                                     14 	.globl _HandleUSBEvents
                                     15 	.globl _ep_isr
                                     16 	.globl _usb_isr
                                     17 	.globl _InitUSB
                                     18 	.globl _SendData1
                                     19 	.globl _SendData0
                                     20 	.globl _SendControlResponse
                                     21 	.globl _SetDMA
                                     22 	.globl _HandleVendorRequest
                                     23 	.globl _HandleClassRequest
                                     24 	.globl _HandleStandardRequest
                                     25 	.globl _HandleCDB
                                     26 	.globl _RI
                                     27 	.globl _TI
                                     28 	.globl _RB8
                                     29 	.globl _TB8
                                     30 	.globl _REN
                                     31 	.globl _SM2
                                     32 	.globl _SM1
                                     33 	.globl _SM0
                                     34 	.globl _RXD
                                     35 	.globl _TXD
                                     36 	.globl _INT0
                                     37 	.globl _INT1
                                     38 	.globl _T0
                                     39 	.globl _T1
                                     40 	.globl _WR
                                     41 	.globl _RD
                                     42 	.globl _PX0
                                     43 	.globl _PT0
                                     44 	.globl _PX1
                                     45 	.globl _PT1
                                     46 	.globl _PS
                                     47 	.globl _EX0
                                     48 	.globl _ET0
                                     49 	.globl _EX1
                                     50 	.globl _ET1
                                     51 	.globl _ES
                                     52 	.globl _EA
                                     53 	.globl _IT0
                                     54 	.globl _IE0
                                     55 	.globl _IT1
                                     56 	.globl _IE1
                                     57 	.globl _TR0
                                     58 	.globl _TF0
                                     59 	.globl _TR1
                                     60 	.globl _TF1
                                     61 	.globl _P
                                     62 	.globl _OV
                                     63 	.globl _RS0
                                     64 	.globl _RS1
                                     65 	.globl _F0
                                     66 	.globl _AC
                                     67 	.globl _CY
                                     68 	.globl _SBUF
                                     69 	.globl _SCON
                                     70 	.globl _IP
                                     71 	.globl _IE
                                     72 	.globl _TH1
                                     73 	.globl _TH0
                                     74 	.globl _TL1
                                     75 	.globl _TL0
                                     76 	.globl _TMOD
                                     77 	.globl _TCON
                                     78 	.globl _PCON
                                     79 	.globl _DPH
                                     80 	.globl _DPL
                                     81 	.globl _SP
                                     82 	.globl _B
                                     83 	.globl _ACC
                                     84 	.globl _PSW
                                     85 	.globl _P3
                                     86 	.globl _P2
                                     87 	.globl _P1
                                     88 	.globl _P0
                                     89 	.globl _usb_have_csw_ready
                                     90 	.globl _usb_received_data_ready
                                     91 	.globl _usb_buffer
                                     92 	.globl _PRAMCTL
                                     93 	.globl _BANK2PAH
                                     94 	.globl _BANK2PAL
                                     95 	.globl _BANK2VA
                                     96 	.globl _BANK1PAH
                                     97 	.globl _BANK1PAL
                                     98 	.globl _BANK1VA
                                     99 	.globl _BANK0PAH
                                    100 	.globl _BANK0PAL
                                    101 	.globl _WARMSTATUS
                                    102 	.globl _GPIO0OUT
                                    103 	.globl _GPIO0DIR
                                    104 	.globl _DMACMD
                                    105 	.globl _DMAFILL3
                                    106 	.globl _DMAFILL2
                                    107 	.globl _DMAFILL1
                                    108 	.globl _DMAFILL0
                                    109 	.globl _DMASIZEH
                                    110 	.globl _DMASIZEM
                                    111 	.globl _DMASIZEL
                                    112 	.globl _DMADSTH
                                    113 	.globl _DMADSTM
                                    114 	.globl _DMADSTL
                                    115 	.globl _DMASRCH
                                    116 	.globl _DMASRCM
                                    117 	.globl _DMASRCL
                                    118 	.globl _NANDCSDIR
                                    119 	.globl _NANDCSOUT
                                    120 	.globl _EP4
                                    121 	.globl _EP3
                                    122 	.globl _EP2
                                    123 	.globl _EP1
                                    124 	.globl _EP0
                                    125 	.globl _SETUPDAT
                                    126 	.globl _EP0CS
                                    127 	.globl _EPIE
                                    128 	.globl _EPIRQ
                                    129 	.globl _USBIRQ
                                    130 	.globl _USBSTAT
                                    131 	.globl _USBCTL
                                    132 	.globl _REGBANK
                                    133 	.globl _SendData1_PARM_2
                                    134 	.globl _SendData0_PARM_2
                                    135 	.globl _usb_speed
                                    136 	.globl _wLength
                                    137 	.globl _wIndex
                                    138 	.globl _wValue
                                    139 	.globl _bRequest
                                    140 	.globl _bmRequestType
                                    141 ;--------------------------------------------------------
                                    142 ; special function registers
                                    143 ;--------------------------------------------------------
                                    144 	.area RSEG    (ABS,DATA)
      000000                        145 	.org 0x0000
                           000080   146 _P0	=	0x0080
                           000090   147 _P1	=	0x0090
                           0000A0   148 _P2	=	0x00a0
                           0000B0   149 _P3	=	0x00b0
                           0000D0   150 _PSW	=	0x00d0
                           0000E0   151 _ACC	=	0x00e0
                           0000F0   152 _B	=	0x00f0
                           000081   153 _SP	=	0x0081
                           000082   154 _DPL	=	0x0082
                           000083   155 _DPH	=	0x0083
                           000087   156 _PCON	=	0x0087
                           000088   157 _TCON	=	0x0088
                           000089   158 _TMOD	=	0x0089
                           00008A   159 _TL0	=	0x008a
                           00008B   160 _TL1	=	0x008b
                           00008C   161 _TH0	=	0x008c
                           00008D   162 _TH1	=	0x008d
                           0000A8   163 _IE	=	0x00a8
                           0000B8   164 _IP	=	0x00b8
                           000098   165 _SCON	=	0x0098
                           000099   166 _SBUF	=	0x0099
                                    167 ;--------------------------------------------------------
                                    168 ; special function bits
                                    169 ;--------------------------------------------------------
                                    170 	.area RSEG    (ABS,DATA)
      000000                        171 	.org 0x0000
                           0000D7   172 _CY	=	0x00d7
                           0000D6   173 _AC	=	0x00d6
                           0000D5   174 _F0	=	0x00d5
                           0000D4   175 _RS1	=	0x00d4
                           0000D3   176 _RS0	=	0x00d3
                           0000D2   177 _OV	=	0x00d2
                           0000D0   178 _P	=	0x00d0
                           00008F   179 _TF1	=	0x008f
                           00008E   180 _TR1	=	0x008e
                           00008D   181 _TF0	=	0x008d
                           00008C   182 _TR0	=	0x008c
                           00008B   183 _IE1	=	0x008b
                           00008A   184 _IT1	=	0x008a
                           000089   185 _IE0	=	0x0089
                           000088   186 _IT0	=	0x0088
                           0000AF   187 _EA	=	0x00af
                           0000AC   188 _ES	=	0x00ac
                           0000AB   189 _ET1	=	0x00ab
                           0000AA   190 _EX1	=	0x00aa
                           0000A9   191 _ET0	=	0x00a9
                           0000A8   192 _EX0	=	0x00a8
                           0000BC   193 _PS	=	0x00bc
                           0000BB   194 _PT1	=	0x00bb
                           0000BA   195 _PX1	=	0x00ba
                           0000B9   196 _PT0	=	0x00b9
                           0000B8   197 _PX0	=	0x00b8
                           0000B7   198 _RD	=	0x00b7
                           0000B6   199 _WR	=	0x00b6
                           0000B5   200 _T1	=	0x00b5
                           0000B4   201 _T0	=	0x00b4
                           0000B3   202 _INT1	=	0x00b3
                           0000B2   203 _INT0	=	0x00b2
                           0000B1   204 _TXD	=	0x00b1
                           0000B0   205 _RXD	=	0x00b0
                           00009F   206 _SM0	=	0x009f
                           00009E   207 _SM1	=	0x009e
                           00009D   208 _SM2	=	0x009d
                           00009C   209 _REN	=	0x009c
                           00009B   210 _TB8	=	0x009b
                           00009A   211 _RB8	=	0x009a
                           000099   212 _TI	=	0x0099
                           000098   213 _RI	=	0x0098
                                    214 ;--------------------------------------------------------
                                    215 ; overlayable register banks
                                    216 ;--------------------------------------------------------
                                    217 	.area REG_BANK_0	(REL,OVR,DATA)
      000000                        218 	.ds 8
                                    219 ;--------------------------------------------------------
                                    220 ; internal ram data
                                    221 ;--------------------------------------------------------
                                    222 	.area DSEG    (DATA)
      00001A                        223 _bmRequestType::
      00001A                        224 	.ds 1
      00001B                        225 _bRequest::
      00001B                        226 	.ds 1
      00001C                        227 _wValue::
      00001C                        228 	.ds 2
      00001E                        229 _wIndex::
      00001E                        230 	.ds 2
      000020                        231 _wLength::
      000020                        232 	.ds 2
      000022                        233 _usb_speed::
      000022                        234 	.ds 1
      000023                        235 _SendData0_PARM_2:
      000023                        236 	.ds 1
      000024                        237 _SendData1_PARM_2:
      000024                        238 	.ds 1
                                    239 ;--------------------------------------------------------
                                    240 ; overlayable items in internal ram 
                                    241 ;--------------------------------------------------------
                                    242 	.area	OSEG    (OVR,DATA)
      000045                        243 _SetDMA_PARM_2:
      000045                        244 	.ds 1
      000046                        245 _SetDMA_PARM_3:
      000046                        246 	.ds 1
                                    247 	.area	OSEG    (OVR,DATA)
                                    248 ;--------------------------------------------------------
                                    249 ; indirectly addressable internal ram data
                                    250 ;--------------------------------------------------------
                                    251 	.area ISEG    (DATA)
                                    252 ;--------------------------------------------------------
                                    253 ; absolute internal ram data
                                    254 ;--------------------------------------------------------
                                    255 	.area IABS    (ABS,DATA)
                                    256 	.area IABS    (ABS,DATA)
                                    257 ;--------------------------------------------------------
                                    258 ; bit data
                                    259 ;--------------------------------------------------------
                                    260 	.area BSEG    (BIT)
                                    261 ;--------------------------------------------------------
                                    262 ; paged external ram data
                                    263 ;--------------------------------------------------------
                                    264 	.area PSEG    (PAG,XDATA)
                                    265 ;--------------------------------------------------------
                                    266 ; external ram data
                                    267 ;--------------------------------------------------------
                                    268 	.area XSEG    (XDATA)
                           00F000   269 _REGBANK	=	0xf000
                           00F008   270 _USBCTL	=	0xf008
                           00F009   271 _USBSTAT	=	0xf009
                           00F027   272 _USBIRQ	=	0xf027
                           00F020   273 _EPIRQ	=	0xf020
                           00F030   274 _EPIE	=	0xf030
                           00F048   275 _EP0CS	=	0xf048
                           00F0B8   276 _SETUPDAT	=	0xf0b8
                           00F1C0   277 _EP0	=	0xf1c0
                           00F200   278 _EP1	=	0xf200
                           00F240   279 _EP2	=	0xf240
                           00F280   280 _EP3	=	0xf280
                           00F2C0   281 _EP4	=	0xf2c0
                           00F608   282 _NANDCSOUT	=	0xf608
                           00F618   283 _NANDCSDIR	=	0xf618
                           00F900   284 _DMASRCL	=	0xf900
                           00F901   285 _DMASRCM	=	0xf901
                           00F902   286 _DMASRCH	=	0xf902
                           00F904   287 _DMADSTL	=	0xf904
                           00F905   288 _DMADSTM	=	0xf905
                           00F906   289 _DMADSTH	=	0xf906
                           00F908   290 _DMASIZEL	=	0xf908
                           00F909   291 _DMASIZEM	=	0xf909
                           00F90A   292 _DMASIZEH	=	0xf90a
                           00F90C   293 _DMAFILL0	=	0xf90c
                           00F90D   294 _DMAFILL1	=	0xf90d
                           00F90E   295 _DMAFILL2	=	0xf90e
                           00F90F   296 _DMAFILL3	=	0xf90f
                           00F930   297 _DMACMD	=	0xf930
                           00FA14   298 _GPIO0DIR	=	0xfa14
                           00FA15   299 _GPIO0OUT	=	0xfa15
                           00FA38   300 _WARMSTATUS	=	0xfa38
                           00FA40   301 _BANK0PAL	=	0xfa40
                           00FA41   302 _BANK0PAH	=	0xfa41
                           00FA42   303 _BANK1VA	=	0xfa42
                           00FA43   304 _BANK1PAL	=	0xfa43
                           00FA44   305 _BANK1PAH	=	0xfa44
                           00FA45   306 _BANK2VA	=	0xfa45
                           00FA46   307 _BANK2PAL	=	0xfa46
                           00FA47   308 _BANK2PAH	=	0xfa47
                           00FA48   309 _PRAMCTL	=	0xfa48
                           000000   310 _usb_buffer	=	0x0000
      006000                        311 _usb_irq:
      006000                        312 	.ds 1
      006001                        313 _UsbIntStsF080:
      006001                        314 	.ds 1
      006002                        315 _UsbIntStsF082:
      006002                        316 	.ds 1
      006003                        317 _UsbIntStsF086:
      006003                        318 	.ds 1
      006004                        319 _UsbIntStsF087:
      006004                        320 	.ds 1
      006005                        321 _usb_received_data_ready::
      006005                        322 	.ds 1
      006006                        323 _usb_have_csw_ready::
      006006                        324 	.ds 1
                                    325 ;--------------------------------------------------------
                                    326 ; absolute external ram data
                                    327 ;--------------------------------------------------------
                                    328 	.area XABS    (ABS,XDATA)
                                    329 ;--------------------------------------------------------
                                    330 ; external initialized ram data
                                    331 ;--------------------------------------------------------
                                    332 	.area XISEG   (XDATA)
                                    333 	.area HOME    (CODE)
                                    334 	.area GSINIT0 (CODE)
                                    335 	.area GSINIT1 (CODE)
                                    336 	.area GSINIT2 (CODE)
                                    337 	.area GSINIT3 (CODE)
                                    338 	.area GSINIT4 (CODE)
                                    339 	.area GSINIT5 (CODE)
                                    340 	.area GSINIT  (CODE)
                                    341 	.area GSFINAL (CODE)
                                    342 	.area CSEG    (CODE)
                                    343 ;--------------------------------------------------------
                                    344 ; global & static initialisations
                                    345 ;--------------------------------------------------------
                                    346 	.area HOME    (CODE)
                                    347 	.area GSINIT  (CODE)
                                    348 	.area GSFINAL (CODE)
                                    349 	.area GSINIT  (CODE)
                                    350 ;--------------------------------------------------------
                                    351 ; Home
                                    352 ;--------------------------------------------------------
                                    353 	.area HOME    (CODE)
                                    354 	.area HOME    (CODE)
                                    355 ;--------------------------------------------------------
                                    356 ; code
                                    357 ;--------------------------------------------------------
                                    358 	.area CSEG    (CODE)
                                    359 ;------------------------------------------------------------
                                    360 ;Allocation info for local variables in function 'SetDMA'
                                    361 ;------------------------------------------------------------
                                    362 ;p3                        Allocated with name '_SetDMA_PARM_2'
                                    363 ;px                        Allocated with name '_SetDMA_PARM_3'
                                    364 ;p5                        Allocated to registers r7 
                                    365 ;------------------------------------------------------------
                                    366 ;	usb.c:34: void SetDMA(BYTE p5, BYTE p3, BYTE px)
                                    367 ;	-----------------------------------------
                                    368 ;	 function SetDMA
                                    369 ;	-----------------------------------------
      000414                        370 _SetDMA:
                           000007   371 	ar7 = 0x07
                           000006   372 	ar6 = 0x06
                           000005   373 	ar5 = 0x05
                           000004   374 	ar4 = 0x04
                           000003   375 	ar3 = 0x03
                           000002   376 	ar2 = 0x02
                           000001   377 	ar1 = 0x01
                           000000   378 	ar0 = 0x00
      000414 AF 82            [24]  379 	mov	r7,dpl
                                    380 ;	usb.c:36: XVAL(0xF80B) = 0;
      000416 90 F8 0B         [24]  381 	mov	dptr,#0xF80B
      000419 E4               [12]  382 	clr	a
      00041A F0               [24]  383 	movx	@dptr,a
                                    384 ;	usb.c:37: XVAL(0xF80C) = p5-1;
      00041B 1F               [12]  385 	dec	r7
      00041C 90 F8 0C         [24]  386 	mov	dptr,#0xF80C
      00041F EF               [12]  387 	mov	a,r7
      000420 F0               [24]  388 	movx	@dptr,a
                                    389 ;	usb.c:39: switch(px)
      000421 E4               [12]  390 	clr	a
      000422 B5 46 02         [24]  391 	cjne	a,_SetDMA_PARM_3,00117$
      000425 80 0E            [24]  392 	sjmp	00101$
      000427                        393 00117$:
      000427 74 01            [12]  394 	mov	a,#0x01
      000429 B5 46 02         [24]  395 	cjne	a,_SetDMA_PARM_3,00118$
      00042C 80 14            [24]  396 	sjmp	00102$
      00042E                        397 00118$:
      00042E 74 02            [12]  398 	mov	a,#0x02
                                    399 ;	usb.c:41: case 0:
      000430 B5 46 1C         [24]  400 	cjne	a,_SetDMA_PARM_3,00106$
      000433 80 14            [24]  401 	sjmp	00103$
      000435                        402 00101$:
                                    403 ;	usb.c:43: XVAL(0xF80D) = p3;
      000435 90 F8 0D         [24]  404 	mov	dptr,#0xF80D
      000438 E5 45            [12]  405 	mov	a,_SetDMA_PARM_2
      00043A F0               [24]  406 	movx	@dptr,a
                                    407 ;	usb.c:44: XVAL(0xF80E) = p3;
      00043B 90 F8 0E         [24]  408 	mov	dptr,#0xF80E
      00043E E5 45            [12]  409 	mov	a,_SetDMA_PARM_2
      000440 F0               [24]  410 	movx	@dptr,a
                                    411 ;	usb.c:45: break;
                                    412 ;	usb.c:47: case 1:
      000441 22               [24]  413 	ret
      000442                        414 00102$:
                                    415 ;	usb.c:49: XVAL(0xF80D) = p3;
      000442 90 F8 0D         [24]  416 	mov	dptr,#0xF80D
      000445 E5 45            [12]  417 	mov	a,_SetDMA_PARM_2
      000447 F0               [24]  418 	movx	@dptr,a
                                    419 ;	usb.c:50: break;
                                    420 ;	usb.c:52: case 2:
      000448 22               [24]  421 	ret
      000449                        422 00103$:
                                    423 ;	usb.c:54: XVAL(0xF80E) = p3;
      000449 90 F8 0E         [24]  424 	mov	dptr,#0xF80E
      00044C E5 45            [12]  425 	mov	a,_SetDMA_PARM_2
      00044E F0               [24]  426 	movx	@dptr,a
                                    427 ;	usb.c:61: }
      00044F                        428 00106$:
      00044F 22               [24]  429 	ret
                                    430 ;------------------------------------------------------------
                                    431 ;Allocation info for local variables in function 'SendControlResponse'
                                    432 ;------------------------------------------------------------
                                    433 ;size                      Allocated to registers r6 r7 
                                    434 ;------------------------------------------------------------
                                    435 ;	usb.c:64: void SendControlResponse(int size)
                                    436 ;	-----------------------------------------
                                    437 ;	 function SendControlResponse
                                    438 ;	-----------------------------------------
      000450                        439 _SendControlResponse:
      000450 AE 82            [24]  440 	mov	r6,dpl
      000452 AF 83            [24]  441 	mov	r7,dph
                                    442 ;	usb.c:66: EP0.len_l = LSB(size);
      000454 8E 04            [24]  443 	mov	ar4,r6
      000456 7D 00            [12]  444 	mov	r5,#0x00
      000458 90 F1 CC         [24]  445 	mov	dptr,#(_EP0 + 0x000c)
      00045B EC               [12]  446 	mov	a,r4
      00045C F0               [24]  447 	movx	@dptr,a
                                    448 ;	usb.c:67: EP0.len_m = MSB(size);
      00045D 8F 06            [24]  449 	mov	ar6,r7
      00045F 90 F1 CD         [24]  450 	mov	dptr,#(_EP0 + 0x000d)
      000462 EE               [12]  451 	mov	a,r6
      000463 F0               [24]  452 	movx	@dptr,a
                                    453 ;	usb.c:68: EP0.len_h = 0;
      000464 90 F1 CE         [24]  454 	mov	dptr,#(_EP0 + 0x000e)
      000467 E4               [12]  455 	clr	a
      000468 F0               [24]  456 	movx	@dptr,a
                                    457 ;	usb.c:69: EP0.cs = 0x40;
      000469 90 F1 D3         [24]  458 	mov	dptr,#(_EP0 + 0x0013)
      00046C 74 40            [12]  459 	mov	a,#0x40
      00046E F0               [24]  460 	movx	@dptr,a
                                    461 ;	usb.c:70: while (EP0.cs & 0x40);
      00046F                        462 00101$:
      00046F 90 F1 D3         [24]  463 	mov	dptr,#(_EP0 + 0x0013)
      000472 E0               [24]  464 	movx	a,@dptr
      000473 FF               [12]  465 	mov	r7,a
      000474 20 E6 F8         [24]  466 	jb	acc.6,00101$
                                    467 ;	usb.c:71: EP0CS = 0x05;
      000477 90 F0 48         [24]  468 	mov	dptr,#_EP0CS
      00047A 74 05            [12]  469 	mov	a,#0x05
      00047C F0               [24]  470 	movx	@dptr,a
      00047D 22               [24]  471 	ret
                                    472 ;------------------------------------------------------------
                                    473 ;Allocation info for local variables in function 'SendData0'
                                    474 ;------------------------------------------------------------
                                    475 ;offset                    Allocated with name '_SendData0_PARM_2'
                                    476 ;size                      Allocated to registers r6 r7 
                                    477 ;------------------------------------------------------------
                                    478 ;	usb.c:74: void SendData0(WORD size, BYTE offset)
                                    479 ;	-----------------------------------------
                                    480 ;	 function SendData0
                                    481 ;	-----------------------------------------
      00047E                        482 _SendData0:
      00047E AE 82            [24]  483 	mov	r6,dpl
      000480 AF 83            [24]  484 	mov	r7,dph
                                    485 ;	usb.c:76: if (size > 0)
      000482 EE               [12]  486 	mov	a,r6
      000483 4F               [12]  487 	orl	a,r7
      000484 60 58            [24]  488 	jz	00106$
                                    489 ;	usb.c:78: SetDMA(0x20, 0, 0);
      000486 75 45 00         [24]  490 	mov	_SetDMA_PARM_2,#0x00
      000489 75 46 00         [24]  491 	mov	_SetDMA_PARM_3,#0x00
      00048C 75 82 20         [24]  492 	mov	dpl,#0x20
      00048F C0 07            [24]  493 	push	ar7
      000491 C0 06            [24]  494 	push	ar6
      000493 12 04 14         [24]  495 	lcall	_SetDMA
                                    496 ;	usb.c:79: SetDMA(0x20, 0x80, 1);
      000496 75 45 80         [24]  497 	mov	_SetDMA_PARM_2,#0x80
      000499 75 46 01         [24]  498 	mov	_SetDMA_PARM_3,#0x01
      00049C 75 82 20         [24]  499 	mov	dpl,#0x20
      00049F 12 04 14         [24]  500 	lcall	_SetDMA
      0004A2 D0 06            [24]  501 	pop	ar6
      0004A4 D0 07            [24]  502 	pop	ar7
                                    503 ;	usb.c:80: EP0.ptr_l = usb_buffer_PA>>8;
      0004A6 90 F1 C5         [24]  504 	mov	dptr,#(_EP0 + 0x0005)
      0004A9 74 80            [12]  505 	mov	a,#0x80
      0004AB F0               [24]  506 	movx	@dptr,a
                                    507 ;	usb.c:81: EP0.ptr_m = usb_buffer_PA>>16;
      0004AC 90 F1 C6         [24]  508 	mov	dptr,#(_EP0 + 0x0006)
      0004AF E4               [12]  509 	clr	a
      0004B0 F0               [24]  510 	movx	@dptr,a
                                    511 ;	usb.c:82: EP0.ptr_h = usb_buffer_PA>>24;
      0004B1 90 F1 C7         [24]  512 	mov	dptr,#(_EP0 + 0x0007)
      0004B4 F0               [24]  513 	movx	@dptr,a
                                    514 ;	usb.c:83: EP0.offset = offset;
      0004B5 90 F1 CA         [24]  515 	mov	dptr,#(_EP0 + 0x000a)
      0004B8 E5 23            [12]  516 	mov	a,_SendData0_PARM_2
      0004BA F0               [24]  517 	movx	@dptr,a
                                    518 ;	usb.c:84: EP0.len_l = LSB(size);
      0004BB 8E 04            [24]  519 	mov	ar4,r6
      0004BD 7D 00            [12]  520 	mov	r5,#0x00
      0004BF 90 F1 CC         [24]  521 	mov	dptr,#(_EP0 + 0x000c)
      0004C2 EC               [12]  522 	mov	a,r4
      0004C3 F0               [24]  523 	movx	@dptr,a
                                    524 ;	usb.c:85: EP0.len_m = MSB(size);
      0004C4 8F 06            [24]  525 	mov	ar6,r7
      0004C6 90 F1 CD         [24]  526 	mov	dptr,#(_EP0 + 0x000d)
      0004C9 EE               [12]  527 	mov	a,r6
      0004CA F0               [24]  528 	movx	@dptr,a
                                    529 ;	usb.c:86: EP0.len_h = 0;
      0004CB 90 F1 CE         [24]  530 	mov	dptr,#(_EP0 + 0x000e)
      0004CE E4               [12]  531 	clr	a
      0004CF F0               [24]  532 	movx	@dptr,a
                                    533 ;	usb.c:87: EP0.cs = 0x88;		
      0004D0 90 F1 D3         [24]  534 	mov	dptr,#(_EP0 + 0x0013)
      0004D3 74 88            [12]  535 	mov	a,#0x88
      0004D5 F0               [24]  536 	movx	@dptr,a
                                    537 ;	usb.c:89: while(EP0.cs & 0x80);	
      0004D6                        538 00101$:
      0004D6 90 F1 D3         [24]  539 	mov	dptr,#(_EP0 + 0x0013)
      0004D9 E0               [24]  540 	movx	a,@dptr
      0004DA FF               [12]  541 	mov	r7,a
      0004DB 20 E7 F8         [24]  542 	jb	acc.7,00101$
      0004DE                        543 00106$:
      0004DE 22               [24]  544 	ret
                                    545 ;------------------------------------------------------------
                                    546 ;Allocation info for local variables in function 'SendData1'
                                    547 ;------------------------------------------------------------
                                    548 ;offset                    Allocated with name '_SendData1_PARM_2'
                                    549 ;size                      Allocated to registers r6 r7 
                                    550 ;------------------------------------------------------------
                                    551 ;	usb.c:93: void SendData1(WORD size, BYTE offset)
                                    552 ;	-----------------------------------------
                                    553 ;	 function SendData1
                                    554 ;	-----------------------------------------
      0004DF                        555 _SendData1:
      0004DF AE 82            [24]  556 	mov	r6,dpl
      0004E1 AF 83            [24]  557 	mov	r7,dph
                                    558 ;	usb.c:95: if (size > 0)
      0004E3 EE               [12]  559 	mov	a,r6
      0004E4 4F               [12]  560 	orl	a,r7
      0004E5 60 58            [24]  561 	jz	00106$
                                    562 ;	usb.c:97: SetDMA(0x20, 0, 0);
      0004E7 75 45 00         [24]  563 	mov	_SetDMA_PARM_2,#0x00
      0004EA 75 46 00         [24]  564 	mov	_SetDMA_PARM_3,#0x00
      0004ED 75 82 20         [24]  565 	mov	dpl,#0x20
      0004F0 C0 07            [24]  566 	push	ar7
      0004F2 C0 06            [24]  567 	push	ar6
      0004F4 12 04 14         [24]  568 	lcall	_SetDMA
                                    569 ;	usb.c:98: SetDMA(0x20, 0x80, 1);
      0004F7 75 45 80         [24]  570 	mov	_SetDMA_PARM_2,#0x80
      0004FA 75 46 01         [24]  571 	mov	_SetDMA_PARM_3,#0x01
      0004FD 75 82 20         [24]  572 	mov	dpl,#0x20
      000500 12 04 14         [24]  573 	lcall	_SetDMA
      000503 D0 06            [24]  574 	pop	ar6
      000505 D0 07            [24]  575 	pop	ar7
                                    576 ;	usb.c:99: EP1.ptr_l = usb_buffer_PA>>8;
      000507 90 F2 05         [24]  577 	mov	dptr,#(_EP1 + 0x0005)
      00050A 74 80            [12]  578 	mov	a,#0x80
      00050C F0               [24]  579 	movx	@dptr,a
                                    580 ;	usb.c:100: EP1.ptr_m = usb_buffer_PA>>16;
      00050D 90 F2 06         [24]  581 	mov	dptr,#(_EP1 + 0x0006)
      000510 E4               [12]  582 	clr	a
      000511 F0               [24]  583 	movx	@dptr,a
                                    584 ;	usb.c:101: EP1.ptr_h = usb_buffer_PA>>24;
      000512 90 F2 07         [24]  585 	mov	dptr,#(_EP1 + 0x0007)
      000515 F0               [24]  586 	movx	@dptr,a
                                    587 ;	usb.c:102: EP1.offset = offset;
      000516 90 F2 0A         [24]  588 	mov	dptr,#(_EP1 + 0x000a)
      000519 E5 24            [12]  589 	mov	a,_SendData1_PARM_2
      00051B F0               [24]  590 	movx	@dptr,a
                                    591 ;	usb.c:103: EP1.len_l = LSB(size);
      00051C 8E 04            [24]  592 	mov	ar4,r6
      00051E 7D 00            [12]  593 	mov	r5,#0x00
      000520 90 F2 0C         [24]  594 	mov	dptr,#(_EP1 + 0x000c)
      000523 EC               [12]  595 	mov	a,r4
      000524 F0               [24]  596 	movx	@dptr,a
                                    597 ;	usb.c:104: EP1.len_m = MSB(size);
      000525 8F 06            [24]  598 	mov	ar6,r7
      000527 90 F2 0D         [24]  599 	mov	dptr,#(_EP1 + 0x000d)
      00052A EE               [12]  600 	mov	a,r6
      00052B F0               [24]  601 	movx	@dptr,a
                                    602 ;	usb.c:105: EP1.len_h = 0;
      00052C 90 F2 0E         [24]  603 	mov	dptr,#(_EP1 + 0x000e)
      00052F E4               [12]  604 	clr	a
      000530 F0               [24]  605 	movx	@dptr,a
                                    606 ;	usb.c:106: EP1.cs = 0x88;		
      000531 90 F2 13         [24]  607 	mov	dptr,#(_EP1 + 0x0013)
      000534 74 88            [12]  608 	mov	a,#0x88
      000536 F0               [24]  609 	movx	@dptr,a
                                    610 ;	usb.c:108: while(EP1.cs & 0x80);	
      000537                        611 00101$:
      000537 90 F2 13         [24]  612 	mov	dptr,#(_EP1 + 0x0013)
      00053A E0               [24]  613 	movx	a,@dptr
      00053B FF               [12]  614 	mov	r7,a
      00053C 20 E7 F8         [24]  615 	jb	acc.7,00101$
      00053F                        616 00106$:
      00053F 22               [24]  617 	ret
                                    618 ;------------------------------------------------------------
                                    619 ;Allocation info for local variables in function 'SendCSW'
                                    620 ;------------------------------------------------------------
                                    621 ;	usb.c:112: static void SendCSW()
                                    622 ;	-----------------------------------------
                                    623 ;	 function SendCSW
                                    624 ;	-----------------------------------------
      000540                        625 _SendCSW:
                                    626 ;	usb.c:114: usb_buffer[0] = 'U';
      000540 90 00 00         [24]  627 	mov	dptr,#_usb_buffer
      000543 74 55            [12]  628 	mov	a,#0x55
      000545 F0               [24]  629 	movx	@dptr,a
                                    630 ;	usb.c:115: usb_buffer[1] = 'S';
      000546 90 00 01         [24]  631 	mov	dptr,#(_usb_buffer + 0x0001)
      000549 74 53            [12]  632 	mov	a,#0x53
      00054B F0               [24]  633 	movx	@dptr,a
                                    634 ;	usb.c:116: usb_buffer[2] = 'B';
      00054C 90 00 02         [24]  635 	mov	dptr,#(_usb_buffer + 0x0002)
      00054F 74 42            [12]  636 	mov	a,#0x42
      000551 F0               [24]  637 	movx	@dptr,a
                                    638 ;	usb.c:117: usb_buffer[3] = 'S';
      000552 90 00 03         [24]  639 	mov	dptr,#(_usb_buffer + 0x0003)
      000555 74 53            [12]  640 	mov	a,#0x53
      000557 F0               [24]  641 	movx	@dptr,a
                                    642 ;	usb.c:118: usb_buffer[4] = scsi_tag[0];
      000558 90 00 04         [24]  643 	mov	dptr,#(_usb_buffer + 0x0004)
      00055B E5 2E            [12]  644 	mov	a,_scsi_tag
      00055D F0               [24]  645 	movx	@dptr,a
                                    646 ;	usb.c:119: usb_buffer[5] = scsi_tag[1];
      00055E 90 00 05         [24]  647 	mov	dptr,#(_usb_buffer + 0x0005)
      000561 E5 2F            [12]  648 	mov	a,(_scsi_tag + 0x0001)
      000563 F0               [24]  649 	movx	@dptr,a
                                    650 ;	usb.c:120: usb_buffer[6] = scsi_tag[2];
      000564 90 00 06         [24]  651 	mov	dptr,#(_usb_buffer + 0x0006)
      000567 E5 30            [12]  652 	mov	a,(_scsi_tag + 0x0002)
      000569 F0               [24]  653 	movx	@dptr,a
                                    654 ;	usb.c:121: usb_buffer[7] = scsi_tag[3];
      00056A 90 00 07         [24]  655 	mov	dptr,#(_usb_buffer + 0x0007)
      00056D E5 31            [12]  656 	mov	a,(_scsi_tag + 0x0003)
      00056F F0               [24]  657 	movx	@dptr,a
                                    658 ;	usb.c:122: usb_buffer[8] = scsi_data_residue;
      000570 AF 26            [24]  659 	mov	r7,_scsi_data_residue
      000572 90 00 08         [24]  660 	mov	dptr,#(_usb_buffer + 0x0008)
      000575 EF               [12]  661 	mov	a,r7
      000576 F0               [24]  662 	movx	@dptr,a
                                    663 ;	usb.c:123: usb_buffer[9] = scsi_data_residue>>8;
      000577 AF 27            [24]  664 	mov	r7,(_scsi_data_residue + 1)
      000579 90 00 09         [24]  665 	mov	dptr,#(_usb_buffer + 0x0009)
      00057C EF               [12]  666 	mov	a,r7
      00057D F0               [24]  667 	movx	@dptr,a
                                    668 ;	usb.c:124: usb_buffer[10] = scsi_data_residue>>16;
      00057E AF 28            [24]  669 	mov	r7,(_scsi_data_residue + 2)
      000580 90 00 0A         [24]  670 	mov	dptr,#(_usb_buffer + 0x000a)
      000583 EF               [12]  671 	mov	a,r7
      000584 F0               [24]  672 	movx	@dptr,a
                                    673 ;	usb.c:125: usb_buffer[11] = scsi_data_residue>>24;
      000585 AF 29            [24]  674 	mov	r7,(_scsi_data_residue + 3)
      000587 90 00 0B         [24]  675 	mov	dptr,#(_usb_buffer + 0x000b)
      00058A EF               [12]  676 	mov	a,r7
      00058B F0               [24]  677 	movx	@dptr,a
                                    678 ;	usb.c:126: usb_buffer[12] = scsi_status;
      00058C 90 00 0C         [24]  679 	mov	dptr,#(_usb_buffer + 0x000c)
      00058F E5 25            [12]  680 	mov	a,_scsi_status
      000591 F0               [24]  681 	movx	@dptr,a
                                    682 ;	usb.c:128: SendData1(13, 0);
      000592 75 24 00         [24]  683 	mov	_SendData1_PARM_2,#0x00
      000595 90 00 0D         [24]  684 	mov	dptr,#0x000D
      000598 12 04 DF         [24]  685 	lcall	_SendData1
                                    686 ;	usb.c:129: usb_have_csw_ready = 0;
      00059B 90 60 06         [24]  687 	mov	dptr,#_usb_have_csw_ready
      00059E E4               [12]  688 	clr	a
      00059F F0               [24]  689 	movx	@dptr,a
                                    690 ;	usb.c:130: scsi_data_residue = 0;
      0005A0 F5 26            [12]  691 	mov	_scsi_data_residue,a
      0005A2 F5 27            [12]  692 	mov	(_scsi_data_residue + 1),a
      0005A4 F5 28            [12]  693 	mov	(_scsi_data_residue + 2),a
      0005A6 F5 29            [12]  694 	mov	(_scsi_data_residue + 3),a
      0005A8 22               [24]  695 	ret
                                    696 ;------------------------------------------------------------
                                    697 ;Allocation info for local variables in function 'SendCSW2'
                                    698 ;------------------------------------------------------------
                                    699 ;	usb.c:133: static void SendCSW2()
                                    700 ;	-----------------------------------------
                                    701 ;	 function SendCSW2
                                    702 ;	-----------------------------------------
      0005A9                        703 _SendCSW2:
                                    704 ;	usb.c:135: while(EP1.cs & bmSTALL);
      0005A9                        705 00101$:
      0005A9 90 F2 13         [24]  706 	mov	dptr,#(_EP1 + 0x0013)
      0005AC E0               [24]  707 	movx	a,@dptr
      0005AD FF               [12]  708 	mov	r7,a
      0005AE 20 E1 F8         [24]  709 	jb	acc.1,00101$
                                    710 ;	usb.c:136: while((EP1.r17 & 0x80)==0)
      0005B1 90 F0 10         [24]  711 	mov	dptr,#0xF010
      0005B4 E0               [24]  712 	movx	a,@dptr
      0005B5 FF               [12]  713 	mov	r7,a
      0005B6 53 07 20         [24]  714 	anl	ar7,#0x20
      0005B9                        715 00106$:
      0005B9 90 F2 17         [24]  716 	mov	dptr,#(_EP1 + 0x0017)
      0005BC E0               [24]  717 	movx	a,@dptr
      0005BD FE               [12]  718 	mov	r6,a
      0005BE 20 E7 09         [24]  719 	jb	acc.7,00109$
                                    720 ;	usb.c:138: if ((XVAL(0xF010) & 0x20)==0)
      0005C1 EF               [12]  721 	mov	a,r7
      0005C2 70 F5            [24]  722 	jnz	00106$
                                    723 ;	usb.c:140: usb_have_csw_ready = 0;
      0005C4 90 60 06         [24]  724 	mov	dptr,#_usb_have_csw_ready
      0005C7 E4               [12]  725 	clr	a
      0005C8 F0               [24]  726 	movx	@dptr,a
                                    727 ;	usb.c:141: return;
      0005C9 22               [24]  728 	ret
                                    729 ;	usb.c:145: while(EP1.cs & 0x40);
      0005CA                        730 00109$:
      0005CA 90 F2 13         [24]  731 	mov	dptr,#(_EP1 + 0x0013)
      0005CD E0               [24]  732 	movx	a,@dptr
      0005CE FF               [12]  733 	mov	r7,a
      0005CF 20 E6 F8         [24]  734 	jb	acc.6,00109$
                                    735 ;	usb.c:146: while(EP2.cs & 0x40);
      0005D2                        736 00112$:
      0005D2 90 F2 53         [24]  737 	mov	dptr,#(_EP2 + 0x0013)
      0005D5 E0               [24]  738 	movx	a,@dptr
      0005D6 FF               [12]  739 	mov	r7,a
      0005D7 20 E6 F8         [24]  740 	jb	acc.6,00112$
                                    741 ;	usb.c:147: while(EP3.cs & 0x40);
      0005DA                        742 00115$:
      0005DA 90 F2 93         [24]  743 	mov	dptr,#(_EP3 + 0x0013)
      0005DD E0               [24]  744 	movx	a,@dptr
      0005DE FF               [12]  745 	mov	r7,a
      0005DF 20 E6 F8         [24]  746 	jb	acc.6,00115$
                                    747 ;	usb.c:148: while(EP4.cs & 0x40);
      0005E2                        748 00118$:
      0005E2 90 F2 D3         [24]  749 	mov	dptr,#(_EP4 + 0x0013)
      0005E5 E0               [24]  750 	movx	a,@dptr
      0005E6 FF               [12]  751 	mov	r7,a
      0005E7 20 E6 F8         [24]  752 	jb	acc.6,00118$
                                    753 ;	usb.c:150: EP1.fifo = 'U';
                                    754 ;	usb.c:151: EP1.fifo = 'S';
                                    755 ;	usb.c:152: EP1.fifo = 'B';
                                    756 ;	usb.c:153: EP1.fifo = 'S';
      0005EA 90 F2 1C         [24]  757 	mov	dptr,#(_EP1 + 0x001c)
      0005ED 74 55            [12]  758 	mov	a,#0x55
      0005EF F0               [24]  759 	movx	@dptr,a
      0005F0 74 53            [12]  760 	mov	a,#0x53
      0005F2 F0               [24]  761 	movx	@dptr,a
      0005F3 74 42            [12]  762 	mov	a,#0x42
      0005F5 F0               [24]  763 	movx	@dptr,a
      0005F6 74 53            [12]  764 	mov	a,#0x53
      0005F8 F0               [24]  765 	movx	@dptr,a
                                    766 ;	usb.c:154: EP1.fifo = scsi_tag[0];
                                    767 ;	usb.c:155: EP1.fifo = scsi_tag[1];
                                    768 ;	usb.c:156: EP1.fifo = scsi_tag[2];
                                    769 ;	usb.c:157: EP1.fifo = scsi_tag[3];
      0005F9 90 F2 1C         [24]  770 	mov	dptr,#(_EP1 + 0x001c)
      0005FC E5 2E            [12]  771 	mov	a,_scsi_tag
      0005FE F0               [24]  772 	movx	@dptr,a
      0005FF E5 2F            [12]  773 	mov	a,(_scsi_tag + 0x0001)
      000601 F0               [24]  774 	movx	@dptr,a
      000602 E5 30            [12]  775 	mov	a,(_scsi_tag + 0x0002)
      000604 F0               [24]  776 	movx	@dptr,a
      000605 E5 31            [12]  777 	mov	a,(_scsi_tag + 0x0003)
      000607 F0               [24]  778 	movx	@dptr,a
                                    779 ;	usb.c:158: EP1.fifo = scsi_data_residue;
      000608 AF 26            [24]  780 	mov	r7,_scsi_data_residue
      00060A 90 F2 1C         [24]  781 	mov	dptr,#(_EP1 + 0x001c)
      00060D EF               [12]  782 	mov	a,r7
      00060E F0               [24]  783 	movx	@dptr,a
                                    784 ;	usb.c:159: EP1.fifo = scsi_data_residue>>8;
      00060F AF 27            [24]  785 	mov	r7,(_scsi_data_residue + 1)
      000611 90 F2 1C         [24]  786 	mov	dptr,#(_EP1 + 0x001c)
      000614 EF               [12]  787 	mov	a,r7
      000615 F0               [24]  788 	movx	@dptr,a
                                    789 ;	usb.c:160: EP1.fifo = scsi_data_residue>>16;
      000616 AF 28            [24]  790 	mov	r7,(_scsi_data_residue + 2)
      000618 90 F2 1C         [24]  791 	mov	dptr,#(_EP1 + 0x001c)
      00061B EF               [12]  792 	mov	a,r7
      00061C F0               [24]  793 	movx	@dptr,a
                                    794 ;	usb.c:161: EP1.fifo = scsi_data_residue>>24;
      00061D AF 29            [24]  795 	mov	r7,(_scsi_data_residue + 3)
                                    796 ;	usb.c:162: EP1.fifo = scsi_status;
      00061F 90 F2 1C         [24]  797 	mov	dptr,#(_EP1 + 0x001c)
      000622 EF               [12]  798 	mov	a,r7
      000623 F0               [24]  799 	movx	@dptr,a
      000624 E5 25            [12]  800 	mov	a,_scsi_status
      000626 F0               [24]  801 	movx	@dptr,a
                                    802 ;	usb.c:163: EP1.len_l = 13;
      000627 90 F2 0C         [24]  803 	mov	dptr,#(_EP1 + 0x000c)
      00062A 74 0D            [12]  804 	mov	a,#0x0D
      00062C F0               [24]  805 	movx	@dptr,a
                                    806 ;	usb.c:164: EP1.len_m = 0;
      00062D 90 F2 0D         [24]  807 	mov	dptr,#(_EP1 + 0x000d)
      000630 E4               [12]  808 	clr	a
      000631 F0               [24]  809 	movx	@dptr,a
                                    810 ;	usb.c:165: EP1.len_h = 0;
      000632 90 F2 0E         [24]  811 	mov	dptr,#(_EP1 + 0x000e)
      000635 F0               [24]  812 	movx	@dptr,a
                                    813 ;	usb.c:166: EP1.cs = 0x40;		
      000636 90 F2 13         [24]  814 	mov	dptr,#(_EP1 + 0x0013)
      000639 74 40            [12]  815 	mov	a,#0x40
      00063B F0               [24]  816 	movx	@dptr,a
                                    817 ;	usb.c:167: usb_have_csw_ready = 0;
      00063C 90 60 06         [24]  818 	mov	dptr,#_usb_have_csw_ready
      00063F E4               [12]  819 	clr	a
      000640 F0               [24]  820 	movx	@dptr,a
                                    821 ;	usb.c:168: scsi_data_residue = 0;
      000641 F5 26            [12]  822 	mov	_scsi_data_residue,a
      000643 F5 27            [12]  823 	mov	(_scsi_data_residue + 1),a
      000645 F5 28            [12]  824 	mov	(_scsi_data_residue + 2),a
      000647 F5 29            [12]  825 	mov	(_scsi_data_residue + 3),a
      000649 22               [24]  826 	ret
                                    827 ;------------------------------------------------------------
                                    828 ;Allocation info for local variables in function 'InitUSB'
                                    829 ;------------------------------------------------------------
                                    830 ;b                         Allocated to registers r7 
                                    831 ;------------------------------------------------------------
                                    832 ;	usb.c:171: void InitUSB(void)
                                    833 ;	-----------------------------------------
                                    834 ;	 function InitUSB
                                    835 ;	-----------------------------------------
      00064A                        836 _InitUSB:
                                    837 ;	usb.c:175: usb_irq = 0;
      00064A 90 60 00         [24]  838 	mov	dptr,#_usb_irq
      00064D E4               [12]  839 	clr	a
      00064E F0               [24]  840 	movx	@dptr,a
                                    841 ;	usb.c:176: usb_received_data_ready = 0;
      00064F 90 60 05         [24]  842 	mov	dptr,#_usb_received_data_ready
      000652 F0               [24]  843 	movx	@dptr,a
                                    844 ;	usb.c:177: usb_have_csw_ready = 0;
      000653 90 60 06         [24]  845 	mov	dptr,#_usb_have_csw_ready
      000656 F0               [24]  846 	movx	@dptr,a
                                    847 ;	usb.c:178: usb_speed = 0;
                                    848 ;	1-genFromRTrack replaced	mov	_usb_speed,#0x00
      000657 F5 22            [12]  849 	mov	_usb_speed,a
                                    850 ;	usb.c:179: EP1.ptr_l = usb_buffer_PA>>8;
      000659 90 F2 05         [24]  851 	mov	dptr,#(_EP1 + 0x0005)
      00065C 74 80            [12]  852 	mov	a,#0x80
      00065E F0               [24]  853 	movx	@dptr,a
                                    854 ;	usb.c:180: EP1.ptr_m = usb_buffer_PA>>16;
      00065F 90 F2 06         [24]  855 	mov	dptr,#(_EP1 + 0x0006)
      000662 E4               [12]  856 	clr	a
      000663 F0               [24]  857 	movx	@dptr,a
                                    858 ;	usb.c:181: EP1.ptr_h = usb_buffer_PA>>24;
      000664 90 F2 07         [24]  859 	mov	dptr,#(_EP1 + 0x0007)
      000667 F0               [24]  860 	movx	@dptr,a
                                    861 ;	usb.c:182: EP1.r8 = 0x10;
      000668 90 F2 08         [24]  862 	mov	dptr,#(_EP1 + 0x0008)
      00066B 74 10            [12]  863 	mov	a,#0x10
      00066D F0               [24]  864 	movx	@dptr,a
                                    865 ;	usb.c:183: EP1.offset = 0;
      00066E 90 F2 0A         [24]  866 	mov	dptr,#(_EP1 + 0x000a)
      000671 E4               [12]  867 	clr	a
      000672 F0               [24]  868 	movx	@dptr,a
                                    869 ;	usb.c:184: EP2.ptr_l = usb_buffer_PA>>8;
      000673 90 F2 45         [24]  870 	mov	dptr,#(_EP2 + 0x0005)
      000676 74 80            [12]  871 	mov	a,#0x80
      000678 F0               [24]  872 	movx	@dptr,a
                                    873 ;	usb.c:185: EP2.ptr_m = usb_buffer_PA>>16;
      000679 90 F2 46         [24]  874 	mov	dptr,#(_EP2 + 0x0006)
      00067C E4               [12]  875 	clr	a
      00067D F0               [24]  876 	movx	@dptr,a
                                    877 ;	usb.c:186: EP2.ptr_h = usb_buffer_PA>>24;
      00067E 90 F2 47         [24]  878 	mov	dptr,#(_EP2 + 0x0007)
      000681 F0               [24]  879 	movx	@dptr,a
                                    880 ;	usb.c:187: EP2.r8 = 0x10;
      000682 90 F2 48         [24]  881 	mov	dptr,#(_EP2 + 0x0008)
      000685 74 10            [12]  882 	mov	a,#0x10
      000687 F0               [24]  883 	movx	@dptr,a
                                    884 ;	usb.c:188: EP2.offset = 0;
      000688 90 F2 4A         [24]  885 	mov	dptr,#(_EP2 + 0x000a)
      00068B E4               [12]  886 	clr	a
      00068C F0               [24]  887 	movx	@dptr,a
                                    888 ;	usb.c:190: if (WARMSTATUS & 2) //USB warm start
      00068D 90 FA 38         [24]  889 	mov	dptr,#_WARMSTATUS
      000690 E0               [24]  890 	movx	a,@dptr
      000691 FF               [12]  891 	mov	r7,a
      000692 30 E1 4B         [24]  892 	jnb	acc.1,00112$
                                    893 ;	usb.c:192: if ((USBSTAT & bmSpeed) == bmSuperSpeed)
      000695 90 F0 09         [24]  894 	mov	dptr,#_USBSTAT
      000698 E0               [24]  895 	movx	a,@dptr
      000699 FF               [12]  896 	mov	r7,a
      00069A 53 07 07         [24]  897 	anl	ar7,#0x07
      00069D BF 04 05         [24]  898 	cjne	r7,#0x04,00108$
                                    899 ;	usb.c:194: usb_speed = bmSuperSpeed;
      0006A0 75 22 04         [24]  900 	mov	_usb_speed,#0x04
      0006A3 80 23            [24]  901 	sjmp	00109$
      0006A5                        902 00108$:
                                    903 ;	usb.c:196: else if ((USBSTAT & bmSpeed) == bmHighSpeed)
      0006A5 90 F0 09         [24]  904 	mov	dptr,#_USBSTAT
      0006A8 E0               [24]  905 	movx	a,@dptr
      0006A9 FF               [12]  906 	mov	r7,a
      0006AA 54 07            [12]  907 	anl	a,#0x07
      0006AC 60 02            [24]  908 	jz	00139$
      0006AE 80 05            [24]  909 	sjmp	00105$
      0006B0                        910 00139$:
                                    911 ;	usb.c:198: usb_speed = bmHighSpeed;
      0006B0 75 22 00         [24]  912 	mov	_usb_speed,#0x00
      0006B3 80 13            [24]  913 	sjmp	00109$
      0006B5                        914 00105$:
                                    915 ;	usb.c:200: else if ((USBSTAT & bmSpeed) == bmFullSpeed)
      0006B5 90 F0 09         [24]  916 	mov	dptr,#_USBSTAT
      0006B8 E0               [24]  917 	movx	a,@dptr
      0006B9 FF               [12]  918 	mov	r7,a
      0006BA 53 07 07         [24]  919 	anl	ar7,#0x07
      0006BD BF 01 05         [24]  920 	cjne	r7,#0x01,00102$
                                    921 ;	usb.c:202: usb_speed = bmFullSpeed;
      0006C0 75 22 01         [24]  922 	mov	_usb_speed,#0x01
      0006C3 80 03            [24]  923 	sjmp	00109$
      0006C5                        924 00102$:
                                    925 ;	usb.c:206: usb_speed = 0;
      0006C5 75 22 00         [24]  926 	mov	_usb_speed,#0x00
      0006C8                        927 00109$:
                                    928 ;	usb.c:209: EX1 = 1;
      0006C8 D2 AA            [12]  929 	setb	_EX1
                                    930 ;	usb.c:210: EX0 = 1;
      0006CA D2 A8            [12]  931 	setb	_EX0
                                    932 ;	usb.c:211: EPIE = bmEP2IRQ | bmEP4IRQ;
      0006CC 90 F0 30         [24]  933 	mov	dptr,#_EPIE
      0006CF 74 0A            [12]  934 	mov	a,#0x0A
      0006D1 F0               [24]  935 	movx	@dptr,a
                                    936 ;	usb.c:212: scsi_data_residue = 0;
      0006D2 E4               [12]  937 	clr	a
      0006D3 F5 26            [12]  938 	mov	_scsi_data_residue,a
      0006D5 F5 27            [12]  939 	mov	(_scsi_data_residue + 1),a
      0006D7 F5 28            [12]  940 	mov	(_scsi_data_residue + 2),a
      0006D9 F5 29            [12]  941 	mov	(_scsi_data_residue + 3),a
                                    942 ;	usb.c:213: scsi_status = 0;
                                    943 ;	1-genFromRTrack replaced	mov	_scsi_status,#0x00
      0006DB F5 25            [12]  944 	mov	_scsi_status,a
                                    945 ;	usb.c:214: SendCSW();
      0006DD 02 05 40         [24]  946 	ljmp	_SendCSW
      0006E0                        947 00112$:
                                    948 ;	usb.c:219: REGBANK = 6;
      0006E0 90 F0 00         [24]  949 	mov	dptr,#_REGBANK
      0006E3 74 06            [12]  950 	mov	a,#0x06
      0006E5 F0               [24]  951 	movx	@dptr,a
                                    952 ;	usb.c:220: XVAL(0xF240) = 2;
      0006E6 90 F2 40         [24]  953 	mov	dptr,#0xF240
      0006E9 74 02            [12]  954 	mov	a,#0x02
      0006EB F0               [24]  955 	movx	@dptr,a
                                    956 ;	usb.c:221: XVAL(0xF28C) = 0x36;
      0006EC 90 F2 8C         [24]  957 	mov	dptr,#0xF28C
      0006EF 74 36            [12]  958 	mov	a,#0x36
      0006F1 F0               [24]  959 	movx	@dptr,a
                                    960 ;	usb.c:222: XVAL(0xF28D) = 0xD0;
      0006F2 90 F2 8D         [24]  961 	mov	dptr,#0xF28D
      0006F5 74 D0            [12]  962 	mov	a,#0xD0
      0006F7 F0               [24]  963 	movx	@dptr,a
                                    964 ;	usb.c:223: XVAL(0xF28E) = 0x98;
      0006F8 90 F2 8E         [24]  965 	mov	dptr,#0xF28E
      0006FB 74 98            [12]  966 	mov	a,#0x98
      0006FD F0               [24]  967 	movx	@dptr,a
                                    968 ;	usb.c:224: REGBANK = 0;
      0006FE 90 F0 00         [24]  969 	mov	dptr,#_REGBANK
      000701 E4               [12]  970 	clr	a
      000702 F0               [24]  971 	movx	@dptr,a
                                    972 ;	usb.c:225: EPIE = bmEP2IRQ | bmEP4IRQ;
      000703 90 F0 30         [24]  973 	mov	dptr,#_EPIE
      000706 74 0A            [12]  974 	mov	a,#0x0A
      000708 F0               [24]  975 	movx	@dptr,a
                                    976 ;	usb.c:226: USBCTL = bmAttach | bmSuperSpeed;
      000709 90 F0 08         [24]  977 	mov	dptr,#_USBCTL
      00070C 74 84            [12]  978 	mov	a,#0x84
      00070E F0               [24]  979 	movx	@dptr,a
                                    980 ;	usb.c:228: XVAL(0xFA38) |= 2;
      00070F 90 FA 38         [24]  981 	mov	dptr,#0xFA38
      000712 E0               [24]  982 	movx	a,@dptr
      000713 44 02            [12]  983 	orl	a,#0x02
      000715 F0               [24]  984 	movx	@dptr,a
                                    985 ;	usb.c:230: EX1 = 1;
      000716 D2 AA            [12]  986 	setb	_EX1
                                    987 ;	usb.c:231: EX0 = 1;
      000718 D2 A8            [12]  988 	setb	_EX0
                                    989 ;	usb.c:232: for (b = 0; b < 250; b++);			
      00071A 7F FA            [12]  990 	mov	r7,#0xFA
      00071C                        991 00116$:
      00071C 8F 06            [24]  992 	mov	ar6,r7
      00071E 1E               [12]  993 	dec	r6
      00071F EE               [12]  994 	mov	a,r6
      000720 FF               [12]  995 	mov	r7,a
      000721 70 F9            [24]  996 	jnz	00116$
      000723 22               [24]  997 	ret
                                    998 ;------------------------------------------------------------
                                    999 ;Allocation info for local variables in function 'usb_isr'
                                   1000 ;------------------------------------------------------------
                                   1001 ;	usb.c:236: void usb_isr(void) __interrupt USB_VECT
                                   1002 ;	-----------------------------------------
                                   1003 ;	 function usb_isr
                                   1004 ;	-----------------------------------------
      000724                       1005 _usb_isr:
      000724 C0 E0            [24] 1006 	push	acc
      000726 C0 82            [24] 1007 	push	dpl
      000728 C0 83            [24] 1008 	push	dph
      00072A C0 07            [24] 1009 	push	ar7
      00072C C0 06            [24] 1010 	push	ar6
      00072E C0 05            [24] 1011 	push	ar5
      000730 C0 04            [24] 1012 	push	ar4
      000732 C0 03            [24] 1013 	push	ar3
      000734 C0 02            [24] 1014 	push	ar2
      000736 C0 01            [24] 1015 	push	ar1
      000738 C0 00            [24] 1016 	push	ar0
      00073A C0 D0            [24] 1017 	push	psw
      00073C 75 D0 00         [24] 1018 	mov	psw,#0x00
                                   1019 ;	usb.c:238: usb_irq = USBIRQ;
      00073F 90 F0 27         [24] 1020 	mov	dptr,#_USBIRQ
      000742 E0               [24] 1021 	movx	a,@dptr
      000743 FF               [12] 1022 	mov	r7,a
      000744 90 60 00         [24] 1023 	mov	dptr,#_usb_irq
      000747 F0               [24] 1024 	movx	@dptr,a
                                   1025 ;	usb.c:240: if (usb_irq & 0x20)
      000748 EF               [12] 1026 	mov	a,r7
      000749 30 E5 06         [24] 1027 	jnb	acc.5,00102$
                                   1028 ;	usb.c:242: USBIRQ = 0x20;
      00074C 90 F0 27         [24] 1029 	mov	dptr,#_USBIRQ
      00074F 74 20            [12] 1030 	mov	a,#0x20
      000751 F0               [24] 1031 	movx	@dptr,a
      000752                       1032 00102$:
                                   1033 ;	usb.c:245: if (usb_irq & 0x10)
      000752 EF               [12] 1034 	mov	a,r7
      000753 30 E4 06         [24] 1035 	jnb	acc.4,00104$
                                   1036 ;	usb.c:247: USBIRQ = 0x10;
      000756 90 F0 27         [24] 1037 	mov	dptr,#_USBIRQ
      000759 74 10            [12] 1038 	mov	a,#0x10
      00075B F0               [24] 1039 	movx	@dptr,a
      00075C                       1040 00104$:
                                   1041 ;	usb.c:250: if (usb_irq & bmSpeedChange)
      00075C EF               [12] 1042 	mov	a,r7
      00075D 30 E7 36         [24] 1043 	jnb	acc.7,00115$
                                   1044 ;	usb.c:252: USBIRQ = bmSpeedChange;
      000760 90 F0 27         [24] 1045 	mov	dptr,#_USBIRQ
      000763 74 80            [12] 1046 	mov	a,#0x80
      000765 F0               [24] 1047 	movx	@dptr,a
                                   1048 ;	usb.c:253: if ((USBSTAT & bmSpeed) == bmSuperSpeed)
      000766 90 F0 09         [24] 1049 	mov	dptr,#_USBSTAT
      000769 E0               [24] 1050 	movx	a,@dptr
      00076A FE               [12] 1051 	mov	r6,a
      00076B 53 06 07         [24] 1052 	anl	ar6,#0x07
      00076E BE 04 05         [24] 1053 	cjne	r6,#0x04,00112$
                                   1054 ;	usb.c:255: usb_speed = bmSuperSpeed;
      000771 75 22 04         [24] 1055 	mov	_usb_speed,#0x04
      000774 80 20            [24] 1056 	sjmp	00115$
      000776                       1057 00112$:
                                   1058 ;	usb.c:257: else if ((USBSTAT & bmSpeed) == bmHighSpeed)
      000776 90 F0 09         [24] 1059 	mov	dptr,#_USBSTAT
      000779 E0               [24] 1060 	movx	a,@dptr
      00077A FE               [12] 1061 	mov	r6,a
      00077B 54 07            [12] 1062 	anl	a,#0x07
                                   1063 ;	usb.c:259: usb_speed = bmHighSpeed;
      00077D 70 04            [24] 1064 	jnz	00109$
      00077F F5 22            [12] 1065 	mov	_usb_speed,a
      000781 80 13            [24] 1066 	sjmp	00115$
      000783                       1067 00109$:
                                   1068 ;	usb.c:261: else if ((USBSTAT & bmSpeed) == bmFullSpeed)
      000783 90 F0 09         [24] 1069 	mov	dptr,#_USBSTAT
      000786 E0               [24] 1070 	movx	a,@dptr
      000787 FE               [12] 1071 	mov	r6,a
      000788 53 06 07         [24] 1072 	anl	ar6,#0x07
      00078B BE 01 05         [24] 1073 	cjne	r6,#0x01,00106$
                                   1074 ;	usb.c:263: usb_speed = bmFullSpeed;
      00078E 75 22 01         [24] 1075 	mov	_usb_speed,#0x01
      000791 80 03            [24] 1076 	sjmp	00115$
      000793                       1077 00106$:
                                   1078 ;	usb.c:267: usb_speed = 0;
      000793 75 22 00         [24] 1079 	mov	_usb_speed,#0x00
      000796                       1080 00115$:
                                   1081 ;	usb.c:271: if (usb_irq & 0x40)
      000796 EF               [12] 1082 	mov	a,r7
      000797 30 E6 06         [24] 1083 	jnb	acc.6,00117$
                                   1084 ;	usb.c:273: USBIRQ = 0x40;
      00079A 90 F0 27         [24] 1085 	mov	dptr,#_USBIRQ
      00079D 74 40            [12] 1086 	mov	a,#0x40
      00079F F0               [24] 1087 	movx	@dptr,a
      0007A0                       1088 00117$:
                                   1089 ;	usb.c:276: UsbIntStsF087 = XVAL(0xF087);
      0007A0 90 F0 87         [24] 1090 	mov	dptr,#0xF087
      0007A3 E0               [24] 1091 	movx	a,@dptr
      0007A4 FE               [12] 1092 	mov	r6,a
      0007A5 90 60 04         [24] 1093 	mov	dptr,#_UsbIntStsF087
      0007A8 F0               [24] 1094 	movx	@dptr,a
                                   1095 ;	usb.c:277: UsbIntStsF086 = XVAL(0xF086);
      0007A9 90 F0 86         [24] 1096 	mov	dptr,#0xF086
      0007AC E0               [24] 1097 	movx	a,@dptr
      0007AD FD               [12] 1098 	mov	r5,a
      0007AE 90 60 03         [24] 1099 	mov	dptr,#_UsbIntStsF086
      0007B1 F0               [24] 1100 	movx	@dptr,a
                                   1101 ;	usb.c:278: UsbIntStsF082 = XVAL(0xF082);
      0007B2 90 F0 82         [24] 1102 	mov	dptr,#0xF082
      0007B5 E0               [24] 1103 	movx	a,@dptr
      0007B6 FC               [12] 1104 	mov	r4,a
      0007B7 90 60 02         [24] 1105 	mov	dptr,#_UsbIntStsF082
      0007BA F0               [24] 1106 	movx	@dptr,a
                                   1107 ;	usb.c:279: UsbIntStsF080 = XVAL(0xF080);
      0007BB 90 F0 80         [24] 1108 	mov	dptr,#0xF080
      0007BE E0               [24] 1109 	movx	a,@dptr
      0007BF FB               [12] 1110 	mov	r3,a
      0007C0 90 60 01         [24] 1111 	mov	dptr,#_UsbIntStsF080
      0007C3 F0               [24] 1112 	movx	@dptr,a
                                   1113 ;	usb.c:281: if (UsbIntStsF082 & 0x80)
      0007C4 EC               [12] 1114 	mov	a,r4
      0007C5 30 E7 06         [24] 1115 	jnb	acc.7,00119$
                                   1116 ;	usb.c:283: XVAL(0xF082) = 0x80;
      0007C8 90 F0 82         [24] 1117 	mov	dptr,#0xF082
      0007CB 74 80            [12] 1118 	mov	a,#0x80
      0007CD F0               [24] 1119 	movx	@dptr,a
      0007CE                       1120 00119$:
                                   1121 ;	usb.c:286: if (UsbIntStsF082 & 0x40)
      0007CE EC               [12] 1122 	mov	a,r4
      0007CF 30 E6 06         [24] 1123 	jnb	acc.6,00121$
                                   1124 ;	usb.c:288: XVAL(0xF082) = 0x40;
      0007D2 90 F0 82         [24] 1125 	mov	dptr,#0xF082
      0007D5 74 40            [12] 1126 	mov	a,#0x40
      0007D7 F0               [24] 1127 	movx	@dptr,a
      0007D8                       1128 00121$:
                                   1129 ;	usb.c:291: if (UsbIntStsF080 & 1)
      0007D8 EB               [12] 1130 	mov	a,r3
      0007D9 30 E0 61         [24] 1131 	jnb	acc.0,00125$
                                   1132 ;	usb.c:293: XVAL(0xF080) = 1;
      0007DC 90 F0 80         [24] 1133 	mov	dptr,#0xF080
      0007DF 74 01            [12] 1134 	mov	a,#0x01
      0007E1 F0               [24] 1135 	movx	@dptr,a
                                   1136 ;	usb.c:294: if (EP0CS & bmSUDAV)
      0007E2 90 F0 48         [24] 1137 	mov	dptr,#_EP0CS
      0007E5 E0               [24] 1138 	movx	a,@dptr
      0007E6 FA               [12] 1139 	mov	r2,a
      0007E7 30 E7 53         [24] 1140 	jnb	acc.7,00125$
                                   1141 ;	usb.c:296: bmRequestType = SETUPDAT[0];
      0007EA C0 05            [24] 1142 	push	ar5
      0007EC 90 F0 B8         [24] 1143 	mov	dptr,#_SETUPDAT
      0007EF E0               [24] 1144 	movx	a,@dptr
      0007F0 F5 1A            [12] 1145 	mov	_bmRequestType,a
                                   1146 ;	usb.c:297: bRequest = SETUPDAT[1];
      0007F2 90 F0 B9         [24] 1147 	mov	dptr,#(_SETUPDAT + 0x0001)
      0007F5 E0               [24] 1148 	movx	a,@dptr
      0007F6 F5 1B            [12] 1149 	mov	_bRequest,a
                                   1150 ;	usb.c:298: wValue = SETUPDAT[2] | (SETUPDAT[3] << 8);
      0007F8 90 F0 BA         [24] 1151 	mov	dptr,#(_SETUPDAT + 0x0002)
      0007FB E0               [24] 1152 	movx	a,@dptr
      0007FC FA               [12] 1153 	mov	r2,a
      0007FD 90 F0 BB         [24] 1154 	mov	dptr,#(_SETUPDAT + 0x0003)
      000800 E0               [24] 1155 	movx	a,@dptr
      000801 F9               [12] 1156 	mov	r1,a
      000802 E4               [12] 1157 	clr	a
      000803 FD               [12] 1158 	mov	r5,a
      000804 4A               [12] 1159 	orl	a,r2
      000805 F5 1C            [12] 1160 	mov	_wValue,a
      000807 E9               [12] 1161 	mov	a,r1
      000808 4D               [12] 1162 	orl	a,r5
      000809 F5 1D            [12] 1163 	mov	(_wValue + 1),a
                                   1164 ;	usb.c:299: wIndex = SETUPDAT[4] | (SETUPDAT[5] << 8);
      00080B 90 F0 BC         [24] 1165 	mov	dptr,#(_SETUPDAT + 0x0004)
      00080E E0               [24] 1166 	movx	a,@dptr
      00080F FD               [12] 1167 	mov	r5,a
      000810 90 F0 BD         [24] 1168 	mov	dptr,#(_SETUPDAT + 0x0005)
      000813 E0               [24] 1169 	movx	a,@dptr
      000814 FA               [12] 1170 	mov	r2,a
      000815 79 00            [12] 1171 	mov	r1,#0x00
      000817 8D 00            [24] 1172 	mov	ar0,r5
      000819 7D 00            [12] 1173 	mov	r5,#0x00
      00081B E9               [12] 1174 	mov	a,r1
      00081C 48               [12] 1175 	orl	a,r0
      00081D F5 1E            [12] 1176 	mov	_wIndex,a
      00081F EA               [12] 1177 	mov	a,r2
      000820 4D               [12] 1178 	orl	a,r5
      000821 F5 1F            [12] 1179 	mov	(_wIndex + 1),a
                                   1180 ;	usb.c:300: wLength = SETUPDAT[6] | (SETUPDAT[7] << 8);
      000823 90 F0 BE         [24] 1181 	mov	dptr,#(_SETUPDAT + 0x0006)
      000826 E0               [24] 1182 	movx	a,@dptr
      000827 FD               [12] 1183 	mov	r5,a
      000828 90 F0 BF         [24] 1184 	mov	dptr,#(_SETUPDAT + 0x0007)
      00082B E0               [24] 1185 	movx	a,@dptr
      00082C FA               [12] 1186 	mov	r2,a
      00082D 79 00            [12] 1187 	mov	r1,#0x00
      00082F 8D 00            [24] 1188 	mov	ar0,r5
      000831 7D 00            [12] 1189 	mov	r5,#0x00
      000833 E9               [12] 1190 	mov	a,r1
      000834 48               [12] 1191 	orl	a,r0
      000835 F5 20            [12] 1192 	mov	_wLength,a
      000837 EA               [12] 1193 	mov	a,r2
      000838 4D               [12] 1194 	orl	a,r5
      000839 F5 21            [12] 1195 	mov	(_wLength + 1),a
                                   1196 ;	usb.c:321: EX0 = 0;
      00083B D0 05            [24] 1197 	pop	ar5
                                   1198 ;	usb.c:300: wLength = SETUPDAT[6] | (SETUPDAT[7] << 8);
      00083D                       1199 00125$:
                                   1200 ;	usb.c:304: if (XVAL(0xF082) & 0x20)
      00083D 90 F0 82         [24] 1201 	mov	dptr,#0xF082
      000840 E0               [24] 1202 	movx	a,@dptr
      000841 FA               [12] 1203 	mov	r2,a
      000842 30 E5 06         [24] 1204 	jnb	acc.5,00127$
                                   1205 ;	usb.c:306: XVAL(0xF082) = 0x20;
      000845 90 F0 82         [24] 1206 	mov	dptr,#0xF082
      000848 74 20            [12] 1207 	mov	a,#0x20
      00084A F0               [24] 1208 	movx	@dptr,a
      00084B                       1209 00127$:
                                   1210 ;	usb.c:309: if (XVAL(0xF081) & 0x10)
      00084B 90 F0 81         [24] 1211 	mov	dptr,#0xF081
      00084E E0               [24] 1212 	movx	a,@dptr
      00084F FA               [12] 1213 	mov	r2,a
      000850 30 E4 06         [24] 1214 	jnb	acc.4,00129$
                                   1215 ;	usb.c:311: XVAL(0xF081) = 0x10;
      000853 90 F0 81         [24] 1216 	mov	dptr,#0xF081
      000856 74 10            [12] 1217 	mov	a,#0x10
      000858 F0               [24] 1218 	movx	@dptr,a
      000859                       1219 00129$:
                                   1220 ;	usb.c:314: if (XVAL(0xF081) & 0x20)
      000859 90 F0 81         [24] 1221 	mov	dptr,#0xF081
      00085C E0               [24] 1222 	movx	a,@dptr
      00085D FA               [12] 1223 	mov	r2,a
      00085E 30 E5 06         [24] 1224 	jnb	acc.5,00131$
                                   1225 ;	usb.c:316: XVAL(0xF081) = 0x20;
      000861 90 F0 81         [24] 1226 	mov	dptr,#0xF081
      000864 74 20            [12] 1227 	mov	a,#0x20
      000866 F0               [24] 1228 	movx	@dptr,a
      000867                       1229 00131$:
                                   1230 ;	usb.c:319: if (UsbIntStsF080 | UsbIntStsF082 | UsbIntStsF086 | UsbIntStsF087 | usb_irq)
      000867 EC               [12] 1231 	mov	a,r4
      000868 4B               [12] 1232 	orl	a,r3
      000869 4D               [12] 1233 	orl	a,r5
      00086A 4E               [12] 1234 	orl	a,r6
      00086B 4F               [12] 1235 	orl	a,r7
      00086C 60 02            [24] 1236 	jz	00134$
                                   1237 ;	usb.c:321: EX0 = 0;
      00086E C2 A8            [12] 1238 	clr	_EX0
      000870                       1239 00134$:
      000870 D0 D0            [24] 1240 	pop	psw
      000872 D0 00            [24] 1241 	pop	ar0
      000874 D0 01            [24] 1242 	pop	ar1
      000876 D0 02            [24] 1243 	pop	ar2
      000878 D0 03            [24] 1244 	pop	ar3
      00087A D0 04            [24] 1245 	pop	ar4
      00087C D0 05            [24] 1246 	pop	ar5
      00087E D0 06            [24] 1247 	pop	ar6
      000880 D0 07            [24] 1248 	pop	ar7
      000882 D0 83            [24] 1249 	pop	dph
      000884 D0 82            [24] 1250 	pop	dpl
      000886 D0 E0            [24] 1251 	pop	acc
      000888 32               [24] 1252 	reti
                                   1253 ;	eliminated unneeded push/pop b
                                   1254 ;------------------------------------------------------------
                                   1255 ;Allocation info for local variables in function 'ep_isr'
                                   1256 ;------------------------------------------------------------
                                   1257 ;interrupts                Allocated to registers r7 
                                   1258 ;------------------------------------------------------------
                                   1259 ;	usb.c:325: void ep_isr(void) __interrupt EP_VECT
                                   1260 ;	-----------------------------------------
                                   1261 ;	 function ep_isr
                                   1262 ;	-----------------------------------------
      000889                       1263 _ep_isr:
      000889 C0 E0            [24] 1264 	push	acc
      00088B C0 82            [24] 1265 	push	dpl
      00088D C0 83            [24] 1266 	push	dph
      00088F C0 07            [24] 1267 	push	ar7
      000891 C0 06            [24] 1268 	push	ar6
      000893 C0 D0            [24] 1269 	push	psw
      000895 75 D0 00         [24] 1270 	mov	psw,#0x00
                                   1271 ;	usb.c:327: BYTE interrupts = (EPIRQ & (bmEP2IRQ | bmEP4IRQ));
      000898 90 F0 20         [24] 1272 	mov	dptr,#_EPIRQ
      00089B E0               [24] 1273 	movx	a,@dptr
                                   1274 ;	usb.c:328: if (interrupts & bmEP2IRQ)
      00089C 54 0A            [12] 1275 	anl	a,#0x0A
      00089E FF               [12] 1276 	mov	r7,a
      00089F 30 E1 18         [24] 1277 	jnb	acc.1,00102$
                                   1278 ;	usb.c:330: EPIE &= ~bmEP2IRQ; //disable this 
      0008A2 90 F0 30         [24] 1279 	mov	dptr,#_EPIE
      0008A5 E0               [24] 1280 	movx	a,@dptr
      0008A6 FE               [12] 1281 	mov	r6,a
      0008A7 74 FD            [12] 1282 	mov	a,#0xFD
      0008A9 5E               [12] 1283 	anl	a,r6
      0008AA F0               [24] 1284 	movx	@dptr,a
                                   1285 ;	usb.c:331: EPIRQ = bmEP2IRQ; //acknowledge it
      0008AB 90 F0 20         [24] 1286 	mov	dptr,#_EPIRQ
      0008AE 74 02            [12] 1287 	mov	a,#0x02
      0008B0 F0               [24] 1288 	movx	@dptr,a
                                   1289 ;	usb.c:332: usb_received_data_ready |= bmEP2IRQ;
      0008B1 90 60 05         [24] 1290 	mov	dptr,#_usb_received_data_ready
      0008B4 E0               [24] 1291 	movx	a,@dptr
      0008B5 FE               [12] 1292 	mov	r6,a
      0008B6 74 02            [12] 1293 	mov	a,#0x02
      0008B8 4E               [12] 1294 	orl	a,r6
      0008B9 F0               [24] 1295 	movx	@dptr,a
      0008BA                       1296 00102$:
                                   1297 ;	usb.c:335: if (interrupts & bmEP4IRQ)
      0008BA EF               [12] 1298 	mov	a,r7
      0008BB 30 E3 18         [24] 1299 	jnb	acc.3,00105$
                                   1300 ;	usb.c:337: EPIE &= ~bmEP4IRQ; //disable this 
      0008BE 90 F0 30         [24] 1301 	mov	dptr,#_EPIE
      0008C1 E0               [24] 1302 	movx	a,@dptr
      0008C2 FF               [12] 1303 	mov	r7,a
      0008C3 74 F7            [12] 1304 	mov	a,#0xF7
      0008C5 5F               [12] 1305 	anl	a,r7
      0008C6 F0               [24] 1306 	movx	@dptr,a
                                   1307 ;	usb.c:338: EPIRQ = bmEP4IRQ; //acknowledge it
      0008C7 90 F0 20         [24] 1308 	mov	dptr,#_EPIRQ
      0008CA 74 08            [12] 1309 	mov	a,#0x08
      0008CC F0               [24] 1310 	movx	@dptr,a
                                   1311 ;	usb.c:339: usb_received_data_ready |= bmEP4IRQ;
      0008CD 90 60 05         [24] 1312 	mov	dptr,#_usb_received_data_ready
      0008D0 E0               [24] 1313 	movx	a,@dptr
      0008D1 FF               [12] 1314 	mov	r7,a
      0008D2 74 08            [12] 1315 	mov	a,#0x08
      0008D4 4F               [12] 1316 	orl	a,r7
      0008D5 F0               [24] 1317 	movx	@dptr,a
      0008D6                       1318 00105$:
      0008D6 D0 D0            [24] 1319 	pop	psw
      0008D8 D0 06            [24] 1320 	pop	ar6
      0008DA D0 07            [24] 1321 	pop	ar7
      0008DC D0 83            [24] 1322 	pop	dph
      0008DE D0 82            [24] 1323 	pop	dpl
      0008E0 D0 E0            [24] 1324 	pop	acc
      0008E2 32               [24] 1325 	reti
                                   1326 ;	eliminated unneeded push/pop b
                                   1327 ;------------------------------------------------------------
                                   1328 ;Allocation info for local variables in function 'ResetEPs'
                                   1329 ;------------------------------------------------------------
                                   1330 ;	usb.c:343: static void ResetEPs()
                                   1331 ;	-----------------------------------------
                                   1332 ;	 function ResetEPs
                                   1333 ;	-----------------------------------------
      0008E3                       1334 _ResetEPs:
                                   1335 ;	usb.c:345: EPIE = bmEP2IRQ | bmEP4IRQ;
      0008E3 90 F0 30         [24] 1336 	mov	dptr,#_EPIE
      0008E6 74 0A            [12] 1337 	mov	a,#0x0A
      0008E8 F0               [24] 1338 	movx	@dptr,a
                                   1339 ;	usb.c:346: EP1.cs = 0;
      0008E9 90 F2 13         [24] 1340 	mov	dptr,#(_EP1 + 0x0013)
      0008EC E4               [12] 1341 	clr	a
      0008ED F0               [24] 1342 	movx	@dptr,a
                                   1343 ;	usb.c:347: EP2.cs = 0;
      0008EE 90 F2 53         [24] 1344 	mov	dptr,#(_EP2 + 0x0013)
      0008F1 F0               [24] 1345 	movx	@dptr,a
                                   1346 ;	usb.c:348: EP3.cs = 0;
      0008F2 90 F2 93         [24] 1347 	mov	dptr,#(_EP3 + 0x0013)
      0008F5 F0               [24] 1348 	movx	@dptr,a
                                   1349 ;	usb.c:349: EP4.cs = 0;
      0008F6 90 F2 D3         [24] 1350 	mov	dptr,#(_EP4 + 0x0013)
      0008F9 F0               [24] 1351 	movx	@dptr,a
      0008FA 22               [24] 1352 	ret
                                   1353 ;------------------------------------------------------------
                                   1354 ;Allocation info for local variables in function 'HandleControlRequest'
                                   1355 ;------------------------------------------------------------
                                   1356 ;res                       Allocated to registers r7 
                                   1357 ;------------------------------------------------------------
                                   1358 ;	usb.c:352: static void HandleControlRequest(void)
                                   1359 ;	-----------------------------------------
                                   1360 ;	 function HandleControlRequest
                                   1361 ;	-----------------------------------------
      0008FB                       1362 _HandleControlRequest:
                                   1363 ;	usb.c:355: switch(bmRequestType & 0x60)
      0008FB 74 60            [12] 1364 	mov	a,#0x60
      0008FD 55 1A            [12] 1365 	anl	a,_bmRequestType
      0008FF FF               [12] 1366 	mov	r7,a
      000900 60 0A            [24] 1367 	jz	00101$
      000902 BF 20 02         [24] 1368 	cjne	r7,#0x20,00128$
      000905 80 0C            [24] 1369 	sjmp	00102$
      000907                       1370 00128$:
                                   1371 ;	usb.c:357: case 0:
      000907 BF 40 17         [24] 1372 	cjne	r7,#0x40,00104$
      00090A 80 0E            [24] 1373 	sjmp	00103$
      00090C                       1374 00101$:
                                   1375 ;	usb.c:358: res = HandleStandardRequest();
      00090C 12 0C 66         [24] 1376 	lcall	_HandleStandardRequest
      00090F AF 82            [24] 1377 	mov	r7,dpl
                                   1378 ;	usb.c:359: break;
                                   1379 ;	usb.c:360: case 0x20:
      000911 80 10            [24] 1380 	sjmp	00105$
      000913                       1381 00102$:
                                   1382 ;	usb.c:361: res = HandleClassRequest();
      000913 12 0C AD         [24] 1383 	lcall	_HandleClassRequest
      000916 AF 82            [24] 1384 	mov	r7,dpl
                                   1385 ;	usb.c:362: break;
                                   1386 ;	usb.c:363: case 0x40:
      000918 80 09            [24] 1387 	sjmp	00105$
      00091A                       1388 00103$:
                                   1389 ;	usb.c:364: res = HandleVendorRequest();
      00091A 12 0C DA         [24] 1390 	lcall	_HandleVendorRequest
      00091D AF 82            [24] 1391 	mov	r7,dpl
                                   1392 ;	usb.c:365: break;
                                   1393 ;	usb.c:366: default:
      00091F 80 02            [24] 1394 	sjmp	00105$
      000921                       1395 00104$:
                                   1396 ;	usb.c:367: res = FALSE;
      000921 7F 00            [12] 1397 	mov	r7,#0x00
                                   1398 ;	usb.c:368: }
      000923                       1399 00105$:
                                   1400 ;	usb.c:370: if (!res)
      000923 EF               [12] 1401 	mov	a,r7
      000924 70 11            [24] 1402 	jnz	00108$
                                   1403 ;	usb.c:372: EP0CS = wLength ? bmEP0STALL : bmEP0NAK;
      000926 E5 20            [12] 1404 	mov	a,_wLength
      000928 45 21            [12] 1405 	orl	a,(_wLength + 1)
      00092A 60 04            [24] 1406 	jz	00110$
      00092C 7F 08            [12] 1407 	mov	r7,#0x08
      00092E 80 02            [24] 1408 	sjmp	00111$
      000930                       1409 00110$:
      000930 7F 02            [12] 1410 	mov	r7,#0x02
      000932                       1411 00111$:
      000932 90 F0 48         [24] 1412 	mov	dptr,#_EP0CS
      000935 EF               [12] 1413 	mov	a,r7
      000936 F0               [24] 1414 	movx	@dptr,a
      000937                       1415 00108$:
      000937 22               [24] 1416 	ret
                                   1417 ;------------------------------------------------------------
                                   1418 ;Allocation info for local variables in function 'HandleUSBEvents'
                                   1419 ;------------------------------------------------------------
                                   1420 ;a                         Allocated to registers r7 
                                   1421 ;b                         Allocated to registers r6 
                                   1422 ;c                         Allocated to registers r5 
                                   1423 ;d                         Allocated to registers r4 
                                   1424 ;------------------------------------------------------------
                                   1425 ;	usb.c:376: void HandleUSBEvents(void)
                                   1426 ;	-----------------------------------------
                                   1427 ;	 function HandleUSBEvents
                                   1428 ;	-----------------------------------------
      000938                       1429 _HandleUSBEvents:
                                   1430 ;	usb.c:378: if (UsbIntStsF080 | UsbIntStsF082 | UsbIntStsF086 | UsbIntStsF087 | usb_irq)
      000938 90 60 02         [24] 1431 	mov	dptr,#_UsbIntStsF082
      00093B E0               [24] 1432 	movx	a,@dptr
      00093C FF               [12] 1433 	mov	r7,a
      00093D 90 60 01         [24] 1434 	mov	dptr,#_UsbIntStsF080
      000940 E0               [24] 1435 	movx	a,@dptr
      000941 FE               [12] 1436 	mov	r6,a
      000942 4F               [12] 1437 	orl	a,r7
      000943 FD               [12] 1438 	mov	r5,a
      000944 90 60 03         [24] 1439 	mov	dptr,#_UsbIntStsF086
      000947 E0               [24] 1440 	movx	a,@dptr
      000948 42 05            [12] 1441 	orl	ar5,a
      00094A 90 60 04         [24] 1442 	mov	dptr,#_UsbIntStsF087
      00094D E0               [24] 1443 	movx	a,@dptr
      00094E 42 05            [12] 1444 	orl	ar5,a
      000950 90 60 00         [24] 1445 	mov	dptr,#_usb_irq
      000953 E0               [24] 1446 	movx	a,@dptr
      000954 FC               [12] 1447 	mov	r4,a
      000955 4D               [12] 1448 	orl	a,r5
      000956 60 79            [24] 1449 	jz	00144$
                                   1450 ;	usb.c:380: if (usb_irq)
      000958 EC               [12] 1451 	mov	a,r4
      000959 60 3B            [24] 1452 	jz	00116$
                                   1453 ;	usb.c:382: if (usb_irq & 0x40)
      00095B EC               [12] 1454 	mov	a,r4
      00095C 30 E6 25         [24] 1455 	jnb	acc.6,00105$
                                   1456 ;	usb.c:384: USBCTL &= ~bmAttach;
      00095F 90 F0 08         [24] 1457 	mov	dptr,#_USBCTL
      000962 E0               [24] 1458 	movx	a,@dptr
      000963 FD               [12] 1459 	mov	r5,a
      000964 74 7F            [12] 1460 	mov	a,#0x7F
      000966 5D               [12] 1461 	anl	a,r5
      000967 F0               [24] 1462 	movx	@dptr,a
                                   1463 ;	usb.c:385: ResetEPs();
      000968 12 08 E3         [24] 1464 	lcall	_ResetEPs
                                   1465 ;	usb.c:386: XVAL(0xFE88) = 0;
      00096B 90 FE 88         [24] 1466 	mov	dptr,#0xFE88
      00096E E4               [12] 1467 	clr	a
      00096F F0               [24] 1468 	movx	@dptr,a
                                   1469 ;	usb.c:387: XVAL(0xFE82) = 0x10;
      000970 90 FE 82         [24] 1470 	mov	dptr,#0xFE82
      000973 74 10            [12] 1471 	mov	a,#0x10
      000975 F0               [24] 1472 	movx	@dptr,a
                                   1473 ;	usb.c:388: while(XVAL(0xFE88)!=2);
      000976                       1474 00101$:
      000976 90 FE 88         [24] 1475 	mov	dptr,#0xFE88
      000979 E0               [24] 1476 	movx	a,@dptr
      00097A FD               [12] 1477 	mov	r5,a
      00097B BD 02 F8         [24] 1478 	cjne	r5,#0x02,00101$
                                   1479 ;	usb.c:389: USBCTL = bmAttach;
      00097E 90 F0 08         [24] 1480 	mov	dptr,#_USBCTL
      000981 74 80            [12] 1481 	mov	a,#0x80
      000983 F0               [24] 1482 	movx	@dptr,a
      000984                       1483 00105$:
                                   1484 ;	usb.c:392: if (usb_irq & bmSpeedChange)
      000984 90 60 00         [24] 1485 	mov	dptr,#_usb_irq
      000987 E0               [24] 1486 	movx	a,@dptr
      000988 FD               [12] 1487 	mov	r5,a
      000989 30 E7 03         [24] 1488 	jnb	acc.7,00107$
                                   1489 ;	usb.c:394: ResetEPs();
      00098C 12 08 E3         [24] 1490 	lcall	_ResetEPs
      00098F                       1491 00107$:
                                   1492 ;	usb.c:397: usb_irq = 0;
      00098F 90 60 00         [24] 1493 	mov	dptr,#_usb_irq
      000992 E4               [12] 1494 	clr	a
      000993 F0               [24] 1495 	movx	@dptr,a
      000994 80 39            [24] 1496 	sjmp	00117$
      000996                       1497 00116$:
                                   1498 ;	usb.c:401: if (UsbIntStsF082 & 0xC0)
      000996 EF               [12] 1499 	mov	a,r7
      000997 54 C0            [12] 1500 	anl	a,#0xC0
      000999 60 1C            [24] 1501 	jz	00113$
                                   1502 ;	usb.c:403: ResetEPs();
      00099B 12 08 E3         [24] 1503 	lcall	_ResetEPs
                                   1504 ;	usb.c:404: XVAL(0xF092) = 0;
      00099E 90 F0 92         [24] 1505 	mov	dptr,#0xF092
      0009A1 E4               [12] 1506 	clr	a
      0009A2 F0               [24] 1507 	movx	@dptr,a
                                   1508 ;	usb.c:405: XVAL(0xF096) = 0;
      0009A3 90 F0 96         [24] 1509 	mov	dptr,#0xF096
      0009A6 F0               [24] 1510 	movx	@dptr,a
                                   1511 ;	usb.c:406: if (UsbIntStsF082 & 0x40)
      0009A7 90 60 02         [24] 1512 	mov	dptr,#_UsbIntStsF082
      0009AA E0               [24] 1513 	movx	a,@dptr
      0009AB FF               [12] 1514 	mov	r7,a
      0009AC 30 E6 0F         [24] 1515 	jnb	acc.6,00114$
                                   1516 ;	usb.c:408: XVAL(0xF07A) = 1;
      0009AF 90 F0 7A         [24] 1517 	mov	dptr,#0xF07A
      0009B2 74 01            [12] 1518 	mov	a,#0x01
      0009B4 F0               [24] 1519 	movx	@dptr,a
      0009B5 80 07            [24] 1520 	sjmp	00114$
      0009B7                       1521 00113$:
                                   1522 ;	usb.c:413: if (UsbIntStsF080 & 1)
      0009B7 EE               [12] 1523 	mov	a,r6
      0009B8 30 E0 03         [24] 1524 	jnb	acc.0,00114$
                                   1525 ;	usb.c:415: HandleControlRequest();
      0009BB 12 08 FB         [24] 1526 	lcall	_HandleControlRequest
      0009BE                       1527 00114$:
                                   1528 ;	usb.c:419: UsbIntStsF080 = 0;
      0009BE 90 60 01         [24] 1529 	mov	dptr,#_UsbIntStsF080
      0009C1 E4               [12] 1530 	clr	a
      0009C2 F0               [24] 1531 	movx	@dptr,a
                                   1532 ;	usb.c:420: UsbIntStsF082 = 0; 
      0009C3 90 60 02         [24] 1533 	mov	dptr,#_UsbIntStsF082
      0009C6 F0               [24] 1534 	movx	@dptr,a
                                   1535 ;	usb.c:421: UsbIntStsF086 = 0; 
      0009C7 90 60 03         [24] 1536 	mov	dptr,#_UsbIntStsF086
      0009CA F0               [24] 1537 	movx	@dptr,a
                                   1538 ;	usb.c:422: UsbIntStsF087 = 0;
      0009CB 90 60 04         [24] 1539 	mov	dptr,#_UsbIntStsF087
      0009CE F0               [24] 1540 	movx	@dptr,a
      0009CF                       1541 00117$:
                                   1542 ;	usb.c:425: EX0 = 1;	
      0009CF D2 A8            [12] 1543 	setb	_EX0
                                   1544 ;	usb.c:429: if (1)//usb_received_data_ready)
      0009D1                       1545 00144$:
                                   1546 ;	usb.c:433: if (EP4.fifo_count > 0)
      0009D1 90 F2 DA         [24] 1547 	mov	dptr,#(_EP4 + 0x001a)
      0009D4 E0               [24] 1548 	movx	a,@dptr
      0009D5 60 1B            [24] 1549 	jz	00123$
                                   1550 ;	usb.c:435: EP4.cs = 0x40;
      0009D7 90 F2 D3         [24] 1551 	mov	dptr,#(_EP4 + 0x0013)
      0009DA 74 40            [12] 1552 	mov	a,#0x40
      0009DC F0               [24] 1553 	movx	@dptr,a
                                   1554 ;	usb.c:437: send_keys_enabled = 1;
      0009DD 75 0A 01         [24] 1555 	mov	_send_keys_enabled,#0x01
                                   1556 ;	usb.c:438: usb_received_data_ready &= ~bmEP4IRQ;
      0009E0 90 60 05         [24] 1557 	mov	dptr,#_usb_received_data_ready
      0009E3 E0               [24] 1558 	movx	a,@dptr
      0009E4 FF               [12] 1559 	mov	r7,a
      0009E5 74 F7            [12] 1560 	mov	a,#0xF7
      0009E7 5F               [12] 1561 	anl	a,r7
      0009E8 F0               [24] 1562 	movx	@dptr,a
                                   1563 ;	usb.c:439: EPIE |= bmEP4IRQ;
      0009E9 90 F0 30         [24] 1564 	mov	dptr,#_EPIE
      0009EC E0               [24] 1565 	movx	a,@dptr
      0009ED FF               [12] 1566 	mov	r7,a
      0009EE 74 08            [12] 1567 	mov	a,#0x08
      0009F0 4F               [12] 1568 	orl	a,r7
      0009F1 F0               [24] 1569 	movx	@dptr,a
      0009F2                       1570 00123$:
                                   1571 ;	usb.c:443: if (usb_received_data_ready & bmEP2IRQ)
      0009F2 90 60 05         [24] 1572 	mov	dptr,#_usb_received_data_ready
      0009F5 E0               [24] 1573 	movx	a,@dptr
      0009F6 FF               [12] 1574 	mov	r7,a
      0009F7 20 E1 03         [24] 1575 	jb	acc.1,00229$
      0009FA 02 0B 43         [24] 1576 	ljmp	00145$
      0009FD                       1577 00229$:
                                   1578 ;	usb.c:445: if (EP2.fifo_count == 31) //CBW size
      0009FD 90 F2 5A         [24] 1579 	mov	dptr,#(_EP2 + 0x001a)
      000A00 E0               [24] 1580 	movx	a,@dptr
      000A01 FF               [12] 1581 	mov	r7,a
      000A02 BF 1F 02         [24] 1582 	cjne	r7,#0x1F,00230$
      000A05 80 03            [24] 1583 	sjmp	00231$
      000A07                       1584 00230$:
      000A07 02 0B 29         [24] 1585 	ljmp	00140$
      000A0A                       1586 00231$:
                                   1587 ;	usb.c:449: scsi_data_residue = 0;
      000A0A E4               [12] 1588 	clr	a
      000A0B F5 26            [12] 1589 	mov	_scsi_data_residue,a
      000A0D F5 27            [12] 1590 	mov	(_scsi_data_residue + 1),a
      000A0F F5 28            [12] 1591 	mov	(_scsi_data_residue + 2),a
      000A11 F5 29            [12] 1592 	mov	(_scsi_data_residue + 3),a
                                   1593 ;	usb.c:455: a = EP2.fifo;
      000A13 90 F2 5C         [24] 1594 	mov	dptr,#(_EP2 + 0x001c)
      000A16 E0               [24] 1595 	movx	a,@dptr
      000A17 FF               [12] 1596 	mov	r7,a
                                   1597 ;	usb.c:456: b = EP2.fifo;
      000A18 90 F2 5C         [24] 1598 	mov	dptr,#(_EP2 + 0x001c)
      000A1B E0               [24] 1599 	movx	a,@dptr
      000A1C FE               [12] 1600 	mov	r6,a
                                   1601 ;	usb.c:457: c = EP2.fifo;
      000A1D 90 F2 5C         [24] 1602 	mov	dptr,#(_EP2 + 0x001c)
      000A20 E0               [24] 1603 	movx	a,@dptr
      000A21 FD               [12] 1604 	mov	r5,a
                                   1605 ;	usb.c:458: d = EP2.fifo;
      000A22 90 F2 5C         [24] 1606 	mov	dptr,#(_EP2 + 0x001c)
      000A25 E0               [24] 1607 	movx	a,@dptr
      000A26 FC               [12] 1608 	mov	r4,a
                                   1609 ;	usb.c:459: if ((a=='U') && (b=='S') && (c=='B') && (d=='C'))
      000A27 BF 55 02         [24] 1610 	cjne	r7,#0x55,00232$
      000A2A 80 03            [24] 1611 	sjmp	00233$
      000A2C                       1612 00232$:
      000A2C 02 0B 1F         [24] 1613 	ljmp	00134$
      000A2F                       1614 00233$:
      000A2F BE 53 02         [24] 1615 	cjne	r6,#0x53,00234$
      000A32 80 03            [24] 1616 	sjmp	00235$
      000A34                       1617 00234$:
      000A34 02 0B 1F         [24] 1618 	ljmp	00134$
      000A37                       1619 00235$:
      000A37 BD 42 02         [24] 1620 	cjne	r5,#0x42,00236$
      000A3A 80 03            [24] 1621 	sjmp	00237$
      000A3C                       1622 00236$:
      000A3C 02 0B 1F         [24] 1623 	ljmp	00134$
      000A3F                       1624 00237$:
      000A3F BC 43 02         [24] 1625 	cjne	r4,#0x43,00238$
      000A42 80 03            [24] 1626 	sjmp	00239$
      000A44                       1627 00238$:
      000A44 02 0B 1F         [24] 1628 	ljmp	00134$
      000A47                       1629 00239$:
                                   1630 ;	usb.c:461: scsi_tag[0] = EP2.fifo;
      000A47 90 F2 5C         [24] 1631 	mov	dptr,#(_EP2 + 0x001c)
      000A4A E0               [24] 1632 	movx	a,@dptr
      000A4B FF               [12] 1633 	mov	r7,a
      000A4C 8F 2E            [24] 1634 	mov	_scsi_tag,r7
                                   1635 ;	usb.c:462: scsi_tag[1] = EP2.fifo;
      000A4E 90 F2 5C         [24] 1636 	mov	dptr,#(_EP2 + 0x001c)
      000A51 E0               [24] 1637 	movx	a,@dptr
      000A52 FF               [12] 1638 	mov	r7,a
      000A53 8F 2F            [24] 1639 	mov	(_scsi_tag + 0x0001),r7
                                   1640 ;	usb.c:463: scsi_tag[2] = EP2.fifo;
      000A55 90 F2 5C         [24] 1641 	mov	dptr,#(_EP2 + 0x001c)
      000A58 E0               [24] 1642 	movx	a,@dptr
      000A59 FF               [12] 1643 	mov	r7,a
      000A5A 8F 30            [24] 1644 	mov	(_scsi_tag + 0x0002),r7
                                   1645 ;	usb.c:464: scsi_tag[3] = EP2.fifo;
      000A5C 90 F2 5C         [24] 1646 	mov	dptr,#(_EP2 + 0x001c)
      000A5F E0               [24] 1647 	movx	a,@dptr
      000A60 FF               [12] 1648 	mov	r7,a
      000A61 8F 31            [24] 1649 	mov	(_scsi_tag + 0x0003),r7
                                   1650 ;	usb.c:465: scsi_transfer_size = EP2.fifo;
      000A63 90 F2 5C         [24] 1651 	mov	dptr,#(_EP2 + 0x001c)
      000A66 E0               [24] 1652 	movx	a,@dptr
      000A67 FF               [12] 1653 	mov	r7,a
      000A68 8F 2A            [24] 1654 	mov	_scsi_transfer_size,r7
      000A6A 75 2B 00         [24] 1655 	mov	(_scsi_transfer_size + 1),#0x00
      000A6D 75 2C 00         [24] 1656 	mov	(_scsi_transfer_size + 2),#0x00
      000A70 75 2D 00         [24] 1657 	mov	(_scsi_transfer_size + 3),#0x00
                                   1658 ;	usb.c:466: scsi_transfer_size |= ((DWORD)EP2.fifo)<<8;
      000A73 90 F2 5C         [24] 1659 	mov	dptr,#(_EP2 + 0x001c)
      000A76 E0               [24] 1660 	movx	a,@dptr
      000A77 FF               [12] 1661 	mov	r7,a
      000A78 7E 00            [12] 1662 	mov	r6,#0x00
      000A7A 7D 00            [12] 1663 	mov	r5,#0x00
      000A7C 8D 04            [24] 1664 	mov	ar4,r5
      000A7E 8E 05            [24] 1665 	mov	ar5,r6
      000A80 8F 06            [24] 1666 	mov	ar6,r7
      000A82 E4               [12] 1667 	clr	a
      000A83 42 2A            [12] 1668 	orl	_scsi_transfer_size,a
      000A85 EE               [12] 1669 	mov	a,r6
      000A86 42 2B            [12] 1670 	orl	(_scsi_transfer_size + 1),a
      000A88 ED               [12] 1671 	mov	a,r5
      000A89 42 2C            [12] 1672 	orl	(_scsi_transfer_size + 2),a
      000A8B EC               [12] 1673 	mov	a,r4
      000A8C 42 2D            [12] 1674 	orl	(_scsi_transfer_size + 3),a
                                   1675 ;	usb.c:467: scsi_transfer_size |= ((DWORD)EP2.fifo)<<16;
      000A8E 90 F2 5C         [24] 1676 	mov	dptr,#(_EP2 + 0x001c)
      000A91 E0               [24] 1677 	movx	a,@dptr
      000A92 FF               [12] 1678 	mov	r7,a
      000A93 7E 00            [12] 1679 	mov	r6,#0x00
      000A95 8E 04            [24] 1680 	mov	ar4,r6
      000A97 8F 05            [24] 1681 	mov	ar5,r7
      000A99 E4               [12] 1682 	clr	a
      000A9A FE               [12] 1683 	mov	r6,a
      000A9B 42 2A            [12] 1684 	orl	_scsi_transfer_size,a
      000A9D EE               [12] 1685 	mov	a,r6
      000A9E 42 2B            [12] 1686 	orl	(_scsi_transfer_size + 1),a
      000AA0 ED               [12] 1687 	mov	a,r5
      000AA1 42 2C            [12] 1688 	orl	(_scsi_transfer_size + 2),a
      000AA3 EC               [12] 1689 	mov	a,r4
      000AA4 42 2D            [12] 1690 	orl	(_scsi_transfer_size + 3),a
                                   1691 ;	usb.c:468: scsi_transfer_size |= ((DWORD)EP2.fifo)<<24;
      000AA6 90 F2 5C         [24] 1692 	mov	dptr,#(_EP2 + 0x001c)
      000AA9 E0               [24] 1693 	movx	a,@dptr
      000AAA FC               [12] 1694 	mov	r4,a
      000AAB E4               [12] 1695 	clr	a
      000AAC FF               [12] 1696 	mov	r7,a
      000AAD FE               [12] 1697 	mov	r6,a
      000AAE FD               [12] 1698 	mov	r5,a
      000AAF EF               [12] 1699 	mov	a,r7
      000AB0 42 2A            [12] 1700 	orl	_scsi_transfer_size,a
      000AB2 EE               [12] 1701 	mov	a,r6
      000AB3 42 2B            [12] 1702 	orl	(_scsi_transfer_size + 1),a
      000AB5 ED               [12] 1703 	mov	a,r5
      000AB6 42 2C            [12] 1704 	orl	(_scsi_transfer_size + 2),a
      000AB8 EC               [12] 1705 	mov	a,r4
      000AB9 42 2D            [12] 1706 	orl	(_scsi_transfer_size + 3),a
                                   1707 ;	usb.c:469: scsi_dir_in = EP2.fifo & 0x80;
      000ABB 90 F2 5C         [24] 1708 	mov	dptr,#(_EP2 + 0x001c)
      000ABE E0               [24] 1709 	movx	a,@dptr
      000ABF FF               [12] 1710 	mov	r7,a
      000AC0 74 80            [12] 1711 	mov	a,#0x80
      000AC2 5F               [12] 1712 	anl	a,r7
      000AC3 F5 32            [12] 1713 	mov	_scsi_dir_in,a
                                   1714 ;	usb.c:470: scsi_lun = EP2.fifo;
      000AC5 90 F2 5C         [24] 1715 	mov	dptr,#(_EP2 + 0x001c)
      000AC8 E0               [24] 1716 	movx	a,@dptr
      000AC9 F5 33            [12] 1717 	mov	_scsi_lun,a
                                   1718 ;	usb.c:471: scsi_cdb_size = EP2.fifo;
      000ACB 90 F2 5C         [24] 1719 	mov	dptr,#(_EP2 + 0x001c)
      000ACE E0               [24] 1720 	movx	a,@dptr
      000ACF F5 44            [12] 1721 	mov	_scsi_cdb_size,a
                                   1722 ;	usb.c:472: for(a = 0; a < 16; a++)
      000AD1 7F 00            [12] 1723 	mov	r7,#0x00
      000AD3                       1724 00148$:
                                   1725 ;	usb.c:474: scsi_cdb[a] = EP2.fifo;
      000AD3 EF               [12] 1726 	mov	a,r7
      000AD4 24 34            [12] 1727 	add	a,#_scsi_cdb
      000AD6 F9               [12] 1728 	mov	r1,a
      000AD7 90 F2 5C         [24] 1729 	mov	dptr,#(_EP2 + 0x001c)
      000ADA E0               [24] 1730 	movx	a,@dptr
      000ADB FE               [12] 1731 	mov	r6,a
      000ADC F7               [12] 1732 	mov	@r1,a
                                   1733 ;	usb.c:472: for(a = 0; a < 16; a++)
      000ADD 0F               [12] 1734 	inc	r7
      000ADE BF 10 00         [24] 1735 	cjne	r7,#0x10,00240$
      000AE1                       1736 00240$:
      000AE1 40 F0            [24] 1737 	jc	00148$
                                   1738 ;	usb.c:477: EP2.cs = 0x40;
      000AE3 90 F2 53         [24] 1739 	mov	dptr,#(_EP2 + 0x0013)
      000AE6 74 40            [12] 1740 	mov	a,#0x40
      000AE8 F0               [24] 1741 	movx	@dptr,a
                                   1742 ;	usb.c:478: if (!HandleCDB())
      000AE9 12 0C DE         [24] 1743 	lcall	_HandleCDB
      000AEC E5 82            [12] 1744 	mov	a,dpl
      000AEE 70 27            [24] 1745 	jnz	00132$
                                   1746 ;	usb.c:480: scsi_status = 1;
      000AF0 75 25 01         [24] 1747 	mov	_scsi_status,#0x01
                                   1748 ;	usb.c:481: if (scsi_transfer_size == 0)
      000AF3 E5 2A            [12] 1749 	mov	a,_scsi_transfer_size
      000AF5 45 2B            [12] 1750 	orl	a,(_scsi_transfer_size + 1)
      000AF7 45 2C            [12] 1751 	orl	a,(_scsi_transfer_size + 2)
      000AF9 45 2D            [12] 1752 	orl	a,(_scsi_transfer_size + 3)
      000AFB 70 08            [24] 1753 	jnz	00129$
                                   1754 ;	usb.c:483: EP1.cs = bmSTALL; 
      000AFD 90 F2 13         [24] 1755 	mov	dptr,#(_EP1 + 0x0013)
      000B00 74 02            [12] 1756 	mov	a,#0x02
      000B02 F0               [24] 1757 	movx	@dptr,a
      000B03 80 12            [24] 1758 	sjmp	00132$
      000B05                       1759 00129$:
                                   1760 ;	usb.c:485: else if (scsi_dir_in)
      000B05 E5 32            [12] 1761 	mov	a,_scsi_dir_in
      000B07 60 08            [24] 1762 	jz	00126$
                                   1763 ;	usb.c:487: EP1.cs = bmSTALL;
      000B09 90 F2 13         [24] 1764 	mov	dptr,#(_EP1 + 0x0013)
      000B0C 74 02            [12] 1765 	mov	a,#0x02
      000B0E F0               [24] 1766 	movx	@dptr,a
      000B0F 80 06            [24] 1767 	sjmp	00132$
      000B11                       1768 00126$:
                                   1769 ;	usb.c:491: EP2.cs = bmSTALL;
      000B11 90 F2 53         [24] 1770 	mov	dptr,#(_EP2 + 0x0013)
      000B14 74 02            [12] 1771 	mov	a,#0x02
      000B16 F0               [24] 1772 	movx	@dptr,a
      000B17                       1773 00132$:
                                   1774 ;	usb.c:495: usb_have_csw_ready = 1;
      000B17 90 60 06         [24] 1775 	mov	dptr,#_usb_have_csw_ready
      000B1A 74 01            [12] 1776 	mov	a,#0x01
      000B1C F0               [24] 1777 	movx	@dptr,a
      000B1D 80 12            [24] 1778 	sjmp	00141$
      000B1F                       1779 00134$:
                                   1780 ;	usb.c:499: EP2.cs = 0x40;
                                   1781 ;	usb.c:500: EP2.cs = 4;
      000B1F 90 F2 53         [24] 1782 	mov	dptr,#(_EP2 + 0x0013)
      000B22 74 40            [12] 1783 	mov	a,#0x40
      000B24 F0               [24] 1784 	movx	@dptr,a
      000B25 C4               [12] 1785 	swap	a
      000B26 F0               [24] 1786 	movx	@dptr,a
      000B27 80 08            [24] 1787 	sjmp	00141$
      000B29                       1788 00140$:
                                   1789 ;	usb.c:505: EP2.cs = 0x40;
                                   1790 ;	usb.c:506: EP2.cs = 4;
      000B29 90 F2 53         [24] 1791 	mov	dptr,#(_EP2 + 0x0013)
      000B2C 74 40            [12] 1792 	mov	a,#0x40
      000B2E F0               [24] 1793 	movx	@dptr,a
      000B2F C4               [12] 1794 	swap	a
      000B30 F0               [24] 1795 	movx	@dptr,a
      000B31                       1796 00141$:
                                   1797 ;	usb.c:509: usb_received_data_ready &= ~bmEP2IRQ;
      000B31 90 60 05         [24] 1798 	mov	dptr,#_usb_received_data_ready
      000B34 E0               [24] 1799 	movx	a,@dptr
      000B35 FF               [12] 1800 	mov	r7,a
      000B36 74 FD            [12] 1801 	mov	a,#0xFD
      000B38 5F               [12] 1802 	anl	a,r7
      000B39 F0               [24] 1803 	movx	@dptr,a
                                   1804 ;	usb.c:510: EPIE |= bmEP2IRQ;
      000B3A 90 F0 30         [24] 1805 	mov	dptr,#_EPIE
      000B3D E0               [24] 1806 	movx	a,@dptr
      000B3E FF               [12] 1807 	mov	r7,a
      000B3F 74 02            [12] 1808 	mov	a,#0x02
      000B41 4F               [12] 1809 	orl	a,r7
      000B42 F0               [24] 1810 	movx	@dptr,a
      000B43                       1811 00145$:
                                   1812 ;	usb.c:514: if (usb_have_csw_ready)
      000B43 90 60 06         [24] 1813 	mov	dptr,#_usb_have_csw_ready
      000B46 E0               [24] 1814 	movx	a,@dptr
      000B47 E0               [24] 1815 	movx	a,@dptr
      000B48 60 03            [24] 1816 	jz	00150$
                                   1817 ;	usb.c:516: SendCSW2();
      000B4A 02 05 A9         [24] 1818 	ljmp	_SendCSW2
      000B4D                       1819 00150$:
      000B4D 22               [24] 1820 	ret
                                   1821 	.area CSEG    (CODE)
                                   1822 	.area CONST   (CODE)
                                   1823 	.area XINIT   (CODE)
                                   1824 	.area CABS    (ABS,CODE)
