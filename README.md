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
public int[] sort(int[] sourceArray) throws Exception {
// 对 arr 进行拷贝，不改变参数内容
int[] arr = Arrays.copyOf(sourceArray, sourceArray.length);
int len = arr.length;
buildMaxHeap(arr, len);
for (int i = len - 1; i > 0; i--) {
swap(arr, 0, i);
len--;
heapify(arr, 0, len);
}
return arr;


# 5月底冲刺计划

大纲：
参考index.pdf在welink上 潘东的聊天记录
参考小象学院的ppt
重点：
1.手撕qsort 记忆2种方法
a.常规
Done
b.荷兰旗优化方案
三色旗后 lt为边界+1 gt为右边界-1
Done
2.手撕插入排序
Done
题目：147

3.归并排序
数组参考：
https://www.cnblogs.com/yangmenda/p/11726968.html
需要一个临时数组变量做参数指针
链表参考
https://blog.csdn.net/Doutd_y/article/details/81544606


题目：88 148 23

4.栈
a.数组栈、链表栈
题目:155
https://blog.csdn.net/qq_39769369/article/details/83614758

题目:20


队列 621
堆 215
763双指针
3划窗
130




# To display the perf.data header info, please use --header/--header-only options.
#
#
# Total Lost Samples: 0
#
# Samples: 19K of event 'r11'
# Event count (approx.): 20898998011
#
# Children      Self  Command  Shared Object     Symbol                                                      
# ........  ........  .......  ................  ............................................................
#
    99.02%     0.23%  sre_bin  perf-4125.map     [.] Job_Recv                                                
            |
            ---Job_Recv
               |          
               |--98.75%-- L2INF_HAL_RecvJobProcess
               |          |          
               |          |--98.23%-- L2INF_HAL_L2JobProcess
               |          |          |          
               |          |          |--98.08%-- L2INF_HAL_ProcJobFromSlaveCore
               |          |          |          |          
               |          |          |          |--45.93%-- DLSCH_CcSchedulerJobProc
               |          |          |          |          |          
               |          |          |          |          |--45.90%-- DLSCH_CcScheduler
               |          |          |          |          |          |          
               |          |          |          |          |          |--42.95%-- 0xc3f7b4
               |          |          |          |          |          |          |          
               |          |          |          |          |          |          |--34.21%-- DLSCH_UsrGrpPostProc
               |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |--33.97%-- DLSCH_TrpSchedulerLf
               |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |--33.60%-- DLSCH_DataSchLf
               |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |--16.85%-- DLSCH_SuUserSch
               |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |--8.38%-- DLSCH_SuUserSchFromDrbBearGroupPdcch
               |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |--8.23%-- DLSCH_SuUserAllocPdcch
               |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |--7.25%-- DLSCH_SuUserApply4Pdcch
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |--7.20%-- DLSCH_PdcchResAlloc
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--6.65%-- PDCCHSCH_AllocResForTrp
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--4.96%-- PDCCHSCH_ResAllocProc
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--2.60%-- PDCCHSCH_UserResAlloc
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--1.19%-- PDCCHSCH_PrepareResAllocInfo
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.26%-- 0xd1c13c
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.10%-- SUSRPDCCH_GetYk
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |           --0.01%-- SUSRPDCCH_GetUsrInfo
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.22%-- PDCCHSCH_UpdateUserSearchInfo
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.14%-- PDCCHSCH_CalcUserPower
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.01%-- 0xd170cc
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |           --0.01%-- L2INF_MathDb2Liner
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.04%-- PDCCHSCH_UpdateUeSpecificCoresetSearchInfo
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.02%-- PDCCHSCH_UpdateUserSearchCce
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |           --0.01%-- 0xd170a0
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.18%-- 0xd1d140
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.15%-- 0xd1d064
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          
               |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |          |--0.10%-- SUSRPDCCH_GetUsrDlCtrlInfo
字符串 bfs dfs  手机上
https://www.jianshu.com/p/14944a7d273e
划窗 hash
209   1100  两个数组的交集 II  1004   532  1208   560   219  两数之和 III - 数据结构设计   974  355 1 3
队列 栈 差分 链表 排序
346   933   622 353   621  844 用两个栈实现队列   739   503  1124  560   974   1109   234   203   面试题 02.05. 链表求和  19 147  1051  324
210
单位雨水
回溯   二分 归并
401  I. 斐波那契数列  93  526  294  320  270  53  270 875  973  426  215
01矩阵

1086  751  547   557 
三个数组，找到里面均存在的元素

一个乱序的数组，从左边或者右边插入排序，需要的步数

设计一个后台数据库，记录一个航班 经济、商务、豪华 三个仓位，分别在 旺季 和 淡季 的 基本成本 和 浮动成本。并可以查询。

557
根据二维数组组成二叉树，二维数组nums[i][0]为子节点的数值val，nums[i][1]为父节点的数值val。如果nums[i][1]的数值为-1，说明nums[i][0]为根节点。排放的时候优先排放树的左节点，右节点可能为空。返回树的根节点，输出会是按层次遍历的树节点的值。
比如：
输入[[1,3],[2,3],[3,-1],[4,1],[5,2]]
输出会是[3,1,2,4,null,5]

删除数组中两个位置的值，将一个数组A分成三段，如果存在两个点能将数组三等分（即分割成和相等的三段），返回这两个点索引升序排序的数组，否则返回空数组。5<=A.length<=10^5
比如：
输入[1,2,1,3,1]   返回[1,3]。（去掉index=1的值2和index=3的值3，剩下的三段和一致）
输入[1,1,1,1,1,1]   返回[]。

105
 （1）由于噪声是以一个点为起始点逐渐向外扩展递减的，首先想到的就是递归的思路，处理完一个点，然后递归处理其周围的8个点

（2）递归的退出条件：到达边界 || 矩阵中原有的值 >= 新来的值

（3）遍历方向比较简单的方法：将8个方向写成-1,0,1的变量数组，循环遍历

注意：对功能函数进行相应的抽取，不要都堆在主逻辑中

代码如下：
ublic class Case1 {
02
    // 方向数组
03
    private int[][] list = {{-1, -1}, {-1, 0}, {-1, 1}, {0, -1}, {0, 1}, {1, -1}, {1, 0}, {1, 1}};
04
 
05
    private int rowNo;
06
 
07
    private int columnNo;
08
 
09
    public int spreadNoise(int n, int m, int[][] noise) {
10
        rowNo = n;
11
        columnNo = m;
12
        int[][] matrix = new int[n][m];
13
        for (int[] tempData : noise) {
14
            fillMatrix(matrix, tempData);
15
        }
16
        return calculateResult(matrix);
17
    }
18
 
19
    // 填充矩阵，递归调用
20
    private void fillMatrix(int[][] matrix, int[] tempData) {
21
        int x = tempData[0];
22
        int y = tempData[1];
23
        int value = tempData[2];
24
        // 退出条件：越界 || 原来的值 >= 新的值
25
        if (isOutOfBoard(x, y) || matrix[x][y] >= value) {
26
            return;
27
        }
28
 
29
        matrix[x][y] = value;
30
        // 八个方向依次递归调用填充方法
31
        for (int[] tempList : list) {
32
            int newX = x + tempList[0];
33
            int newY = y + tempList[1];
34
            int[] newData = {newX, newY, value - 1};
35
            fillMatrix(matrix, newData);
36
        }
37
    }
38
 
39
    // 越界判断
40
    private boolean isOutOfBoard(int x, int y) {
41
        return x < 0 || x >= rowNo || y < 0 || y >= columnNo;
42
    }
43
 
44
    // 计算最终结果
45
    private int calculateResult(int[][] array) {
46
        int result = 0;
47
        for (int[] ints : array) {
48
            for (int j = 0; j < array[0].length; j++) {
49
                result = result + ints[j];
50
            }
51
        }
52
        return result;
53
    }
54
}
有visit dfs 记忆化搜索
518  494  1201  1011  939  963  105  357 10
https://www.cnblogs.com/gongpixin/p/6761389.html  二分搜和变形
