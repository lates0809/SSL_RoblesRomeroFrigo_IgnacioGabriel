LINEAS_I=821

R: El número de líneas es mucho mayor porque el preprocesador incluye el contenido de las librerías como stdio.h, agregando muchas líneas al archivo.

COMENTARIOS_EN_I=NO

R: Porque el preprocesador elimina los comentarios antes de la compilación.

R: 790:    printf("CUADRADO(%d)      = %d\n", 5, ((5) * (5)));

CUADRADO_EN_I=NO

R: 781:    printf("=== Laboratorio de Compilacion en C (v%s) ===\n\n", "1.0");

NOMBRE_MACRO_VERSION=VERSION

R:
(sin salida)

printf("[DEBUG] %s\n", ("Iniciando main"));

DEBUG_ACTIVA_CODIGO=SI

R: 
6:# 1 "c:\\mingw\\include\\stdio.h" 1 3
7:# 38 "c:\\mingw\\include\\stdio.h" 3
9:# 39 "c:\\mingw\\include\\stdio.h" 3
10:# 56 "c:\\mingw\\include\\stdio.h" 3
38:# 57 "c:\\mingw\\include\\stdio.h" 2 3

R: Estas líneas indican el número de línea y el archivo de origen del código. En este caso, muestran que el contenido proviene de stdio.h, donde está definida la función printf.

R:
.ascii "area_circulo(%.1f) = %.4f\12\0"
call    _area_circulo
.def    _area_circulo;  .scl    2;      .type   32;     .endef

AREA_EN_S=LLAMADA

R:
_sumar:
LFB14:
    .cfi_startproc
    pushl   %ebp

R: Estas instrucciones inicializan la función, guardan el estado previo y preparan la pila para ejecutar la suma de los parámetros.

R:
.globl  _llamadas
_llamadas:
    movl    _llamadas, %eax
    movl    %eax, _llamadas
    movl    _llamadas, %eax

LLAMADAS_EN_S=SI

R:
00000000 b .bss
00000000 d .data
00000000 r .eh_frame
00000000 r .rdata
00000000 r .rdata$zzz
00000000 t .text
         U ___main
         U _area_circulo
         U _factorial
00000132 T _imprimir_separador
00000000 B _llamadas
0000001a T _main
         U _printf
         U _puts
00000000 T _sumar

TIPO_AREA_EN_O=U

R: Porque en programa.o la función area_circulo está declarada pero no definida, mientras que en matematica.o sí está definida.

ETAPA_QUE_RESUELVE=ENLAZADO

R: bash: ./programa.o: cannot execute binary file: Exec format error

EJECUTABLE_O=NO