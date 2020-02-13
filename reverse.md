给出一个 32 位的有符号整数，你需要将这个整数中每位上的数字进行反转。

示例 1:

输入: 123
输出: 321


 示例 2:

输入: -123
输出: -321


示例 3:

输入: 120
输出: 21

int reverse(int x){
    int max=2147483647,min=-2147483648;
    long result=0;
    while(x!=0)
    {
        result=result*10+x%10;
        x=x/10;
    }
    return (result>max || result<min) ? 0:result;
}
