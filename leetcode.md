# T1 2235.两整数相加
没啥好说的
```cpp
class Solution 
{
public:
    int sum(int num1, int num2) 
    {
        return num1+num2;
    }
};
```
# T2 2469.温度转换
很简单的题，但是不知道输出数组啥意思,费了点时间，还以为要最后返回一个vector
```cpp
class Solution 
{
public:
    vector<double> convertTemperature(double celsius) 
    {
        double Kelvin,Fahrenheit;
        Kelvin=celsius+273.15;
        Fahrenheit=celsius*1.80+32.00;
        return {Kelvin,Fahrenheit};
    }
};
```
# T3 231.2的幂
有关二进制的一点思维
还摸到了位运算运算优先级的盲点，这个要补
```cpp
class Solution 
{
public:
    bool isPowerOfTwo(int n) 
    {
        if(n>0 && (n&(n-1))==0)
            return 1;
        else
            return 0;
    }
};
```
# T4 2413.最小偶倍数
想麻烦了，但是通过这个练习了一下二进制运算
```cpp
class Solution {
public:
    int smallestEvenMultiple(int n) 
    {
        return n % 2 == 0 ? n : 2*n;
    }
};
//another solution
class Solution {
public:
    int smallestEvenMultiple(int n) 
    {
        int temp=0;
        if(n%2)
            return 2*n;
        else
        {
            while(n%2==0)
        {
            temp++;
            n/=2;
        }
        return (1<<temp)*n;
        }
        
    }
};
```