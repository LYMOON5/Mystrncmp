#include<stdio.h>
#include<assert.h>

//限制长度的字符串比较函数
void Mystrncmp(const char *str1,const char *str2,int  count)
{
	assert(str1 && str2);
	while(count && (*str1 == *str2))
	{
		if(str1 == '\0')
		{
			break;
		}
		str1++;
		str2++;
		count--;
	}
	printf("%d\n",*str1-*str2);
}

int main()
{
  //限制长度字符串比较测试用例
	char *arr1 = "abcde";           
	char *arr2 = "abcdef";
	Mystrncmp(arr1,arr2,strlen(arr1));
  
  return 0;
}
