#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>

using namespace std;
#define INT_MAX 99999

typedef long long int LL;


void FloydWarshall(int **dist, int N)
{


	
	for(int k = 0; k < N; k++)
	{
		for(int i = 0; i < N; i++)
		{
			for(int j = 0; j < N; j++)
			{
				if(dist[k][j] != INT_MAX && dist[i][k] != INT_MAX && dist[i][j] > dist[i][k] + dist[k][j])
				{	dist[i][j] = dist[i][k] + dist[k][j]; }
			}
		}
	}



	
}



/* Driver program to test above functions*/
int main()
{

		int N;
        LL M;
		cin>>N>>M;
	
		int **Graph = new int*[N];
		for(int i = 0; i < N ; i++)
		{
			Graph[i] = new int[N];
		}

		for(int i = 0; i < N ; i++)
		{
			for(int j = 0; j < N; j++)
			{
				Graph[i][j] = 0;
			}
		}
		
		for(LL i = 0; i < M ; i++)
		{
			int s,d,w;
			cin>>s>>d>>w;

			Graph[s-1][d-1] = w;

		}





		int **dist = new int*[N];
		for(int i = 0; i < N; i++)
		{
			dist[i] = new int[N];
		}
		
		for(int i = 0; i < N; i++)
		{
			for(int j = 0; j < N; j++)
			{
                if(i == j)
                    dist[i][j] = 0;
				else if(!Graph[i][j])
					dist[i][j] = INT_MAX;
				else
					dist[i][j] = Graph[i][j];
			}
		}




		FloydWarshall(dist, N);

		int Q;
		cin>>Q;

		for(int i = 0; i < Q; i++)
		{
			int src, dest;
			cin>>src>>dest;

			if(dist[src-1][dest-1] != INT_MAX)
				cout<<dist[src-1][dest-1]<<endl;
			else
				cout<<"-1"<<endl; 
		}
		
	
  return 0;
}
