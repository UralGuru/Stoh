# Stoh
s = input().split(" ")
n = int(s[0])
m = int(s[1])
A = []
for i in range(n):
    str = input().split(' ')
    for k in range(len(str)):
        str[k] = float(str[k])
    A.append(str)
#print(A)
#print(*A, sep="\n")
#print(A[0][1])
a = 0
f = 0
for q in range(n):
    a = a + round(sum(A[q]), 3)
    n = float(n)
    if a == n:
        f = 1
    else:
        def transpose(matr):
            res = []
            n = len(matr)
            m = len(matr[0])
            for j in range(m):
                tmp = []
                for i in range(n):
                    tmp = tmp + [matr[i][j]]
                res = res + [tmp]
            return res
        r = transpose(A)
        b = 0
        for p in range(m):
            b = b + round(sum(A[p]), 3)
            m = float(m)
            if b == m:
                f = 1
            else:
                f = 0
            m = int(m)
if f == 0:
    print("не стохастическая")
else:
    print("стохастическая")



