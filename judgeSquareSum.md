给定一个非负整数 c ，你要判断是否存在两个整数 a 和 b，使得 a2 + b2 = c。

示例1:

输入: 5
输出: True
解释: 1 * 1 + 2 * 2 = 5


 

示例2:

输入: 3
输出: False

bool judgeSquareSum(int c){
    int a,mark=0,b=0;
    for(a=0;a<=sqrt(c);a++)
    {
        b=sqrt(c-a*a);
        if(b*b+a*a==c)
        {
            mark=1;
            break;
        }
    }
    if(mark==1)
    return true;
    else 
    return false;
}
