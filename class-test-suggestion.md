## 1. [Balanced Array](https://codeforces.com/contest/1343/problem/B)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n;
          cin >> n;

          while (n--)
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
          int arr[5][5];

          for (int i = 0; i < 5; i++)
          {
                    for (int j = 0; j < 5; j++)
                    {
                              cin >> arr[i][j];
                    }
          }

          int a, b;

          for (int i = 0; i < 5; i++)
          {
                    for (int j = 0; j < 5; j++)
                    {
                              if (arr[i][j] == 1)
                              {
                                        a = i;
                                        b = j;
                                        break;
                              }
                    }
          }

          int move = 0, flag = 0;

          do
          {

                    if (a > 2)
                    {
                              a--;
                              move++;
                    }
                    else if (a < 2)
                    {
                              a++;
                              move++;
                    }
                    else if (b > 2)
                    {
                              b--;
                              move++;
                    }
                    else if (b < 2)
                    {
                              b++;
                              move++;
                    }

          } while (a != 2 || b != 2);

          cout << move;

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
          string v;

          for (int i = 0; i < n; ++i)
          {
                    cin >> v;

                    if (v[1] == '+')
                    {
                              x++;
                    }
                    else
                    {
                              x--;
                    }
          }

          cout << x << endl;

          return 0;
}
```

## 6. [Team](https://codeforces.com/contest/231/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int problems, count = 0;

          cin >> problems;

          for (int i = 0; i < problems; i++)
          {
                    int a, b, c, sum;
                    cin >> a >> b >> c;

                    sum = a + b + c;

                    if (sum >= 2)
                    {
                              count++;
                    }
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

          for (int i = 0; i < t; i++)
          {
                    int n;
                    cin >> n;

                    int sum = (n / 10) + (n % 10);

                    cout << sum << endl;
          }

          return 0;
}
```

## 8. [Way to long words](https://codeforces.com/contest/158/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int n, length;
          cin >> n;

          while (n--)
          {
                    string word;
                    cin >> word;

                    length = word.length();

                    if (length > 10)
                    {
                              cout << word[0] << length - 2 << word[length - 1] << "\n";
                    }
                    else
                    {
                              cout << word << endl;
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
          string word1;
          string word2;
          cin >> word1 >> word2;

          for (int i = 0; i < word1.length(); i++)
          {
                    char c1 = word1[i];
                    char c2 = word2[i];

                    word1[i] = tolower(c1);
                    word2[i] = tolower(c2);
          }

          if (word1 > word2)
          {
                    cout << 1;
          }
          else if (word1 < word2)
          {
                    cout << -1;
          }

          else if (word1 == word2)
          {
                    cout << 0;
          }

          return 0;
}
```

## 10. [New year & Hurry](https://codeforces.com/contest/158/problem/A)

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
          int problems, time;
          cin >> problems >> time;

          int maxTime = 240;
          int leftTime = maxTime - time;

          int count = 0;
          int takenTime = 0;
          int timePerQuestion = 5;
          int testCases = problems;

          while (testCases > 0)
          {
                    count++;
                    takenTime += timePerQuestion;
                    timePerQuestion += 5;

                    if (takenTime > leftTime)
                    {
                              count--;
                              cout << count;
                              break;
                    }
                    testCases--;
          }

          if (testCases == 0)
          {
                    cout << problems;
          }

          return 0;
}
```
