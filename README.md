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
      
      
      
      
      public int[] sort(int[] sourceArray) throws Exception {
int[] arr = Arrays.copyOf(sourceArray, sourceArray.length);
return quickSort(arr, 0, arr.length - 1);
}
private int[] quickSort(int[] arr, int left, int right) {
if (left < right) {
int partitionIndex = partition(arr, left, right);
quickSort(arr, left, partitionIndex - 1);
quickSort(arr, partitionIndex + 1, right);
}
return arr;
}
private int partition(int[] arr, int left, int right) {
int pivot = left;
int index = pivot + 1;
for (int i = index; i <= right; i++) {
if (arr[i] < arr[pivot]) {
swap(arr, i, index);
index++;

}
swap(arr, pivot, index - 1);
return index - 1;
}
private void swap(int[] arr, int i, int j) {
int temp = arr[i];
arr[i] = arr[j];
arr[j] = temp;
}


private void quickSort(int[] arr, int left, int right){
if (left < right) {

int lt = left;
int index = left + 1;
int gt = left;
int pivotValue = arr[left];
while (index <= gt) {
if (arr[index] < pivotValue) swap(arr, lt++, index++);
else if (arr[index] > pivotValue) swap(arr, index, gt--);
else index++;
}
quickSort(arr, left, lt - 1);
quickSort(arr, gt + 1, left);
}
}
private void swap(int[] arr, int i, int j) {
int temp = arr[i];
arr[i] = arr[j];
arr[j] = temp;


private void insertSort(int[] arr) {
// 从下标为1的元素开始选择合适的位置插入，因为下标为0的只有一个元素，默认是有序的
for (int i = 1; i < arr.length; i++) {
// 记录要插入的数据
int tmp = arr[i];

int j = i;
while (j > 0 && tmp < arr[j - 1]) {
arr[j] = arr[j - 1];
j--;
}
// 存在比其小的数，插入
if (j != i) {
arr[j] = tmp;
}

