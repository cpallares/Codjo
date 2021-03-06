# Rangoli

<!-- <img src="https://upload.wikimedia.org/wikipedia/commons/8/8c/Rangoli.jpg" /> -->
<img src="https://upload.wikimedia.org/wikipedia/commons/9/9d/Rangoli_before_and_after_colouring.jpg" />

This week's problem has a little more rhythm and a little less algorithm!

Rangoli is an art form from India in which patterns are created on the floor in living rooms or courtyards using materials such as colored rice, dry flour, colored sand or flower petals.

Description
----

Your challenge is to design a function that prints an alphabet rangoli of size _n_.

Here are some examples:

```
# n = 3:

----c----
--c-b-c--
c-b-a-b-c
--c-b-c--
----c----

# n = 5:

--------e--------
------e-d-e------
----e-d-c-d-e----
--e-d-c-b-c-d-e--
e-d-c-b-a-b-c-d-e
--e-d-c-b-c-d-e--
----e-d-c-d-e----
------e-d-e------
--------e--------

# n = 10:

------------------j------------------
----------------j-i-j----------------
--------------j-i-h-i-j--------------
------------j-i-h-g-h-i-j------------
----------j-i-h-g-f-g-h-i-j----------
--------j-i-h-g-f-e-f-g-h-i-j--------
------j-i-h-g-f-e-d-e-f-g-h-i-j------
----j-i-h-g-f-e-d-c-d-e-f-g-h-i-j----
--j-i-h-g-f-e-d-c-b-c-d-e-f-g-h-i-j--
j-i-h-g-f-e-d-c-b-a-b-c-d-e-f-g-h-i-j
--j-i-h-g-f-e-d-c-b-c-d-e-f-g-h-i-j--
----j-i-h-g-f-e-d-c-d-e-f-g-h-i-j----
------j-i-h-g-f-e-d-e-f-g-h-i-j------
--------j-i-h-g-f-e-f-g-h-i-j--------
----------j-i-h-g-f-g-h-i-j----------
------------j-i-h-g-h-i-j------------
--------------j-i-h-i-j--------------
----------------j-i-j----------------
------------------j------------------
```

The center of the rangoli has the first alphabet letter a, and the boundary has the alphabet letter (in alphabetical order).

Input Format
----

You are given an integer `n` where: `0 < n < 27`

Output Format
----

Print the alphabet rangoli in the format explained above.

Explicit Challenge
----

There are no tests* this week. Just make it work, and write it the best you can.

You should:

1. Have fun
2. Make pretty things
3. Write pretty code
4. Remember the things we've gone over

*You can submit your code to the [HackerRank](https://www.hackerrank.com/challenges/alphabet-rangoli) challenge if you want to run their tests.

Extra Challenge
----

Write your function so that it accepts any string `s` as input, where `len(s) > 0`, from which it builds its patterns.

Post screenshots of any cool designs you make!


For the extra challenge, let _n_ be any `n > 0`. If `n > len(s)` repeat from the beginning of `s`.

Example Input 1:

```
n = 15
s = u'\u03e8\u03e9\u03ea\u03eb\u03ec\u03ed\u03ee\u03ef\u03f0\u03f1\u03f2\u03f3\u03f4\u03f5\u03f6\u03f7\u03f8\u03f9\u03fa\u03fb\u03fc\u03fd\u03fe\u03ff\u0400\u0401\u0402\u0403\u0404\u0405\u0406\u0407\u0408\u0409\u040a\u040b\u040c\u040d\u040e\u040f\u0410\u0411\u0412\u0413\u0414\u0415\u0416\u0417\u0418\u0419\u041a\u041b\u041c\u041d\u041e\u041f\u0420\u0421\u0422\u0423\u0424\u0425\u0426\u0427\u0428\u0429\u042a\u042b\u042c\u042d\u042e\u042f\u0430\u0431\u0432\u0433\u0434\u0435\u0436\u0437\u0438\u0439\u043a\u043b\u043c\u043d\u043e\u043f\u0440\u0441\u0442\u0443\u0444\u0445\u0446\u0447\u0448\u0449\u044a\u044b'
```

Example Output 1:

```
----------------------------϶----------------------------
--------------------------϶-ϵ-϶--------------------------
------------------------϶-ϵ-ϴ-ϵ-϶------------------------
----------------------϶-ϵ-ϴ-ϳ-ϴ-ϵ-϶----------------------
--------------------϶-ϵ-ϴ-ϳ-ϲ-ϳ-ϴ-ϵ-϶--------------------
------------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------------------
----------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----------------
--------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--------------
------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------------
----------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----------
--------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--------
------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------
----϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϫ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----
--϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϫ-ϩ-Ϫ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--
϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϫ-ϩ-Ϩ-ϩ-Ϫ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶
--϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϫ-ϩ-Ϫ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--
----϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϫ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----
------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϫ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------
--------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϭ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--------
----------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϭ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----------
------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-Ϯ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------------
--------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϯ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶--------------
----------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϰ-ϱ-ϲ-ϳ-ϴ-ϵ-϶----------------
------------------϶-ϵ-ϴ-ϳ-ϲ-ϱ-ϲ-ϳ-ϴ-ϵ-϶------------------
--------------------϶-ϵ-ϴ-ϳ-ϲ-ϳ-ϴ-ϵ-϶--------------------
----------------------϶-ϵ-ϴ-ϳ-ϴ-ϵ-϶----------------------
------------------------϶-ϵ-ϴ-ϵ-϶------------------------
--------------------------϶-ϵ-϶--------------------------
----------------------------϶----------------------------
```

Example Input 2

```
n = 20
s = "CristinaLukeTamratPaulLinElaineStephanLeoCindySamarthKhalidAnaReed"
```

Example Output 2

```
--------------------------------------a--------------------------------------
------------------------------------a-P-a------------------------------------
----------------------------------a-P-t-P-a----------------------------------
--------------------------------a-P-t-a-t-P-a--------------------------------
------------------------------a-P-t-a-r-a-t-P-a------------------------------
----------------------------a-P-t-a-r-m-r-a-t-P-a----------------------------
--------------------------a-P-t-a-r-m-a-m-r-a-t-P-a--------------------------
------------------------a-P-t-a-r-m-a-T-a-m-r-a-t-P-a------------------------
----------------------a-P-t-a-r-m-a-T-e-T-a-m-r-a-t-P-a----------------------
--------------------a-P-t-a-r-m-a-T-e-k-e-T-a-m-r-a-t-P-a--------------------
------------------a-P-t-a-r-m-a-T-e-k-u-k-e-T-a-m-r-a-t-P-a------------------
----------------a-P-t-a-r-m-a-T-e-k-u-L-u-k-e-T-a-m-r-a-t-P-a----------------
--------------a-P-t-a-r-m-a-T-e-k-u-L-a-L-u-k-e-T-a-m-r-a-t-P-a--------------
------------a-P-t-a-r-m-a-T-e-k-u-L-a-n-a-L-u-k-e-T-a-m-r-a-t-P-a------------
----------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a----------
--------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a--------
------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a------
----a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-i-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a----
--a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-i-r-i-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a--
a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-i-r-C-r-i-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a
--a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-i-r-i-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a--
----a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-i-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a----
------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-s-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a------
--------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-t-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a--------
----------a-P-t-a-r-m-a-T-e-k-u-L-a-n-i-n-a-L-u-k-e-T-a-m-r-a-t-P-a----------
------------a-P-t-a-r-m-a-T-e-k-u-L-a-n-a-L-u-k-e-T-a-m-r-a-t-P-a------------
--------------a-P-t-a-r-m-a-T-e-k-u-L-a-L-u-k-e-T-a-m-r-a-t-P-a--------------
----------------a-P-t-a-r-m-a-T-e-k-u-L-u-k-e-T-a-m-r-a-t-P-a----------------
------------------a-P-t-a-r-m-a-T-e-k-u-k-e-T-a-m-r-a-t-P-a------------------
--------------------a-P-t-a-r-m-a-T-e-k-e-T-a-m-r-a-t-P-a--------------------
----------------------a-P-t-a-r-m-a-T-e-T-a-m-r-a-t-P-a----------------------
------------------------a-P-t-a-r-m-a-T-a-m-r-a-t-P-a------------------------
--------------------------a-P-t-a-r-m-a-m-r-a-t-P-a--------------------------
----------------------------a-P-t-a-r-m-r-a-t-P-a----------------------------
------------------------------a-P-t-a-r-a-t-P-a------------------------------
--------------------------------a-P-t-a-t-P-a--------------------------------
----------------------------------a-P-t-P-a----------------------------------
------------------------------------a-P-a------------------------------------
--------------------------------------a--------------------------------------
```


Example Input 3

```
n = 9
s = "xyz"
```

Example Output 3

```
----------------z----------------
--------------z-y-z--------------
------------z-y-x-y-z------------
----------z-y-x-z-x-y-z----------
--------z-y-x-z-y-z-x-y-z--------
------z-y-x-z-y-x-y-z-x-y-z------
----z-y-x-z-y-x-z-x-y-z-x-y-z----
--z-y-x-z-y-x-z-y-z-x-y-z-x-y-z--
z-y-x-z-y-x-z-y-x-y-z-x-y-z-x-y-z
--z-y-x-z-y-x-z-y-z-x-y-z-x-y-z--
----z-y-x-z-y-x-z-x-y-z-x-y-z----
------z-y-x-z-y-x-y-z-x-y-z------
--------z-y-x-z-y-z-x-y-z--------
----------z-y-x-z-x-y-z----------
------------z-y-x-y-z------------
--------------z-y-z--------------
----------------z----------------
```

<img src="http://i.imgur.com/2PTW7sY.gif" />
----

Taken from [this](https://www.hackerrank.com/challenges/alphabet-rangoli) HackerRank problem
