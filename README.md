/******************************************************************************

                            Online C Compiler.
                Code, Compile, Run and Debug C program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <stdio.h>

int main()
{
    double b,c,d;
    char a;
    START:
    printf("\n입력:");
    scanf("%lf%c%lf",&b,&a,&c);
    
    if(a=='/')
    {
        goto CAL;
        RETURN:
        printf("\n\n(소수점50자리)");
    }
    CAL:
    switch (a)
    {
        case '+':
        printf("%.0lf",b+c);
        break;
        case '-':
        printf("%.0lf",b-c);
        break;
        case '/':
        printf("%.50lf\n",b/c);
        break;
        case '*':
        printf("%.0lf",b*c);
        break;
    }
    if(a != '+' && a != '/' && a != '*' && a != '-')
    {
        printf("'+' '-' '*' '/' 중에 선택");
        goto START;
    }
    else
    {
        goto END;
    }
    END:
    if(a=='/')
    {
        goto RETURN;
    }
    
    RE:
    return 0;
}
