给定一个字符串，找到它的第一个不重复的字符，并返回它的索引。如果不存在，则返回 -1。

案例:

s = "leetcode"
返回 0.

s = "loveleetcode",
返回 2.

int firstUniqChar(char * s){
    int count[26]={0};
    int l;
    l=strlen(s);
    for(int i=0;i<l;i++)
    {
        count[s[i]-'a']++;
    }
    for(int i=0;i<l;i++)
    {
        if(count[s[i]-'a']==1)
        {
            return i;
        }
    }
    return -1;
}
