**Loops**

Decrement

```matlab
for v = 1.0:-0.2:0.0
    disp(v)
end
```

```matlabTextOutput
     1

    0.8000

    0.6000

    0.4000

    0.2000

     0
```

Looping through arrays

```matlab
for v = [[2:2:10],[1:2:9]]
    disp(v)
end
```

```matlabTextOutput
     2

     4

     6

     8

    10

     1

     3

     5

     7

     9
```

Repeat Statements for Each Matrix Column

```matlab
for I = magic(4)
    disp('Current unit vector')
    disp(sum(I))
end
```

```matlabTextOutput
Current unit vector
    34
Current unit vector
    34
Current unit vector
    34
Current unit vector
    34
```

Assign Matrix Values

```matlab
s = 10
```

```matlabTextOutput
s = 10
```

```matlab
H = zeros(s);
for c = 1:s
    for r = 1:s
        H(r,c) = 1/(r+c-1);
    end
end
H
```

```matlabTextOutput
H = 10x10
1.0000    0.5000    0.3333    0.2500    0.2000    0.1667    0.1429    0.1250    0.1111    0.1000
    0.5000    0.3333    0.2500    0.2000    0.1667    0.1429    0.1250    0.1111    0.1000    0.0909
    0.3333    0.2500    0.2000    0.1667    0.1429    0.1250    0.1111    0.1000    0.0909    0.0833
    0.2500    0.2000    0.1667    0.1429    0.1250    0.1111    0.1000    0.0909    0.0833    0.0769
    0.2000    0.1667    0.1429    0.1250    0.1111    0.1000    0.0909    0.0833    0.0769    0.0714
    0.1667    0.1429    0.1250    0.1111    0.1000    0.0909    0.0833    0.0769    0.0714    0.0667
    0.1429    0.1250    0.1111    0.1000    0.0909    0.0833    0.0769    0.0714    0.0667    0.0625
    0.1250    0.1111    0.1000    0.0909    0.0833    0.0769    0.0714    0.0667    0.0625    0.0588
    0.1111    0.1000    0.0909    0.0833    0.0769    0.0714    0.0667    0.0625    0.0588    0.0556
    0.1000    0.0909    0.0833    0.0769    0.0714    0.0667    0.0625    0.0588    0.0556    0.0526

```

Selectively Display Values in Loop: continue

```matlab
for n = 1:50
    if mod(n,7)==3
        continue
    end
    disp(num2str(n))
end
```

```matlabTextOutput
1
2
4
5
6
7
8
9
11
12
13
14
15
16
18
19
20
21
22
23
25
26
27
28
29
30
32
33
34
35
36
37
39
40
41
42
43
44
46
47
48
49
50
```

Factorial using while loop

```matlab
n = 10
```

```matlabTextOutput
n = 10
```

```matlab
f = n;
while n>1
    n = n-1;
    f = f*n;
end
disp(['n!=' num2str(f)])
```

```matlabTextOutput
n!=3628800
```

Infinite Loop

```matlab
f = 1
```

```matlabTextOutput
f = 1
```

```matlab
while f == 1
    disp(f)
end
```
