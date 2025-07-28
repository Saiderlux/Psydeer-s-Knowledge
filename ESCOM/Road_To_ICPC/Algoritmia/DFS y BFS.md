## DFS
Contar componentes
```c++
vector<vector<int>> adj;
vector <bool> vis;

int main(){
	int n, m;
	cin>>n>>m;
	vis.resize(n+1);
	adj.resize(n+1);
	for(int i =0; i<m; i++){
		int u,v;

		cin>>u>>v;
		adj[u].psuh_back(v);
		adj[v].psuh_back(u);
	}
	for(int u=1; v<=n;v++){
		if(vis[v]) continue;
		dfs(v);
		contar++;
	}
	cout<<contar<<end;
	return 0;
}

void dfs(int v){
	vis[v]=true;
	for(auto : adj[v]){
		if(vis[u])continue;
		dfs(u);	
	}

}
```
