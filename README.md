# C-p46-5-
C语言学习笔记 p46 作业讲解(5)
#include<stdio.h>
#include<string.h>
#include<assert.h>
int main()
{
    int a[5]={5,4,3,2,1};
    int* ptr=(int*)(&a+1);
    printf("%d,%d",*(a+1),*(ptr-1));
    return 0;
}//输出4，1

int main()
{
    int aa[2][5]={10,9,8,7,6,5,4,3,2,1};
    int* ptr1=(int*)(&aa+1);
    int* ptr2=(int*)(*(aa+1));
    printf("%d%d",*(ptr1-1),*(ptr2-1));
    return 0;
}//输出为1，6


//暴力求解法
void left_move(char* arr[],int k)
{
    assert(arr!=NULL);
  int i=0;
  int len=strlen(arr);
  for(i=0;i<l;i++)
  {
      //左旋转一个字符
      char tmp=*arr
      int j=0;
      for(j=0;j<len-1;j++)
      {
          *(arr+j)=*(arr+j+1);
      }
      *(arr+len-1)=tmp;
  }
}
int main()
{
    //旋转字符串
    char arr[]="abcdef";
    left_move(arr,2);
    printf("%s\n",arr);
    return 0;
}

//三步翻转法
void reverse(char* left,char* right)
{
    assert(left!=NULL);
    assert(right!=NULL);
    while(left<right)
    {
        char tmp=*left;
        *left=*right;
        *right=tmp;
        left++;
        right--;
    }
}
void left_move(char*arr,int k)
{
    assert(arr);
    int len=strlen(arr);
    assert(k<=len);
    reverse(arr,arr+k-1);//逆序左边
    reverse(arr+k,arr+len-1);//逆序右边
    reverse(arr,arr+len-1);//逆序整体
}
int main()
{
    //旋转字符串
    char arr[]="abcdef";
    left_move(arr,2);
    printf("%s\n",arr);
    return 0;
}


int is_lefgt_move(char* s1,char* s2)
{
    int len=strlen(s1);
    int i=0;
    for(i=0;i<len;i++)
    {
        left_move(s1,1);
        strcmp(s1,s2);
        if(ret==0)
            return 1;
    }
    return 0;
}
int main()
{
    char* arr1[]="abcdef";
    char* arr2[]="cdefab";
    int ret=is_left_move(arr1,arr2);
    if(ret==1)
        printf("Yes\n");
    else
        printf("No\n");
    return 0;
}


