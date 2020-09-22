<div align="center">

## A programm that displays its source


</div>

### Description

A programm that displays its source. Compile, run executiable, and it will show the source code from wich it has been compiled. Just for fun...Useless, i guess ;)
 
### More Info
 
source code of itself


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\.rad](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/rad.md)
**Level**          |Beginner
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Algorithms](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithms__3-29.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/rad-a-programm-that-displays-its-source__3-8782/archive/master.zip)

### API Declarations

stdio.h


### Source Code

```
#include <stdio.h>
char szMyCode[] =
"void printf_strconst( char* str )\n"
"{\n"
"	do\n"
"	{\n"
"		switch( *str )\n"
"		{\n"
"		case \'\\n\':\n"
"			printf(\"\\\\n\\\"\");\n"
"			if( *(str+1) )\n"
"				printf(\"\\\"\");\n"
"			break;\n"
"		case \'\\\"\':\n"
"			printf(\"\\\"\");\n"
"			break;\n"
"		case \'\\\'\':\n"
"			printf(\"\\\'\");\n"
"			break;\n"
"		case \'\\\\\':\n"
"			printf(\"\\\\\\\\\");\n"
"			break;\n"
"		case \'%\':\n"
"			printf(\"%%\");\n"
"			str++;\n"
"			break;\n"
"		default:\n"
"			printf( \"%c\", *str );\n"
"		}\n"
"	}\n"
"	while( *++str );\n"
"	printf( \";\\n\\n\" );\n"
"}\n"
"\n"
"void main()\n"
"{\n"
"	printf( \"#include <stdio.h>\\n\\nchar szMyCode[] =\\n\\\"\" );\n"
"	printf_strconst( szMyCode );\n"
"	printf( \"%s\",szMyCode );\n"
"	printf( \"-=== THIS IS MY SOURCE! Press any key ===-\");\n"
"	getchar();\n"
"}\n";
void printf_strconst( char* str )
{
	do
	{
		switch( *str )
		{
		case '\n':
			printf("\\n\"");
			if( *(str+1) )
				printf("\n\"");
			break;
		case '\"':
			printf("\\\"");
			break;
		case '\'':
			printf("\\\'");
			break;
		case '\\':
			printf("\\\\");
			break;
		case '%':
			printf("%%");
			break;
		default:
			printf( "%c", *str );
		}
	}
	while( *++str );
	printf( ";\n\n" );
}
void main()
{
	printf( "#include <stdio.h>\n\nchar szMyCode[] =\n\"" );
	printf_strconst( szMyCode );
	printf( "%s",szMyCode );
	printf( "-=== THIS IS MY SOURCE! Press any key ===-");
	getchar();
}
```

