# 題目21. 最大值與最小值
### 問題描述：
寫一個程式來找出輸入的十個數字的最大值和最小值，數值不限定為整數，且值可存放於 float 型態數值內。

### 輸入說明：
輸入十個數字，以空白間隔。

### 輸出說明：
輸出數列中的最大值與最小值，輸出時需附上小數點後兩位數字。

### 範例：
輸入範例:
-2 -15.2 0 89.5 100 25.3 7 30 76 4
0 3 52.7 998 135 -256 79 95 10 16  

輸出範例:
maximum:100.00
minimum:-15.20

maximum:998.00
minimum:-256.00

### 解答：
```
#include <iostream>  
#include<iomanip>  
using namespace std;

int main() {
    double num[10];
    double max;
    double min;
    for (int i = 0; i < 10; i++)
    {
        cin >> num[i];
        //輸入10個數字並將其設為數組，判斷數組中的最大值和最小值並輸出
        if (i == 0)
        {
            max = num[i];
            min = num[i];
        }
        else
        {
            if (num[i] > max)
            {
                max = num[i];
            }
            if (num[i] < min)
            {
                min = num[i];
            }
        }
    }
    cout << fixed << setprecision(2) << "maximum:" << max << endl;
    cout << fixed << setprecision(2) << "minimum:" << min << endl;
    return 0;
}
```
