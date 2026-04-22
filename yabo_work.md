# 这是一个帮助鸭脖完成c语言作业的文档

## 首先我们先来看第一题 大小写字母转化

```c
#include<stdio.h>
int main()
{
    char c='b';
    
    //小写转换为大写
    if(c>='a'&&c<='z') //为了增强程序的健壮性 我们增加了这条代码检查c是否是小写字母
    {
        c-=32;
    } 
    printf("%c ",c);

    //计算小写字母的ASCII值
    int ascii=c-0;
    printf("%d",ascii);


    return 0;
}
```

## 第二个问题 判断是否是一个质数

```c
#include<stdio.h>
int main()
{
    int x=51; //要判断的数

    int isPrime;

    if(x==2) isPrime=1;
    else{
        int i=2;
        for(;i<x;i++)
        {
            if(x%i==0) break;
            //如果在2到x-1之间出现一个可以被x整除的数直接break 说明他是和数
        }
        if(i<x) isPrime=0;
        else isPrime=1;
    }

    if(isPrime) printf("这是一个质数");
    else printf("这是一个和数");

    return 0;
}
```

### 剩下的求阶乘和求平均数的代码请你动手自己实现吧