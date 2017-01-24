# stacks
#include<stdio.h>
#define max 10
void main()
{
    int s[max],top=-1,ch;
    for(;;)
    {
    printf("1.push\n");
    printf("2.pop\n");
    printf("3.peep\n");
    printf("4.do nothing\n");
    scanf("%d",&ch);
    switch(ch)
    {
        case 1:push(s,&top);break;
        case 2:pop(s,&top);break;
        case 3:peep(s,&top);break;
        case 4:printf("end");exit(0);break;
        default :printf("wrong choice\n");
    }
}
}
int push(int a[],int *p)
{
    if(*p==max-1)
    {
        printf("stack overflow\n");
        return;
    }
    ++*p;
    printf("enter top element\n");
    scanf("%d",&a[*p]);
    return;
}
int pop(int a[],int *p)
{
    if(*p==-1)
    {
        printf("stack underflow\n");
        return;
    }

    printf(" element removed %d\n",a[*p]);
    --*p;
    return;
}
int peep(int a[],int *p)
{
    if(*p==-1)
    {
        printf("stack underflow\n");
        return;
    }

    printf(" top element %d\n",a[*p]);

    return;
}
