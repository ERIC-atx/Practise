统计所有小于非负整数 n 的质数的数量。

示例:

输入: 10
输出: 4
解释: 小于 10 的质数一共有 4 个, 它们是 2, 3, 5, 7 。

int countPrimes(int n){
    int wnum=0,num=0;
    for(int i=2;i<n;i++)
    {
       int sign=1;
        for(int j=2;j<i;j++)
        {
            if(i%j==0)
            {
                wnum++;
                sign=0;
                break;
            }
        }
        if(sign==1)
        num++;
    }
    return num;
}
