# 離散數學 - 筆記

## 1. 基礎：邏輯與證明

### 1.1 邏輯命題

#### Introduce - 命題

命題通常都是一個明確的陳述句，只會有True或者False兩種結果，不會有兩種結果同時出現的可能。



##### Example 1

1. Washington, D.C., is the capital of the United States of America.
2. Toronto is the capital of Canada.
3. 1 + 1 = 2.
4. 2 + 2 = 3.

命題 1 和 3 是 True，而命題 2 和 4 是 False



##### Example 2

1. What time is it?
2. Read this carefully.
3. x + 1 = 2.
4. x + y = z.

1 和 2 不是命題，因為他們並不是陳述句

3 和 4 不是命題，因為他們並沒辦法用True或者False回答



我們習慣用一些英文字母來當作命題變數(例如$p,q,r,s...$)，也就是用英文字母當作命題，就像數字的代數一樣。

如果命題是true，我們習慣用T來表示這個命題是true，而如果命題是false，則會使用F來表示這個命題是false。



#### Definition - 邏輯非

令$p$為一命題，$p$的邏輯非，我們表示為$\neg p$，或者也可以表示為$\overline{p}$，表示在$p$的條件下，結論不成立。

通常來說，$\neg p$讀做"not $p$"，而$\neg p$的值與$p$的值互為反相，也就是若$p$是true，則$\neg p$就是false，反之亦然。



##### Example 1

Find the negation of the proposition

"Michael’s PC runs Linux."

and express this in simple English.



The negation of "Michael's PC runs Linux" is "It's not the case that Michael's PC runs Linux."

This negation can be more simply expressed as "Michael's PC doesn't run Linux."



##### Example 2

Find the negation of the proposition

"Vandana’s smartphone has at least 32GB of memory"

and express this in simple English.



The negation of "Vandana’s smartphone has at least 32GB of memory" is "It's not the case that Vandana’s smartphone has at least 32GB of memory".

The negation can be more simply expressed as "Vandana’s smartphone does not have at least 32GB of memory"

or even more simply as "Vandana’s smartphone has less then 32GB of memory"



#### Table - 邏輯非的真值表

![image-20210115200649258](https://i.imgur.com/inKIp7g.png)

#### Definition - 邏輯與

令$p$與$q$為命題，$p$與$q$的邏輯與，我們表示為$p \and q$，念作"$p$ and $q$"。

當$p$與$q$都為True時，$p \and q$才會true，反之為false。



##### Example

Find the conjunction of the propositions $p$ and $q$ where $p$ is the proposition “Rebecca’s PC has more than 16 GB free hard disk space” and $q$ is the proposition “The processor in Rebecca’s PC runs faster than 1 GHz.”



The conjunction of the propositions $p$ and $q$ is 

"Rebecca’s PC has more than 16 GB free hard disk space, and the processor in Rebecca’s PC runs faster than 1 GHz."



#### Table - 邏輯與的真值表

![image-20210115201510053](https://i.imgur.com/p2VL2Fy.png)



#### Definition - 邏輯或

令$p$與$q$為命題，$p$與$q$的邏輯或，我們表示為$p \or q$，念作"$p$ or $q$"。

當$p$與$q$都為false時，$p \or q$為false，反之為true。



##### Example

What is the disjunction of the propositions p and q where p and q are the same propositions as in Example 5?



The disjunction of the propositions p and q is

"Rebecca’s PC has more than 16 GB free hard disk space, or the processor in Rebecca’s PC runs faster than 1 GHz."



#### Table - 邏輯或的真值表

![image-20210115201526194](https://i.imgur.com/EHoHvII.png)



#### Definition - 邏輯異或

令$p$與$q$為命題，$p$與$q$的邏輯異或，我們表示為$p \oplus q$。

當$p$或$q$都同為true或同為false時，$p \oplus q$為false，反之為true。



#### Definition - 實質蘊涵

令$p$與$q$為命題，$p$與$q$的 實質蘊涵，我們表示為$p \rightarrow q$，表示若$p$則$q$。

當$p$為true且$q$為false時，則$p \rightarrow q$為false，否則為true。

在實質蘊涵中的$p$，我們稱作前件，而$q$我們稱作後件



#### Table - 實質蘊涵的真值表

![image-20210224131607538](https://i.imgur.com/KegQo7N.png)

##### Example

若期末考考100分，那你就會拿到A。

合理(T)

P：若期末考考100分(T)，則Q：你會拿到A(T)

P：若期末考沒考100分(F)，則Q：你不會拿到A(F)

P：若期末考沒考100分(F)，則Q：你依然可能拿到A(T)

不合理(F)

P：若期末考考了100分(T)，則Q：沒拿到A(F)



#### Definition - 換位命題

令$p$與$q$為命題，$p$與$q$的換位命題，我們表示為$q \rightarrow p$。

當$p$為false且$q$為true時，$q \rightarrow p$為false，否則為true。



##### Example

若期末考考100分，那你就會拿到A。

合理(T)

Q：拿到A，則P：期末考考了100分

Q：沒有拿到A，則P：期末考沒有考100分

Q：拿到A，則P：期末考沒有考100分

不合理(F)

Q：沒有拿到A，則P：期末考考100分



#### Table - 換位命題的真值表

| P    | Q    | Q → P |
| ---- | ---- | ----- |
| 0    | 0    | 1     |
| 0    | 1    | 0     |
| 1    | 0    | 1     |
| 1    | 1    | 1     |



#### Definition - **換質換位命題**

令 $p$ 與 $q$ 為一個命題

則一條件敘述 $\neg q \rightarrow \neg p$ 稱作換質換位命題

質位互換命題與假設邏輯等價(也就是，$(\neg q \rightarrow \neg p) \leftrightarrow (p \rightarrow q)$)，可以窮舉真值表來證明。



#### Table - 換質換位命題的真值表

| $p$  | $q$  | $\neg q \rightarrow \neg p$ | $p \rightarrow q$ |
| ---- | ---- | --------------------------- | ----------------- |
| 0    | 0    | 1                           | 1                 |
| 0    | 1    | 1                           | 1                 |
| 1    | 0    | 0                           | 0                 |
| 1    | 1    | 1                           | 1                 |



#### Definition - 換質命題

令 $p$ 與 $q$ 為一個命題

則一條件敘述 $\neg p \rightarrow \neg q$ 稱作換質命題，與換位命題(也就是，$(q \rightarrow p) \leftrightarrow (\neg p \rightarrow \neg q)$)邏輯等價，可以窮舉真值表來證明。



#### Table - 換質命題的真值表

| $p$  | $q$  | $\neg p \rightarrow \neg q$ |
| ---- | ---- | --------------------------- |
| 0    | 0    | 1                           |
| 0    | 1    | 0                           |
| 1    | 0    | 1                           |
| 1    | 1    | 1                           |



#### Definition - 若且為若

令 $p$ 與 $q$ 為一個命題

則一條件敘述$p \leftrightarrow q$稱作若且為若

若$p$與$q$皆True，或$p$與$q$皆False，則$p\leftrightarrow  q$為True，否則為False。



#### Table - 若為且若的真值表

| $p$  | $q$  | $p \leftrightarrow q$ |
| ---- | ---- | --------------------- |
| 0    | 0    | 1                     |
| 0    | 1    | 0                     |
| 1    | 0    | 0                     |
| 1    | 1    | 1                     |



### 1.2 邏輯命題應用

#### Example

How can this English sentence be translated into a logical expression?

"You can access the Internet from campus only if you are a computer science major or you are not a freshman."



Let $A$ can access the internet from compus, $B$ are a computer science major, and $C$ are a freshman.

So that the English sentence be translated into $A \rightarrow (B \or \neg C)$



### 1.3 命題等價

#### Introduce - 恆真式

恆真式代表複合命題恆為true。



##### Example

$(p \or \neg p)$

無論$p$是True或者False，他都恆為True，稱為tautology(恆真式)



#### Introduce - 矛盾式

矛盾式代表負和命題恆為false。



##### Example

$(p \and \neg p)$

無論$p$是True或者False，他都恆為False，稱為contradiction



#### Definition - 邏輯等價

令$p$和$q$為複合命題，邏輯等價的定義為$p \leftrightarrow q$為恆等式，寫作$p \equiv q$



##### Example 

證明$p \rightarrow q$和$\neg p \or q$為邏輯等價。



我們可以窮舉真值表，來證明兩者為邏輯等價

令$A = p \rightarrow q$，$B = \neg p \or q$，則

| $p$  | $q$  | $A = p \rightarrow q$ | $B = \neg p \or q$ | $A \leftrightarrow B$ |
| ---- | ---- | --------------------- | ------------------ | --------------------- |
| 0    | 0    | 1                     | 1                  | 1                     |
| 0    | 1    | 1                     | 1                  | 1                     |
| 1    | 0    | 0                     | 0                  | 1                     |
| 1    | 1    | 1                     | 1                  | 1                     |



#### Recall - 德摩根定律

$\neg (p \and q) \equiv \neg p \or \neg q$

$\neg (p \or q) \equiv \neg p \and \neg q$



##### Example 2

證明 $\neg (p \or q)$ 與 $\neg p \and \neg q$ 邏輯等價。



設$A=\neg(p \or q)$，$B = \neg p \and \neg q$

我們可以窮舉真值表，來證明兩者為邏輯等價

| $p$  | $q$  | $A=\neg(p \or q)$ | $B = \neg p \and \neg q$ | $A \leftrightarrow B$ |
| ---- | ---- | ----------------- | ------------------------ | --------------------- |
| 0    | 0    | 1                 | 1                        | 1                     |
| 0    | 1    | 0                 | 0                        | 1                     |
| 1    | 0    | 0                 | 0                        | 1                     |
| 1    | 1    | 0                 | 0                        | 1                     |



##### Example 3

證明 $p \rightarrow q$ 和 	$\neg p \or q$ 邏輯等價。



設$A = p \rightarrow q$，$B = \neg p \or q$

我們可以窮舉真值表，來證明兩者為邏輯等價。

| $p$  | $q$  | $A = p \rightarrow q$ | $B = \neg p \or q$ | $A \leftrightarrow B$ |
| ---- | ---- | --------------------- | ------------------ | --------------------- |
| 0    | 0    | 1                     | 1                  | 1                     |
| 0    | 1    | 1                     | 1                  | 1                     |
| 1    | 0    | 0                     | 0                  | 1                     |
| 1    | 1    | 1                     | 1                  | 1                     |



##### Example 4

證明 $p \or (q \and r)$ 和 $(p \or q) \and (p \and r)$ 邏輯等價。



我們可以窮舉真值表，來證明兩者為邏輯等價。

| $p$  | $q$  | $r$  | $(q \and r)$ | $(p \or q)$ | $(p \and r)$ | $p \and (q \or r)$ | $(p \and q) \and (p \and r)$ | $p \and (q \or r) \leftrightarrow (p \and q) \and (p \and r)$ |
| ---- | ---- | ---- | ------------ | ----------- | ------------ | ------------------ | ---------------------------- | ------------------------------------------------------------ |
| 0    | 0    | 0    | 0            | 0           | 0            | 0                  | 0                            | 1                                                            |
| 0    | 0    | 1    | 0            | 0           | 0            | 0                  | 0                            | 1                                                            |
| 0    | 1    | 0    | 0            | 1           | 0            | 0                  | 0                            | 1                                                            |
| 0    | 1    | 1    | 1            | 1           | 0            | 0                  | 0                            | 1                                                            |
| 1    | 0    | 0    | 0            | 1           | 0            | 0                  | 0                            | 1                                                            |
| 1    | 0    | 1    | 0            | 1           | 0            | 0                  | 0                            | 1                                                            |
| 1    | 1    | 0    | 0            | 1           | 0            | 0                  | 0                            | 1                                                            |
| 1    | 1    | 1    | 1            | 1           | 1            | 1                  | 1                            | 1                                                            |



#### Recall - 衡等律

$p \and T \equiv p$

$p \or F \equiv p$



#### Recall - 支配律

$p \and F \equiv F$

$p \or T \equiv T$



#### Recall - 冪等律

$p \and p \equiv p$

$p \or p \equiv p$



#### Recall - 雙非律

$\neg(\neg p) \equiv p$



#### Recall - 交換律

$p \and q \equiv q \and p$

$p \or q \equiv q \or p$



#### Recall - 結合律

$(p \or q) \or r \equiv p \or (q \or r)$

$(p \and q) \and r \equiv p \and (q \and r)$



#### Recall - 分配律

$p \and (q \or r) \equiv (p \and q) \or (p \and r)$

$p \or (q \and r) \equiv (p \or q) \and (p \or r)$



#### Recall - 吸收律

$p \or (p \and q) \equiv p$

$p \and (p \or q) \equiv p$



#### Recall - 否定律

$p \and \neg p \equiv F$

$p \or \neg p \equiv T$



#### Recall - 一些有關實質蘊含的邏輯等價

$p \rightarrow q \equiv \neg p \or q$

$p \rightarrow q \equiv \neg q \rightarrow \neg p$

$p \or q \equiv \neg p \rightarrow q$

$p \and q \equiv \neg(p \rightarrow \neg q)$

$\neg(p \rightarrow q) \equiv p \and \neg q$

$(p \rightarrow q) \and (p \rightarrow r) \equiv p \rightarrow (q \and r)$

$(p \rightarrow r) \and (q \rightarrow r) \equiv (p \and q) \rightarrow r$

$(p \rightarrow q) \and (p \rightarrow r) \and p \rightarrow (q \or r)$

$(p \rightarrow r) \or (q \rightarrow r) \equiv (p \and q) \rightarrow r$



#### Recall - 一些有關若為且若的邏輯等價

$p \leftrightarrow q \equiv (p \rightarrow q) \and (q \rightarrow p)$

$\displaystyle p \leftrightarrow q \equiv \neg p \leftrightarrow \neg q$

$p \leftrightarrow q \equiv (p \and q) \or (\neg p \and \neg q)$

$\neg(p \leftrightarrow q) \equiv p \leftrightarrow \neg q$



#### Introduce - 建構新的邏輯等價

如果$p$與$q$邏輯等價，且$q與r$邏輯等價，那麼我們就可以說$p$與$r$邏輯等價。



##### Example 1

證明 $\neg (p \rightarrow q) \equiv p \and \neg q$ 邏輯等價



首先，$p \rightarrow q \equiv \neg p \or q$，所以$\neg (p \rightarrow q) \equiv \neg(\neg p \or q) \equiv p \and \neg q$

因此$\neg (p \rightarrow q) \equiv p \and \neg q$，證畢



##### Example 2

利用一連串的邏輯等價，證明 $\neg (p \or (\neg p \and q)) \equiv \neg p \and \neg q$



利用德摩根定律，得到$\neg (p \or (\neg p \and q)) \equiv \neg p \and \neg(\neg p \and q)$

再次利用德摩根定律，得到$\neg p \and \neg(\neg p \and q) \equiv \neg p \and(p \or \neg q)$

利用分配律，$\neg p \and(p \or \neg q) \equiv (p \and \neg p) \or (\neg p \and \neg q) \equiv F \or (\neg p \and \neg q) \equiv (\neg p \and \neg q)$

因此，$\neg (p \or (\neg p \and q)) \equiv \neg p \and \neg q$，證畢



##### Example 3

證明 $(p \and q) \rightarrow (p \or q)$為恆等式



利用$p \rightarrow q \equiv \neg p \or q$的特性，改寫為$(p \and q) \rightarrow (p \or q) \equiv \neg(p \and q) \or (p \or q)$

利用德摩根定律，改寫為$\neg(p \and q) \or (p \and q) \equiv (\neg p \or \neg q) \or (p \or q)$

利用交換律，$(\neg p \or p) \or(\neg q \or q) \equiv T \or T \equiv T$

故$(p \and q) \rightarrow (p \or q)$為恆等式，證畢。



#### Introduce - 滿足命題

滿足命題的定義是，若有一個複合命題$P$，若能找到一組變數能夠使$P$為true，則$P$能夠被滿足。



##### Example

判斷以下三個複合命題$P$是否能夠被滿足。

1. $(p \and \neg q) \or (q \and \neg r) \and (r \or \ \neg p)$
2. $(p \and q \and r) \or (\neg p \and \neg q \and \neg r)$
3. $(p \or \neg q) \and (q \or \neg r) \and (r \or \neg p) \and (p \or q \or r) \and (\neg p \or \neg q \or \neg r)$



第一個命題：若$p,q,r$其中有一個是true，則可以滿足命題：。

第二個命題：若$p,q,r$都為true或者都為false，則可以滿足命題。

第三個命題：

考慮到

$(p \or \neg q) \and (q \or \neg r) \and (r \or \neg p)$必須要是true，則$p, q, r$都必須要是true，或者$p, q, r$都必須要是false。

$(p \or q \or r) \and (\neg p \or \neg q \or \neg r)$必須要是true，則$p, q, r$都不能是true，或者都不能是false。

因此，兩者矛盾，故$(p \or \neg q) \and (q \or \neg r) \and (r \or \neg p) \and (p \or q \or r) \and (\neg p \or \neg q \or \neg r)$不能被滿足。



### 1.4 謂語和限定詞

#### Introduce - 謂語

命題是具有真假意義的陳述句，而陳述句是由主語與謂語所組成的。

例如我們可以說

1. 阿軒是北科大的學生
2. 阿哲不是北科大的學生

則我們假設$P(x)$為：$x$是北科大的學生

在這個範例中，$P(x)$為謂語，$x$為主語，當$x$被賦予值，則$P(x)$則成為一個命題。

因此則上面兩句分別可以寫成$P($阿軒$)$與$P($阿哲$)$，所得到的結果分別為true與false。



##### Example 1

若$P(x)$代表$x > 3$，求真值$P(2)$與$P(4)$



$P(2)$等於$2>3$，則$P(2)$的真值為false。

$P(4)$等於$4 > 3$，則$P(4)$的真值為true。



##### Example 2

若$A(x)$代表「電腦$x$正在被入侵者攻擊」，且我們假設正在被入侵者攻擊的電腦為$CS2$與$MATH1$

則求真值$A(CS1)$與$A(CS2)$，以及$A(MATH1)$



我們可以很清楚的知道，$CS2$與$MATH1$正在被攻擊，因此我們可以知道$A(CS2) = T$，$A(MATH1) = T$

而$CS1$沒有被攻擊，故$A(CS1) = F$



##### Example 3

若$Q(x, y)$代表敘述$x = y + 3$，則求真值$Q(1, 2)$與$Q(3, 0)$



$Q(1, 2) \Rightarrow 1 \neq 2 + 3 \Rightarrow Q(1, 2) = F$

$Q(3, 0) \Rightarrow 3 = 0 + 3 \Rightarrow Q(3, 0) = T$



##### Example 4

令$A(c, n)$代表「電腦$c$連接著網路$n$」，其中$c$代表電腦而$n$代表著網路，假設$MATH1$正在連接著網路$CAMPUS2$而不是$CAMPUS1$，求$A(MATH1, CAMPUS1)$與$A(MATH1, CAMPUS2)$的真值。



因為$MATH1$沒有連接著網路$CAMPUS1$，因此$A(MATH1, CAMPUS1)$為false

而$MATH1$連接著網路$CAMPUS2$因此$A(MATH1, CAMPUS2)$為true



##### Example 5

令$R(x, y, z)$代表$x + y = z$，求真值$R(1, 2, 3)$與$R(0, 0, 1)$



因為$R(1, 2, 3)$代表$1 + 2 = 3$，因此$R(1, 2, 3)$為true。

因為$R(0, 0, 1)$代表$0 + 0 = 1$，因此$R(0, 0, 1)$為false。



