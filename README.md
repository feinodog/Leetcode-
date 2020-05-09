# Leetcode刷题
https://github.com/luliyucoordinate/Leetcode
这个人太吊了。。
2020年5月5日12:58:05
贪心算法
题目：455
思路：比较简单 qsort后 贪心获取糖果
题目:435
思路：排序 要么留包含的小的 要么留短的
题目：1326
有点难 但是实际上就是跳跃II
但是要需改，跳跃II是一定会跳到。这个不一定，所以要剪枝判断。
题目：1024

题目：910
有可能就是排序后的端点差 有可能是某个点 采用前面一段+k 后-k 
贪心  推导有点难。。。  划分法

题目：664
https://www.bilibili.com/video/BV12x411E7Rz?from=search&seid=8611268802613329580
dp算法
j是用距离来遍历 从1开始 0距离全是1

题目：98 排序二叉树
INT_MAX LONG_MAX


1405 1007 98 664 1278

字符串练习：
int memcmp(const void *str1, const void *str2, size_t n)
void *memcpy(void *dest, const void *src, size_t n)

errno_t memcpy_s(

   void* dest,

   size_t destMax,

   const void* src,

   size_t count 

)
 


void *memset(void *str, int c, size_t n)

errno_t memset_s(

void* dest, 

size_t destMax, 

int c, 

size_t count

)


_s errno_t
EOK = 0
char *strcat(char *dest, const char *src)
errno_t strcat_s(

   char* strDest,

   size_t destMax,

   const char* strSrc

)
 errno_t strncat_s(

char* strDest, 

size_t destMax, 

const char* strSrc, 

size_t count

)
 
errno_t strncat_s(

char* strDest, 

size_t destMax, 

const char* strSrc, 

size_t count

)
char *strcpy(char *dest, const char *src)

char *strtok_s(char *strToken, const char *strDelimit, char **context); 
strtok_s函数将剩余的字符串存储在contextStr变量中，而不是函数内部的静态变量中，从而保证了多线程访问的安全性。
int main () {
   char str[80] = "This is - a - website";
   const char s[2] = "-";

      char *contextStr = NULL;
