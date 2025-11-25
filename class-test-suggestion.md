## 1. [Balanced Array](https://codeforces.com/contest/1343/problem/B)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int t;
          cin >> t;

          while (t--)
          {
                    int size, sume = 0, sumo = 0, k = 0;
                    cin >> size;

                    int arr[size];

                    if (size % 4 == 0)
                    {
                              cout << "YES" << "\n";

                              for (int i = 2; i <= size; i += 2)
                              {
                                        arr[k] = i;
                                        k++;
                                        sume += i;
                              }

                              for (int i = 1; k < size - 1; i += 2)
                              {
                                        arr[k] = i;
                                        sumo += i;
                                        k++;
                              }

                              arr[k] = sume - sumo;

                              for (int i = 0; i < size; i++)
                              {
                                        cout << arr[i] << " ";
                              }
                              cout << "\n";
                    }
                    else
                    {
                              cout << "NO" << "\n";
                    }
          }

          return 0;
}
```

## 2. [Beautiful Matrix](https://codeforces.com/contest/263/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
    for (int i = 0; i < 5; i++)
    {
        for (int j = 0; j < 5; j++)
        {
            int x;
            cin >> x;

            if (x == 1)
            {
                cout << abs(i - 2) + abs(j - 2);
            }
        }
    }

    return 0;
}
```

## 3. [Watermelon](https://codeforces.com/contest/4/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n;

          cin >> n;

          if (n % 2 == 0 && n > 2)
          {
                    cout << "YES";
          }
          else
          {
                    cout << "NO";
          }

          return 0;
}
```

## 4. [Theatre Square](https://codeforces.com/contest/1/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          long long n, m, a;
          cin >> n >> m >> a;

          n = (n + a - 1) / a;
          m = (m + a - 1) / a;

          cout << n * m;

          return 0;
}
```

## 5. [Bit++](https://codeforces.com/contest/282/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n;
          cin >> n;

          int x = 0;

          while (n--)
          {
                    string s;
                    cin >> s;

                    x += (s[1] == '+') ? 1 : -1;
          }

          cout << x;

          return 0;
}
```

## 6. [Team](https://codeforces.com/contest/231/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n, count = 0;
          cin >> n;

          while (n--)
          {
                    int a, b, c, sum;
                    cin >> a >> b >> c;

                    count += (a + b + c) >= 2;
          }

          cout << count;

          return 0;
}
```

## 7. [A+B again?](https://codeforces.com/contest/1999/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int t;
          cin >> t;

          while (t--)
          {
                    int n;
                    cin >> n;

                    int sum = (n / 10) + (n % 10);

                    cout << sum << '\n';
          }

          return 0;
}
```

## 8. [Way to long words](https://codeforces.com/problemset/problem/71/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n;
          cin >> n;

          while (n--)
          {
                    string word;
                    cin >> word;

                    int length = word.length();

                    if (word.length() > 10)
                    {
                              cout << word[0] << length - 2 << word[length - 1] << "\n";
                    }
                    else
                    {
                              cout << word << '\n';
                    }
          }

          return 0;
}
```

## 9. [Petya & Strings](https://codeforces.com/contest/112/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          string a, b;
          cin >> a >> b;

          for (int i = 0; i < a.size(); i++)
          {
                    a[i] = tolower(a[i]);
          }
          for (int i = 0; i < b.size(); i++)
          {
                    b[i] = tolower(b[i]);
          }

          cout << (a > b ? 1 : a < b ? -1
                                     : 0);

          return 0;
}
```

## 10. [New year & Hurry](https://codeforces.com/problemset/problem/750/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n, t;
          cin >> n >> t;

          int left = 240 - t;
          int solved = 0;
          int timeNeeded = 0;

          for (int i = 1; i <= n; i++)
          {
                    timeNeeded += 5 * i;
                    if (timeNeeded > left)
                    {
                              break;
                    }
                    solved++;
          }

          cout << solved;

          return 0;
}
```
