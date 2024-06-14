# Binary

```
 recFormat=x,i,d,13f
 x=skip. i=int s=short,b=byte,us=unsigned short,f=float,d=double
```

convenient way to describe structures (Cluster "rot" files) This would
imply field count, etc.

```
 format= int1, int2, int4, real4, real8, etc, types that are easier to remember.
```

# Ascii

```
 recFormat=4x,i9,d16,13f  scanf-style format spec.  Much better that fixedColumns, etc.
```

