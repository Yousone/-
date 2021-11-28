# 1.
判断n阶矩阵对角线上的最大元素
/*
1 2 3 4 5
5 6 7 8 9
0 9 8 7 6
3 2 1 4 5
8 5 2 1 3
*/
#include<iostream>
using namespace std;
int main()
{
	int n,i,j,max,x;
	cout<<"请输入矩阵的阶："<<endl;
	cin>>n;
	int a[10][10];
	cout<<"请输入一个矩阵，每个数之间用空格间隔，每行输入完成后按回车："<<endl;
	for(i=0;i<n;i++)
	{
		for(j=0;j<n;j++)
			cin>>a[i][j];
	}
	max = a[0][0];
	for(i=1;i<5;i++)
		if(a[i][i]>max)
		{
			max = a[i][i];
			x = i;
		}
	cout<<"对角线上最大的数为："<<max<<"，行号为："<<x+1<<endl;
	system("Pause");
}
