<div align="center">

## Combination Program


</div>

### Description

This program takes a string and value of r as input and generates all the combinations which is equal to ncr
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Akash Khaitan](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/akash-khaitan.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |C
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__3-26.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/akash-khaitan-combination-program__3-13210/archive/master.zip)





### Source Code

```
#include<stdio.h>
#include<string.h>
int r=0,q=0;
char as[50],bs[50];
int main(void)
{
    void combination(int,int,int);
    int nk=0;
    printf("Enter a String : ");
    gets(as);
    printf("Enter the value of r : ");
    scanf("%d",&r);
    nk=strlen(as)-r;
    combination(0,nk,0);
    printf("No of Combinations : %d\n",q);
    return 0;
}
void combination(int i,int nk,int x)
{
    for(i;i<=nk;i++)
    {
        bs[x]=as[i];
        if(nk==strlen(as)-1)
        {
            bs[x]=as[i];
            puts(bs);
            q++;
        }
        if(nk<strlen(as)-1)
        {
            combination(i+1,nk+1,x+1);
        }
    }
}
```

