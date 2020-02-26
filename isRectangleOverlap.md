矩形以列表 [x1, y1, x2, y2] 的形式表示，其中 (x1, y1) 为左下角的坐标，(x2, y2) 是右上角的坐标。

如果相交的面积为正，则称两矩形重叠。需要明确的是，只在角或边接触的两个矩形不构成重叠。

给出两个矩形，判断它们是否重叠并返回结果。

示例 1：

输入：rec1 = [0,0,2,2], rec2 = [1,1,3,3]
输出：true


示例 2：

输入：rec1 = [0,0,1,1], rec2 = [1,0,2,1]
输出：false


说明：


	两个矩形 rec1 和 rec2 都以含有四个整数的列表的形式给出。
	矩形中的所有坐标都处于 -10^9 和 10^9 之间。

bool isRectangleOverlap(int* rec1, int rec1Size, int* rec2, int rec2Size){
    int mark1,mark2,mark3,mark4;
    mark1 = rec2[0] - rec1[2];
    mark2 = rec2[2] - rec1[0];
    mark3 = rec2[1] - rec1[3];
    mark4 = rec2[3] - rec1[1];
    if(mark1 == 0 || mark2 == 0 || mark3 == 0 || mark4==0)
    return false;
    else
    {
        if(mark1>0)
        mark1=1;
        else mark1=-1;
        if(mark2>0)
        mark2=1;
        else mark2=-1;
        if(mark3>0)
        mark3=1;
        else mark3=-1;
        if(mark4>0)
        mark4=1;
        else mark4=-1;
    }
     return (mark1*mark2<0 && mark3*mark4 < 0 );
}
