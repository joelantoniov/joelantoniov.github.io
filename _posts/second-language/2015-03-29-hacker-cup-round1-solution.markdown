---
layout: post
title:  "Facebook Hacker cup 2015, Round 1 Solution"
date:   2015-03-29 11:30:00
categories: fr post
---

Code Jam 2015 is close, so I wanna practice resolving Hacker cup 2015's problems. Let's begin.

<b>Homework</b>
---

The problem introduces the term <b>primacity</b> as:

Let $$I_{m}$$ an integer positive and $$P_{n}$$ a prime number, the primacity of $$I_{m}$$ is the amount of $$P_{n}$$ which divides it.

For example: Let $$I = 550$$, its primacity is $$3$$ becuase $${2, 5 \mbox{ and } 11}$$ divide it.

The problem ask us: Given 3 numbers $$A, B \mbox{ and } K$$, how many integers in the inclusive range $$[A, B]$$ have a primacity of exactly $$K$$

<b>Constraints:</b>

$$1 \leq T \leq 100$$ , Let $$T$$ the number of test cases \\
$$2 \leq A \leq B \leq 10^7$$ \\
$$1 \leq K \leq 10^9$$ 

Clearly, we need to have a list of primes numbers for used later, we can use a modified of the [Sieve of Eratosthenes][algorithm1]. 
Let $$L$$ an array with length $$10^7+1$$ with initialized values of 0, the principle idea here is that each time that we found a $$P_{n}$$ in the sieve we 
increment by $$1$$ to $$L[P_{n}]$$ thought $$L[iP_{n}]$$, where $$i$$ is a number lesser than $$\frac{10^7}{P_{n}}$$. Then, when we ask if $$I_{m}$$
in the interval $$[A, B]$$ has primacity $$K$$, just we need to check out if $$I_{m}==L[I_{m}]$$.  After that only we increment an $$r$$ by 1 each time
that last statement is true for get the final answer. The complexity of this task is the same than the Sieve: $$\mathcal{O}(n\log{}n)$$ for the integers
$$1 \mbox{ to } n$$.

{% highlight c++ linenos %}
typedef long long ll
#define MAXN 10000001

ll L[MAXN];

void sieve(){
  memset(L, 0, sizeof(L));
  for(ll i = 2; i <= MAXN; i++){
    if(L[i] == 0){
      for(ll j = i; j <= MAXN; j+=i)
        L[j]++;
    }
  }
}

int main(){
  int T;
  ll a, b, k, r;
  cin >> T;
  for(int i = 1; i <= T; i++){
    r = 0;
    cin >> a >> b >> k;
    for(ll j = a; j <= b; j++){
      if(L[j] == k) r++;
    }
    cout << "Case #" << i << ": " << r << "\n";
  }
  return 0;
}
{% endhighlight %}

<b>Autocomplete</b>
---

In layman's terms the problem asks us:

If you have $$N$$ distinct words in a dictionary, What's the sum up for each smallest non-empty prefix of the word for autocomplete it. Where $$1 \leq N \leq 100 000$$

As the problem said, we need get the smallest non-empty prefix, so we are talking about a [Trie][Trie]. The time insertion is of course $$\mathcal{O}(L)$$, where $$L$$ is the length of the word. Apart of the trie, we initialize two arrrays $$step[i]$$ and $$deep\mbox{_}word[i]$$ both in 0's. So when we are inserting the word in the trie, we take a $$x$$ initialized in 0, then we equal $$x$$ in the trie $$(x, i)$$ and we increment $$step[x]$$ by one. What happen if $$step[x] = 1$$? It does mean that the answer is $$deep\mbox{_}word[x]$$ because already we found the smallest non-empty prefix, in otherwise, the answer will be the length complete of the word.

The worst case is when we need to type all the word, so the total complexity of the problem is $$\mathcal{O}(M)$$, where $$M = \sum_{i=0}^{n} L_{i}$$.

{% highlight c++ linenos  %}
#define MAXN 1000004

int trie[MAXN][27], step[MAXN], deep_word[MAXN];
int top;

int add(string s){
  int x = 0, deep = 1, ans = -1;
  for(int i = 0; i < s.size(); i++){
    int nxt = trie[x][s[i]-'a'];
    if(nxt == -1)
      trie[x][s[i]-'a'] = top++;
    x = trie[x][s[i]-'a'];
    step[x]++;
    deep_word[x] = deep++;
    if(ans == -1 && step[x] == 1)
      ans = deep_word[x];
  }
  if(ans == -1) ans = s.size();
  return ans;
}

int main(){
  int t, n, ans;
  string s;
  cin >> t;
  for(int i = 1; i < t; i++){
    top = 1;
    memset(trie, -1, sizeof(trie)); 
    memset(step, 0, sizeof(step)); 
    ans = 0;
    cin >> n; while(n--){
      cin >> s;
      ans += add(s);
    }
    cout << "Case #" << i << ": " << ans << "\n";
  }
  return 0;
}

{% endhighlight  %}

<b>Winning at Sports</b>
---

We have scores are denoted by two hyphen-separated integers $$x-y$$ where $$x$$ is you and you always win. Then, the problem introduces two terms:

<b>Stress-free victory:</b> You score the first point and from then on you always have more points than your opponent.

<b>Stressful victory:</b> You never have more points than your opponent until after their score is equal to their final score.

Then the problem asks us: Given the final score of a game of Sports, how many ways could you arrange the order in which the points are scored such that you secure a stress-free or stressful win?

We can resolve this problem using dynamic programming technique. The solution is both case are similar, but the conditions change.

Let $$A \mbox{ y } B$$ the final score, then for stress-free victory we have:

stress_free($$a$$, $$b$$) if ($$a \leq b$$) return 0, because it's not a stress-free victory \\
stress_free($$a$$, $$b$$) if ($$a > A \ || \ b > B$$) return 0, becuase it's not a stress-free victory \\
stress_free($$a$$, $$b$$) if ($$a == A \ \&\&  \ b == B$$) rerturn 1, because it's a stress-free victory \\
dp[$$a$$][$$b$$] = stress_free($$a+1$$, $$b$$) + stress_free($$a$$, $$b+1$$) 

For stressful:

stress_free($$a$$, $$b$$) if ($$a > b$$) return 0, because it's not a stressful victory \\
stress_free($$a$$, $$b$$) if ($$a > A \ || \ b > B$$) return 0, becuase it's not a stressful victory \\
stress_free($$a$$, $$b$$) if ($$b == B$$) rerturn 1, because it's a stressful victory \\
dp[$$a$$][$$b$$] = stressful($$a+1$$, $$b$$) + stressful($$a$$, $$b+1$$)

{% highlight c++ linenos %}
#define MAXN 2004
#define MOD 1000000007

int dp1[MAXN][MAXN], dp2[MAXN][MAXN];
int A, B;

int stress_free(int a, int b){
  if(a <= b) return 0;
  if(a > A || b > B) return 0;
  if(a == A && b == B) return 1;

  int &r = dp1[a][b];

  if(r == -1){
    r = stress_free(a+1, b) + stress_free(a, b+1);
    r %= MOD;
  }

  return r;
}

int stressful(int a, int b){
  if(a > b) return 0;
  if(a > A || b > B) return 0;
  if(b == B) return 1;

  int &r = dp2[a][b];

  if(r == -1){
    r = stressful(a+1, b) + stressful(a, b+1);
    r %= MOD;
  }

  return r;
}

int main(){
  ios_base::sync_with_stdio(false);
  int t;
  char c;
  for(int i = 1; i <= t; i++){
    cin >> A >> c >> B;
    memset(dp1, -1, sizeof(dp1));
    memset(dp2, -1, sizeof(dp2));
    cout << "Case #"  << i << ": " << stress_free(1, 0) << " ";
    cout << stressful(0, 0) << "\n";
  }
  return 0;
}
{% endhighlight  %}

<b>Corporate Gifting</b>
---

This is a kind [Graph coloring problem][gcoloring]. The employees are the nodes, so we build a vector with adjacency list to save the relation. We use
dynamic programming technique to dertemine the sum of all the colors $$DP[MAXN][MAXK]$$, what it is MAXK? It is the maximum numbers of colors for each node, so
we'll assume that max color is 32, in otherwise, we will not able to compute it.

For each node we go through all its parents, and after we go throught [1, 32> possible chromatic number, actually we do something like [Dijkstra's algorithm][algorithm2]. We have a variable $$tmp = \infty$$, so $$tmp = \min{(tmp, solving(next, j))}$$. After that just we add up $$DP[a][b] += tmp$$

The complexity of the problem is $$\mathcal{O}(n)$$, thanks to the DP.

{% highlight c++ linenos %}
#define MAXN 270000
#define MAXK 32
#define INF 0x3f3f3f3f

vector<int> adj[MAXN];
int DP[MAXN][MAXK], J=0;

int solving(int a, int b){
  if(DP[a][b] == -1){
    DP[a][b] = 0;
    for(int i = 0; i < (int)adj[a].size(); i++){
      int next = DP[a][i];
      int tmp = INF;
      for(int j = 1; j < MAXK; j++){
        if(b == j) continue;
        if(tmp > j + solving(next, j)) J = max(J, j);
        tmp = min(tmp, j + solving(next, j));
      }
      DP[a][b] += tmp;
    }
  }
  return DP[a][b];
}

int main(){
  int t, n, tmp;
  cin >> t;
  for(int i = 1; i <= t; i++){
    cin >> n;
    for(int e = 0; e <= n; e++) adj[e].clear();
    for(int j = 1; j <= n; j++){
      cin >> tmp;
      adj[tmp].push_back(j);
    }
    memset(DP, -1, sizeof(DP));
    cout << "Case #" << i << ": " << solving(0, 0) << "\n";
  }
  return 0;
}
{% endhighlight %}

You can find the codes here: [Codes solutions][csolutions] 

The full problems: [Facebook Hacker Cup 2015 Round 1][fullproblems]


[algorithm1]: https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes
[Trie]: https://en.wikipedia.org/wiki/Trie
[gcoloring]: https://en.wikipedia.org/wiki/Graph_coloring
[algorithm2]:https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm
[csolutions]: https://github.com/joelantonio/HackerCup2015
[fullproblems]:https://www.facebook.com/hackercup/problems.php?pid=582396081891255&round=344496159068801
