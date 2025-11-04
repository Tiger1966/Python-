#阶乘
def factorial1(n):
    product=1
    for i in range(1,n+1):
        product*=i
    return product
print(factorial1(4))

def factorial2(n):
    if n==0:
        return 1
    else:
        return factorial2(n-1)*n #递归公式
for i in range(1,6):
    print(i,factorial2(i))
    
#斐波那契数列
def Fibonacci_numbers(n):
    if n==0 or n==1:
        return n
    else:
        return Fibonacci_numbers(n-1)+Fibonacci_numbers(n-2)
for i in range(1,6):
    print(i,Fibonacci_numbers(i))
    
    
#辗转相除
def gcd(p,q):#最大公因数
    if q==0:
        return p
    else:
        return gcd(q,p%q)
print(gcd(10,12))
def lcm(p,q):#最小公倍数
    return p*q//gcd(p,q)
print(lcm(10,12))

#排列
def permutation(n,k):
    return factorial2(n)//factorial2(n-k)

#组合
def combination(n,k):
    return permutation(n,k)//factorial2(k)
    
#二项式系数
def binomial_coefficients(n):
    for i in range(n+1):
        print(combination(n,i),end="\t")
    print()
binomial_coefficients(3)

#杨辉三角
def Pascal_triangle(n):
    for i in range(n+1):
        binomial_coefficients(i)
Pascal_triangle(5)
