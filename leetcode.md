# T1 2235.���������
ûɶ��˵��
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
# T2 2469.�¶�ת��
�ܼ򵥵��⣬���ǲ�֪���������ɶ��˼,���˵�ʱ�䣬����ΪҪ��󷵻�һ��vector
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
# T3 231.2����
�йض����Ƶ�һ��˼ά
��������λ�����������ȼ���ä�㣬���Ҫ��
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
# T4 2413.��Сż����
���鷳�ˣ�����ͨ�������ϰ��һ�¶���������
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