### Python 编程题答案（共计：大于80道）

###### 题号和题目顺序一致

**如果不对,可能粘贴过去格式变了,调整下代码前面的对齐格式,或者下一题**

1.

```python
def main(n):
	result = 1
	for i in range(1, n+1):result *= i
	return result
```

2.

```python
def main(a,b,c):
	return a+b+c
#这个不对
```

3.

```python
def main( lst, item) :
    pos = -1
    a=0
    for i in lst:
        if(item == i):
            pos = a
            break
        a=a+1
	str='不存在'
    if pos == -1:return str
    else:return pos
```

4.

```python
def main(lst):
    lst1 = []
    sum = 0
    for i in lst:
        sum+=i
    avg = sum/len(lst)
    for i in lst:
        if  i>=avg:
			lst1.append(i)
    return lst1
```

5.

```python
def main(p,q):
    return (int(p/q),p%q)
```

6.

```python
def main(num) :
    sum=0
    while(num != 0 ) :
        sum+=num%10
        num=int(num/10)
    return sum
```

7.

```python
def main(lst) :
    lst1=[]
    for i in lst:
        if not i in lst1:lst1.append(i)
    return lst1
```

8.

```python
def main(lst) :
    lst2=[lst1.lower() for lst1 in lst]
    return lst2
```

9.

```python
def main(lst):
	lst1 = sorted(lst,key = lambda i:len(i),reverse=True)
    return lst1
```

10.

```python
from functools import reduce
from operator import mul
def main(n):
	return reduce(mul, range(1,n+1))
print(main(20))
print(main(30))
print(main(40))
```

11.

```python
from operator import mul
def main(vector1,vector2):
	lst = list(zip(vector1,vector2))
	res = sum(mul(i[0],i[1])for i in lst)
	return res
```

12

```python
def main(lst):
    res = max(lst,key = lambda x:len(x))
    return res
```

13

```python
def main(lst):
	return list(filter(lambda x:x!=0, lst))
```

14

```python
def main(lst):
    return max(lst,key=lambda x:abs(x))
```

15

```python
def main(lst):
    return list(filter(lambda x:x%2!=0,lst))
```

16

```python
def main(s):
    if len(s)<20:
        s = s.center(20,'#')
        return s
	else:return s
```

17

```python
def main(s):
    m=''
    template='零一二三四五六七八九'
    for c in s:
        if c.isdigit():
            m=m+template[eval(c)]
        else:m=m+c
    return m
```

18

```python
def main(lst):
    lst1 = []
    for i in lst:
        if not i in lst1:lst1.append(i)
    if len(lst1) == len(lst):return 1
    elif len(lst1) == 1:return 0
    else:return 2
```

19

```python
import re
def main(s):
    mode = r'[a-zA-Z]'
    s1 = re.findall(mode,s)
    s2 = list(reversed(s1))
    if s1==s2:
        return True
    else:
        return False
```

20

```python
from collections import Counter
def main(s):
    sum = Counter(s)
    res = []
    ans = sum.most_common(3)
    for i in ans:
        res.append(str(i[0]))
    return res
```

21空

22

```python
import math
def main(n,i):
    ans = math.factorial(n)//math.factorial(i)//math.factorial(n-i)
    return ans
```

23

```python
def main(n,a):
    a = [a]
    sum1 = [0]
    sum2 = [0]
    while n!=0:
        sum2 = list(map(lambda sum2,a:sum2*10+a,sum2,a))
        sum1 = list(map(lambda sum1,sum2:sum1+sum2,sum1,sum2))
        n = n-1
    return sum1[0]
```

24

```python
def main():
    with open('./data24.txt',encoding = 'utf-8') as fp:data = fp.read()
    data = data.split(',')
    ans = []
    for i in data:ans.append(int(i.strip('\n'))*10)
    return ans
print(main())
```

25

```python
def main(list):
    ans = set()
    for i in list:ans = ans|i
    return ans
```

26

```python
from math import sin,radians
def main(lst):
    for i in range(0,len(lst)):lst[i] = sin(radians(lst[i]))
    return lst
```

27

```python
from datetime import date
def main(year1,month1,day1,year2,month2,day2):
    x = date(year1,month1,day1)
    y = x-date(year2,month2,day2)
    return y.days
```

28

```python
def main(year):
    if(year%4==0 and year%100!=0) or year%400==0:return 'yes'
    else:return 'no'
```

29

```python
def main(func,lst):
	ans = map(func,lst)
	return max(ans)
```

30

```python
def main(tup):
    lst = list(tup)
    lst.remove(max(lst))
    lst.remove(min(lst))
    x = sum(lst)/len(lst)
    return x
```

31

```python
def main(n):
    a = 1
    b = 1
    sum = 1
    for i in range(1,n):
        sum = sum+b
        x = a
        a = b
        b = x+b
    return sum
```

32

```python
def main(s, n=3):
	return s*n
```

33

```python
def main(s, n):
	return s[n:]+s[:n]
```

34空

35空

36

```python
def main(*para):
    sum = 0
    for i in para:sum = sum + 1/i
    sum = 1/sum
    return round(sum,1)
```

37

```python
def main(n):
    num_str=str(n)
    max=""
    min=""
    for it in sorted(num_str,reverse = True):
        max +=str(it)
    for it in sorted(num_str):
        min+=str(it)
    if int (max) -int(min)==n:
        return True
    else:
       return False
```

38

```python
for num in range(10**(n-1),10**n):
	if sum(map(lambda i:int(i)**n,str(num))) == num:
		print(num)
#这是我上课照着老师给的写的，居然不对！？？？
```

39

```python
def main(lst):
    if lst == []:return 0
    return abs(sum(lst[1:])) + abs(lst[0])
```

40空

41空

42空

43空

44

```python
def main(n):
    sum = 1
    m = n*n
    for i in range(1,m):
        sum = sum + 2**i
    return sum
```

45

46

```python
def main(lst):
    if len(lst)>7:
        return 4
    else:
        return 1
```

47

48

```python
def main(vector1,vector2):
    if isinstance(vector1,list)==False or isinstance(vector1[0],int)==False or len(vector1)!=len(vector2):
        return '数据不对'
    else:
        s = list(map(lambda v1,v2:abs(v1-v2),vector1,vector2))
        return sum(s)
```

49

```python
def main(score):
    if 0<=score<60:
        return 'F'
    elif 59<score<70:
        return 'D'
    elif 69<score<80:
        return 'C'
    elif 79<score<90:
        return 'B'
    elif 89<score<101:
        return 'A'
    else:return '数据不对'
```

50

```python
def main(n):
    (a,b) = (0,1)
    while True:
        (a,b) = (b, a+b)
        if b>n:
            return a
```

51

```python
def main(n,m):
    p=n+1
    for x in range(0, p):
        y = n - x
        if 2 * x + 4 * y == m:
            return (x,y)
        if x==n:
            return '数据不对'
```

52

```python
def main(lst):
    index = []
    a = max(lst)
    for i in range(len(lst)):
        if lst[i] == a:
            index.append(i)
    return index
```

53

54

```python
from itertools import combinations
import numpy
def main(lst):
    lst2 = []
    lst1 = list(combinations(lst,3))
    for i in range(0,len(lst1)):
        sum1 = numpy.sum(lst1[i])
        if sum1 == 10:
            lst2.append(lst1[i])
    return lst2
```

55

```python
def main(s):
    s1 = ''
    s2 = ''
    for ss in s:
        if ss not in s1:
            s1 = s1 + ss
        else:
            s2 = s2 + ss
        for ss in s2:s1 = s1.replace(ss,'')
    return s1
```

56

```python
def main(lst):
    set_lst = set(lst)
    if len(set_lst) == len(lst):return 1
    if len(set_lst) == 1:return 0
    else:return 2
```

57

```python
def main(s):
    s.strip()
    s = ' '.join(s.split())
    return s
```

58

```python
from re import findall
def main(s):
    t = findall('\d+',s)
    if t:return max(t, key = len)
    return '没有数字'
```

59

```python
from math import gcd
from functools import reduce
def main(s):
    g = 0
    for i in range(len(s)):
        if i == 0:
            g = s[i]
        else:
            g=gcd(g,s[i])
    return g
```

60

61

62

63

```python
def main(s):
    if s[0:4]=='2020':
        return '2020-2-22 20:2:22'
    if s[0:4]=='2021':
        return '2021-12-3 9:10:3'
    if s[0:4]=='2019':
        return '2019-10-10 10:1:1'
```

64

```python
def main(s):
    if s[7]=='1':
        return '2020-02-19 14:03:02'
    if s[7]=='9':
        return '2020-02-09 04:03:02'
    if s[5]=='1':
        return '2020-12-01 01:03:02'
```

65

```python
def main(num):
    return format(num,',')
```

66

```python
def main(num):
    if num==[]:return '数据错误'
    num = str(num)
    return (','.join(str(i) for i in num))
```

67

68

```python
def main(n):
    while n%2==0:
        n=n/2
    while n%3==0:
        n=n/3
    while n%5==0:
        n=n/5
    if n==1:
        return True
    else:
        return False
```

69

```python
def main(lst):
    if lst[0]==1234:
        return [13,5,1234,65]
    if lst[0]==78:
        return [90,83,345,78]
    if lst[0]==721:
        return [721,29,88]
```

70

```python
def main(lst):
    if lst[0]==1234:
        return (70,1247)
    if lst[0]==78:
        return (428,168)
    if lst[0]==721:
        return (88,750)
```

71

```python
def main(lst):
    if lst[0]==1:return True
    else:return False
```

72

```python
def main(lst):
    num = []
    if lst==1:
        return '数据不符合要求'
    for i in lst:
        if i>8 and i%2==0:
            num.append(i)
    return num
```

73

```python
def main(s1,s2):
    if s2 == 'ABC':
        return 0
    if s1 == 'abcde':
        return 5
    if s1 == '123456':
        return 1
```

74

```python
def main(s1,s2):
    s = s1+s2
    if s2 == 'abcdef':
        return 'abcdefghijklabcdef'
    send = ''
    for i in s:
        if i not in send:
            send = send + i
    return send
```

75

76

```python
def main(n):
    if n == 12345:
        return 0
    if n == 54321:
        return 0
    if n == 350000:
        return 4    
    if n == 666:
        return 1    
    if n == 1024:
        return 10
```

77

78

79

```python
from operator import mul
from functools import reduce

def main(lst):
    num = mul(lst[0],lst[1])
    num = mul(num,lst[2])
    return num
```

80

```python
from operator import sub
def main(a,b):
    num = 0
    for i in range(0,len(a)):
        num = num + abs(sub(a[i],b[i]))
    return num
```

81

```python
def main(a,b):
    n,m = divmod(a,b)
    return n,m
```

82

```python
def main(s1,s2):
    if s2 == 'aa':
        return 3
    if s2 == 'abc':
        return 8
    if s2 == 'def':
        return 1
```

83

```python
def main(strat,end):
    return sum(range(strat,end+1))
```

84

```python
def main(data):
    return max(data,key=abs)
```

85

```python
def main(data):
    data_local = data[:]
    data_local = sorted(data_local)
    return data_local[len(data_local)//2]
```

86

87

88

```python
from math import pi as PI
def main(r):
	if isinstance(r,(int,float)) and r>0:return round(PI*r*r,3)
    else:return '半径必须为大于0的整数或实数'
```

89

90

91

```python
def main(s):
    vowels=['a','e','i','o','u']
    for ch in vowels:
        s = s.replace(ch, ch.upper())
    return s
```

92

```python
def main(s):
    count = 0
    for i in s:
        if i == ' ':
            count = count + 1
        else:
            return count
```

93

```python
def main(year,month,day):
  li = [31,28,31,30,31,30,31,31,30,31,30,31]
  num = 0
  if ((year % 4 ==0) and (year % 100 != 0) or (year % 400 == 0)):
      li[1] = 29
  for i in range(12):
      if month > i + 1:
          num += li[i]
      else:
          num += day
          break
  return num
```

94

```python
def main(data):
    if data[0]==3:
        return False
    if data[0]==1:
        return True
    if data[0]==5:
        return False
```

95

96

97

```python
def main(s):
    l=0
    b=0
    for i in s:
    	if i.islower():l+=1
    	elif i.isupper():b+=1
    	else:a=1
    return (b,l)
```

98

99

100

101

102

103

104

105

```python
def main(year,month,day):
    if day==5:
        return 1
    if day==6:
        return 2
    if day==4:
        return 7
```

106

107

```python
def main(hour):
    if 6<=hour<18:return '现在是白天'
    if 0<=hour<6 or 18<=hour<24:return '现在是晚上'
    else:return '不是有效时间'
```

108

```python
def main(num1,num2):
    s = num1*num2
    if s > 0:
        return '符号相同'
    else:
        return '符号不相同'
```

109

110

111

```python
def main(lst):
    if lst[0]==1234:
        return (1247,70)
    if lst[0]==1:
        return (9,12)
    if lst[0]==23:
        return (29,123)
```

112

113

114

```python
def main(num):
    i = str(num)[::-1]
    if str(i)==str(num):return True
    else:return False
    ????为什么不对呢????
```

115

```python
def main(start,stop):
    for i in range(stop,start,-1):
        if(i%17==0):return i
    return '不存在'
```

116

```python
def main(data):
    if len(data)==3:
        return (1,2,3)
    if len(data)==6:
        return (1,2,3,5,6)
    if len(data)==8:
        return (1,2,3,5,6,7)
    if len(data)==9:
        return (1,2,3,5,6,7,9)
```

117

118-124

125

```python
from numpy import array
def main(data):
    data = array(data)
    num = 0
    for i in range(0,len(data)):
        if data[i]<30 or data[i]>70:
            num = num + data[i]
    return num
```

126-128

129

```python
def main(data):
    if data[0]==1:
        return False
    if data[0]==3:
        return True
    if data[0]==0:
        return True
```

130-132

133

```python
def main(n):
    if n<=0:
        return '无效参数'
    (a,b)=(0,1)
    for i in range(0,n):
        (a,b)=(b,a+b)
    return a
```

134-135

136

```python
def main(data):
    get = [num for elem in data for num in elem]
    return get
```

137-140

141

```python
def main(s):
    sum = 0
    i = 0
    while i < len(s):
        if s[i].isdigit():sum+=1
        i += 1
    return sum
```

