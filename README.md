~~~
 Ex-3 GENERATION OF LEXICAL TOKENS USING C
  AIM
 To write a C program to implement lexical analyzer to recognize a few patterns.
ALGORITHM
1)	Start the program.
2)	Get the input from the user with the terminating symbol ‘;’.
3)	Until the symbol is ‘;’, do the following
4)	If the next character of the symbol is an operator then print it as an operator.
5)	Stop the program.
 PROGRAM

#include<stdio.h>
#include<ctype.h>
#include<stdlib.h>
#include<string.h>
#define PAREN_CLOSE 297
char lexemes[MAX];
char buffer[SIZE];
int lastchar = -1;{
    int token;
} symtable[100];

struct entry keywords[] = {
    {"if", KEYWORD},
    {"else", KEYWORD},
    {"for", KEYWORD},
    {"int", KEYWORD},
    {"float", KEYWORD},
    {0, 0}
};
}
int insert(char s[], int tok) {
    if (lastentry + 1 >= MAX)
        errormsg("symtable is full");
    if (lastentry + len + 1 >= MAX)
        errormsg("lexemes array is full");
return lastentry;
}
void initialise() {
    struct entry *ptr;
    for (ptr = keywords; ptr->token; ptr++)
        insert(ptr->lexptr, ptr->token);
}
int lexer() {
    int t;
    int val, i = 0;
     else if (isalpha(t)) {
            buffer[i] = EOS;
            if (t != EOF)
                ungetc(t, stdin);
            val = lookup(buffer);
            if (val == 0)
                val = insert(buffer, ID);
            tokenval = val;
            return symtable[val].token;
        } else if (t == EOF)
            return DONE;
        else {
            tokenval = NONE;
            return t;
        }
int main() {
  while (lookahead != DONE) {
        if (lookahead == NUM) {
            printf("\n Number :%d", tokenval);
    }
    return 0;
}
~~~
# OUTPUT
![image](https://github.com/niranjanadevi-s/Ex-3-GENERATION-OF-LEXICAL-TOKENS-/assets/141748873/015a3fea-259f-4994-abdf-020b3347cd5d)

# RESULT
 The program to implement lexical analyzer is executed and the output is verified.
