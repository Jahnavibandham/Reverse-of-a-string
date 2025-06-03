# Reverse-of-a-string

#include <stdio.h>
#include<string.h>
#define max 1000
void reversestring(char *s)
{
    char stack[max];
    int top=-1;
    //push
    for(int i=0;s[i]!='\0';i++)
    {
        stack[++top]=s[i];
    }

    //pop
    for(int i=0;s[i]!='\0';i++)
    {
        s[i]=stack[top--];
    }
}

int main()
{
   
    char str[max];
    printf("enter the string");
    scanf("%s",str);
    reversestring(str);
    printf("reverse string:%s\n",str);
   
    return 0;
}
