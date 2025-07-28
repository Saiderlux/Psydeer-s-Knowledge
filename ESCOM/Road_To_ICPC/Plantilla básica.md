```cpp
#include <bits/stdc++.h>
using namespace std;

// -------------------- OPTIMIZACIONES --------------------
#pragma GCC optimize("O3,unroll-loops")
#pragma GCC target("avx2,bmi,bmi2,popcnt,lzcnt")

// -------------------- ALIAS DE TIPOS --------------------
using ll = long long;
using ull = unsigned long long;
using ld = long double;
using pii = pair<int, int>;
using pll = pair<ll, ll>;
using vi = vector<int>;
using vll = vector<ll>;
using vpii = vector<pii>;
using vpll = vector<pll>;

// -------------------- MACROS --------------------
#define endl '\n'                  // Reemplaza "\n" para velocidad
#define pb push_back
#define eb emplace_back
#define all(x) (x).begin(), (x).end()
#define rall(x) (x).rbegin(), (x).rend()
#define sz(x) ((int)(x).size())
#define rep(i, a, b) for (int i = (a); i < (b); ++i)
#define per(i, a, b) for (int i = (a)-1; i >= (b); --i)
#define yes cout << "YES\n"
#define no cout << "NO\n"

// -------------------- DEBUG --------------------
#ifdef LOCAL
#define debug(x) cerr << #x << ": " << x << endl
#else
#define debug(x)
#endif

// -------------------- FUNCIONES ÚTILES --------------------
template<typename T> inline void chmin(T &a, T b) { a = min(a, b); }
template<typename T> inline void chmax(T &a, T b) { a = max(a, b); }

// -------------------- CONSTANTES --------------------
const int INF = 1e9;
const ll LINF = 1e18;
const int MOD = 1e9 + 7;  // cambia según el problema
const int MX = 2e5 + 5;

// -------------------- LECTURA RÁPIDA --------------------
void fastIO() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
}

// -------------------- LÓGICA PRINCIPAL --------------------
void solve() {
    // TODO: Escribe aquí tu lógica para un caso de prueba
    int n;
    cin >> n;
    vi a(n);
    rep(i, 0, n) cin >> a[i];
    sort(all(a));
    cout << a[0] << endl;
}

// -------------------- MAIN --------------------
int main() {
    fastIO();
    int T = 1;
    // cin >> T; // descomenta si hay múltiples casos
    while (T--) {
        solve();
    }
    return 0;
}

```