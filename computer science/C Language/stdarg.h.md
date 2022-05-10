# stdarg.h
C 함수가 가변 길이 인자를 사용하기 위해서 필요한 매크로와 자료형을 포함한다. 대표적으로 `printf`에서 사용한다.

**EXAMPLE**
``` C
void foo(char *fmt, ...)
{
   va_list ap;
   int d;
   char c, *p, *
   va_start(ap, fmt);
   while (*fmt)
           switch(*fmt++) {
           case 's':                       /* string */
                   s = va_arg(ap, char *);
                   printf("string %s\n", s);
                   break;
           case 'd':                       /* int */
                   d = va_arg(ap, int);
                   printf("int %d\n", d);
                   break;
           case 'c':                       /* char */
                   c = va_arg(ap, char);
                   printf("char %c\n", c);
                   break;
           }
   va_end(ap);
}
```

**SYNOPSIS**
``` C
#include <stdarg.h>

void
va_start(va_list ap, last);

type
va_arg(va_list ap, type);

void
va_end(va_list ap);
```

**va_list**는 va_arg, va_start와 va_end가 사용하는 객체이다. 
**va_start()** 는 *ap(argument pointer)* 가  va_arg나 va_end가 사용할 수 있도록 한다. *last*인자는 가변인자가 등장하기 전 마지막 인자를 넣어준다. *last* 인자는 register variable이나 함수, 배열이면 ***안된다***.
**va_arg()** 는 *ap*에서 값을 반환하고 *ap*를 증가시켜 다음 인자를 가르키게 합니다. 이때 반환디고 증가되는 값은 *type*에 따라 결정됩니다.
%*type*이 *int* 보다 작을 경우(ex char, short) int형(또는 unsigned int)으로 자동으로 변환되고 warning이 뜬다. 컴파일러에 의존적인 작동??
**va_end()** 는 va_start로 초기화한 가변 인자 리스트를 반환합니다. 함수가 반환되기 전에 va_start로 초기화한 모든 가변인자리스트는 반환되어야 합니다.

##### Links
[[가변인자]]
##### Tags
#va_start #va_end #va_arg #va_list #가변길이인자 #stdarg #가변함수 #cstdarg