# stdarg.h
C 함수가 가변 길이 인자를 사용하기 위해서 사용하기 위해 필요한 매크로와 자료형을 포함한다. 대표적으로 `printf`에서 사용한다.

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
```
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
**va_arg()** 는 #TODO
**va_end()** 는 va_start로 초기화한 가변 인자 리스트를 반환합니다. 함수가 반환되기 전에 va_start로 초기화한 모든 가변인자리스트는 반환되어야 합니다.



##### Links
[[가변인자]]
##### Tags
#va_start #va_end #va_arg #va_list #가변길이인자 #stdarg #가변함수 #cstdarg