# qiguaibisai
#include<iostream>
#include<iomanip>
using namespace std;
int f[11];
void answer(int k,int score)
{
	if(k>10||score<=0)
	{
		if(score==100)
		{
			for(int i=1;i<=10;i++)
			{
				cout<<f[i];
			} 
			cout<<endl;
			 
		}
		return;
		
	}
	for(int i=1;i>=0;i--)
	{
		f[k] = i;
		if(i==0)
		answer(k+1,score-k);
		else if(i==1)
		answer(k+1,score*2);
	}
	return;
}
int main()
{
	int score = 10;
	int k = 1;
	
	answer(k,score);
	return 0;
} 

