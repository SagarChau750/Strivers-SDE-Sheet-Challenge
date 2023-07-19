#include <bits/stdc++.h>
using namespace std;
int maxProfit(vector<int> &values, vector<int> &weights, int n, int w)
{
	vector<int> prev(w+1,0);
	//Base Condition
	for(int i=weights[0]; i<=w; i++){
		prev[i] = values[0];
	}
	for(int ind =1; ind<n; ind++){
		for(int cap=w; cap>=0; cap--){
			int notTaken = 0 + prev[cap];
			int taken = INT_MIN;
			if(weights[ind] <= cap)
				taken = values[ind] + prev[cap - weights[ind]];
			prev[cap] = max(notTaken, taken);
		}
	}
	return prev[w];
}
