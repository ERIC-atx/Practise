给定一个整数数组 nums ，找到一个具有最大和的连续子数组（子数组最少包含一个元素），返回其最大和。

示例:

输入: [-2,1,-3,4,-1,2,1,-5,4],
输出: 6
解释: 连续子数组 [4,-1,2,1] 的和最大，为 6。

int maxSubArray(int* nums, int numsSize){
    int max=0;
    int a[numsSize];
    a[0]=nums[0];
    for(int i=1;i<numsSize;i++)
    {
        if(nums[i]>nums[i]+a[i-1])
        a[i]=nums[i];
        else 
        a[i]=nums[i]+a[i-1];
    }
    max=a[0];
    for(int i=1;i<numsSize;i++)
    {
        if(a[i]>max)
        max=a[i];
    }
    return max;
}
