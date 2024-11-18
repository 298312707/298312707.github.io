#	一、滑动窗口

##	1.定长滑动窗口

分三步：	

​		①处理滑入窗口元素

​		②更新答案（一般是最值）

​		③移出元素（同时更新统计量）

eg：

```java
class Solution {
    public int maxVowels(String s, int k) {
        char[] str=s.toCharArray();
        int cnt=0;
        int ans=0;
        for(int i=0;i<str.length;i++){
            if(str[i]=='a' ||str[i]=='e' ||str[i]=='i' ||str[i]=='o' ||str[i]=='u'){
                cnt++;
            }//①处理滑入窗口元素
            if(i<k-1){
                continue;
            }//不足区间长度，继续滑动
            ans=Math.max(cnt,ans);//②更新答案（一般是最值）
            int out=str[i-k+1];
            if(out=='a' ||out=='e' ||out=='i' ||out=='o' ||out=='u'){
                cnt--;
            }//③移出元素（同时更新统计量）
        }
        return ans;
    }
}
```



##	2.不定长滑动窗口

分三步：

​		①移动左边界(确保滑入元素符合条件)

​		②更新滑入元素相关统计量（一般是数量+1...）

​		③更新答案（一般是区间长度right-left+1）

eg：

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        char[] str=s.toCharArray();
        int ans=0;

        int left=0;
        boolean[] ch=new boolean[128];
        for(int right=0;right<str.length;right++){
            int c=str[right];

            while(ch[c]){
                ch[str[left++]]=false;
            }//①移动左边界(确保滑入元素符合条件)
            ch[c]=true;//②更新滑入元素相关统计量（一般是数量+1...）
            ans=Math.max(ans,right-left+1);//③更新答案（一般是区间长度right-left+1）
        }
        return ans;
    }
}
```

