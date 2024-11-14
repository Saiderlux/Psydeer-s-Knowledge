$$DP(i)=\begin{cases}0 & i>n\\
 min(DP(i+1)+abs(h[i]-h[i+1],DP(i+2)+abs(h[i]-h[i+2])) & i<=n\\
\end{cases}$$
```cpp
int n;
h[];

int rec(int i){
	if(i>n) return 0;
	return min(rec(i+1)+abs(h[i]-h[i+1]));
}

int rec(int i){
	int uno=0;
	int dos=0;
	if(i+1<=n) rec(i+1)+abs(h[i]-h[i+1]);
	if(i+2<=n) return min(uno,dos);
	int minimo= INT_MAX;
}

int rec(int i, int x){
	for(int i=1;i<=x;i++){
		if(i+x<=n)
			minimo=min(minimo,rec(i+x)+abs(h[i]-h[i+x]));
	}
	return minimo;
}
```

Ahora con DP
```cpp
int n;
int h[];
int DP[n];

int rec(int i){
	 if(i>n) return 0;
	 int uno=0;
	 int dos=0;
	 if(i+1<=n){
		if(DP[i+1]!=-1) uno=DP[i+1];
		else DP[i+1]=rec(i+1)+abs(h[i]-h[i+1]);
	}
}
```
