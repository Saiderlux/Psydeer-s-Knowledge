## Iterativo
```cpp
int binaryIt(vector <int> a, int n){
	int low=0;
	int high=a.size()-1;
	int mid;

	while(low<=high){
		mid=low+(high-low)/2;
		if(a[mid] < n)
			low=mid+1;
		else if(a[mid>n])
			high=mid-1;
		else{
			return mid;
		}	
		return -1;
	}
}
```

## Recursivo

```cpp
int BinaryR(vector <int> a, int n, int low, int high){
	if(low>high){
		return -1;
	}
	int mid;
	if (a[mid]<n){
		return binaryR(a,n, mid+1, high);
	}
	else if{
		return binaryR(a,n,low,mid-1);
	}
	else
		return mid;
}

```

#### Upper bound
Va a regresar el número, inmediatamente después del que estamos buscando
por ejemplo:
{1,2,3,4,5,6,7,8,9,10} -> el upper de 1 es 2, el de 2 es 3, etc.

#### Lower bound
Estamos buscando el número más pequeño entre el número escogido y los menores
{1,2,3,4,5,6,7,20} el de 20 es 7, el de 7 es el mismo 7.

## Implementación lower bound
```cpp
int LowerR(vector <int> a, int n, int low, int high){
	if(low>high){
		return low;
	}
	int mid;
	if (a[mid]<n){
		return LowerR(a,n, mid+1, high);
	}
	else if{
		return LowerR(a,n,low,mid-1);
	}
	else
		return mid;
}

```
```cpp
int LowerIt(vector <int> a, int n){
	int low=0;
	int high=a.size()-1;
	int mid;

	while(low<=high){
		mid=low+(high-low)/2;
		if(a[mid] < n)
			low=mid+1;
		else if(a[mid>n])
			high=mid-1;
		else{
			return mid;
		}	
		return low;
	}
}
```

## Implementación upper bound
```cpp
int UpperIt(vector <int> a, int n){
	int low=0;
	int high=a.size()-1;
	int mid;

	while(low<=high){
		mid=low+(high-low)/2;
		if(a[mid] < n)
			low=mid+1;
		else if(a[mid>n])
			high=mid-1;
		else{
			return mid;
		}	
		return -1;
	}
}
```

```cpp
int BinaryR(vector <int> a, int n, int low, int high){
	if(low>high){
		return -1;
	}
	int mid;
	if (a[mid]<n){
		return binaryR(a,n, mid+1, high);
	}
	else if{
		return binaryR(a,n,low,mid-1);
	}
	else
		return ;
}

```
#### Ejemplo de uso de binary search

Existe un arr[] de ints y un número x, queremos encontrar el mínimo tamaño de sub-arreglos con una suma mayor que un valor K
	1)Input ordenado
	2) Oputput ordenado
	3) Rango L -> R
monotónica

inputo: arr, K.

|     |     |     |     |     |     |     |     |     |     |     |     |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |


