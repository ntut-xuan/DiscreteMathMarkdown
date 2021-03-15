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



##### Table - 邏輯非的真值表

![image-20210115200649258](https://i.imgur.com/inKIp7g.png)

#### Definition - 邏輯與

令$p$與$q$為命題，$p$與$q$的邏輯與，我們表示為$p \and q$，念作"$p$ and $q$"。

當$p$與$q$都為True時，$p \and q$才會true，反之為false。



##### Example

Find the conjunction of the propositions $p$ and $q$ where $p$ is the proposition “Rebecca’s PC has more than 16 GB free hard disk space” and $q$ is the proposition “The processor in Rebecca’s PC runs faster than 1 GHz.”



The conjunction of the propositions $p$ and $q$ is 

"Rebecca’s PC has more than 16 GB free hard disk space, and the processor in Rebecca’s PC runs faster than 1 GHz."



##### Table - 邏輯與的真值表

![image-20210115201510053](https://i.imgur.com/p2VL2Fy.png)



#### Definition - 邏輯或

令$p$與$q$為命題，$p$與$q$的邏輯或，我們表示為$p \or q$，念作"$p$ or $q$"。

當$p$與$q$都為false時，$p \or q$為false，反之為true。



##### Example

What is the disjunction of the propositions p and q where p and q are the same propositions as in Example 5?



The disjunction of the propositions p and q is

"Rebecca’s PC has more than 16 GB free hard disk space, or the processor in Rebecca’s PC runs faster than 1 GHz."



##### Table - 邏輯或的真值表

![image-20210115201526194](https://i.imgur.com/EHoHvII.png)



#### Definition - 邏輯異或

令$p$與$q$為命題，$p$與$q$的邏輯異或，我們表示為$p \oplus q$。

當$p$或$q$都同為true或同為false時，$p \oplus q$為false，反之為true。



#### Definition - 實質蘊涵

令$p$與$q$為命題，$p$與$q$的 實質蘊涵，我們表示為$p \rightarrow q$，表示若$p$則$q$。

當$p$為true且$q$為false時，則$p \rightarrow q$為false，否則為true。

在實質蘊涵中的$p$，我們稱作前件，而$q$我們稱作後件



##### Table - 實質蘊涵的真值表

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



##### Table - 換質換位命題的真值表

| $p$  | $q$  | $\neg q \rightarrow \neg p$ | $p \rightarrow q$ |
| ---- | ---- | --------------------------- | ----------------- |
| 0    | 0    | 1                           | 1                 |
| 0    | 1    | 1                           | 1                 |
| 1    | 0    | 0                           | 0                 |
| 1    | 1    | 1                           | 1                 |



#### Definition - 換質命題

令 $p$ 與 $q$ 為一個命題

則一條件敘述 $\neg p \rightarrow \neg q$ 稱作換質命題，與換位命題(也就是，$(q \rightarrow p) \leftrightarrow (\neg p \rightarrow \neg q)$)邏輯等價，可以窮舉真值表來證明。



##### Table - 換質命題的真值表

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



##### Table - 若為且若的真值表

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



#### Introduce - 量化

量化用來決定一個謂詞，在一定的事物上成立的程度。

產生量化的語言叫作量詞。



舉個例子，「我**所有**的玻璃都破了」，「**大量**的人是聰明的」。

通常來說，有兩種量化的類型：全稱量化、存在量化



#### Definition - 全稱量化

對於$P(x)$來說，全稱量化的代表對於所有在$P$的定義域內的$x$，我們可以寫作$\forall x P(x)$

$\forall$符號代表全域量詞，我們把$\forall x P(x)$讀作"for all $x, P(x)$" 或者"for every $x, P(x)$"。

若存在一個$x$，使得$P(x)$為false，則我們把他稱作$\forall x P(x)$的反例。



##### Table - 量化類別

| 敘述             | 什麼時候為true                                  | 什麼時候為false                                  |
| ---------------- | ----------------------------------------------- | ------------------------------------------------ |
| $\forall x P(x)$ | 對於所有在$P(x)$定義域中的$x$，$P(x)$都為true。 | 存在一個$x$使得$P(x)$為false                     |
| $\exist x P(x)$  | 存在一個$x$使得$P(x)$為true                     | 對於所有在$P(x)$定義域中的$x$，$P(x)$都為false。 |



##### Example 1

令$P(x)$代表$x + 1 > x$，對於所有實數域中的$x$，$\forall x P(x)$的真值為何



我們可以清楚知道，對於所有實數域中的$x$，$x+1$都大於$x$，找不到一個反例使的$x + 1 < x$，因此$\forall x P(x)$的真值為true。



##### Example 2

令$Q(x)$代表$x < 2$，對於所有實數域中的$x$，$\forall x P(x)$的真值為何



當$Q(0), Q(1)$的時候$Q(x)$為true，但$Q(2)$為false，故$\forall x P(x)$為false。



##### Example 3

令$P(x)$代表$x^2 < 10$，求所有不超過4的正整數中，$\forall x P(x)$的真值為何



我們可以把真值表達成$P(1) \and P(2) \and P(3) \and P(4)$

但是$P(4)$為false，因為$4^2 < 10$

所以$\forall x P(x)$為false。



##### Example 4

令$P(x)$代表$x^2 \ge x$，若$x$的定義域為所有實數，則$\forall x P(x)$的真值為何？

若$x$的定義域為所有整數，那麼$\forall x P(x)$的真值又為何？



我們可以找到一個反例，若$x = 0.5$，則$0.5^2 < 0.5$。

故若$x$的定義域為所有實數，則$\forall x P(x)$的真值為false。

但若$x$的定義域為所有整數，我們找不到任何一個反例能夠證明$\forall x P(x)$的真值為false。

故若$x$的定義域為所有整數，$\forall x P(x)$的真值為true。



#### Definition - 存在量化

對於$P(x)$來說，存在量化的代表對於至少一個在$P$的定義域內的$x$，我們可以寫作$\exist x P(x)$，$\exist$符號代表存在量詞

若不存在一個$x$，使得$P(x)$為true，則我們把他稱作$\exist x P(x)$的反例。



##### Example 1

令$P(x)$代表$x > 3$，若$x$的定義域為所有實數，則$\exist x P(x)$的真值為何？



我們可以找到$x = 4$使得$x > 3$成立，故$\exist x P(x)$的真值為true。



##### Example 2

令$Q(x)$代表$x = x+1$，若$x$的定義域為所有實數，則$\exist x Q(x)$的真值為何？



我們找不到任何一個實數，使得$x = x + 1$，故$\exist x Q(x)$為false。



##### Example 3

令$P(x)$代表$x^2 > 10$，若$x$的定義域為不超過4的正整數，則$\exist x P(x)$的真值為何？



我們可以知道$x \in \{1, 2, 3, 4\}$

所以我們可以寫成$P(1) \or P(2) \or P(3) \or P(4)$

由於我們可以知道，$4^2 = 16 > 10$ ，因此$P(4)$為true

故$P(1) \or P(2) \or P(3) \or P(4)$為true

因此$\exist x P(x)$為true



#### Introduce - 唯一量化

我們可以使用$\exist !xP(x)$，用來表示「唯一一個」、「正好一個」、「剛好一個」$x$使得$P(x)$為真。

例如，令$P(x)$代表$x - 2 = 4$，則$\exist ! xP(x)$成立，因為我們可以找到$x = 6$，使得$P(6)$為true

除此之外我們找不到任何的$x$，使得$P(x)$為true，故$\exist ! xP(x)$為true。



#### Introduce - 限定定義域的量詞

通常來說， 我們可以透過縮寫，來表示定義域所需要符合的條件。

例如說$\forall x > 0 (x^2 > x)$，且定義域為所有實數，則代表說，對於所有大於0的實數，使得$x^2 > x$。



##### Example 

若下列敘述的定義域皆為$x \in \mathbb{R}$，求$\forall x < 0 (x^2 > 0)$，$\forall y \neq 0 (y^3 \neq 0)$，還有$\exist z > 0 (z^2 = 2)$的意義。



第一個例子，若$x < 0$，則$x^2 > 0$，則我們可以寫成$(x < 0) \rightarrow (x^2 > 0)$

且所有的實數$x$都要符合這個敘述，因此$\forall x[(x < 0) \rightarrow (x^2 > 0)]$

第二個例子，若$y \neq 0$，則$y^3 \neq 0$，則我們可以寫成$(y \neq 0) \rightarrow (y^3 \neq 0)$

且所有的實數$y$都要符合這個敘述，因此$\forall y[(y\neq 0) \rightarrow (y^3\neq 0)]$

第三個例子，若$z > 0$，則$z^2 = 2$，則我們可以寫成$(z > 0) \and (z^2 = 2)$

且至少一個$z$都要符合這個敘述，因此$\exist z[(z > 0) \and (z^2 = 2)]$



##### Introduce - 量詞的優先級

$\forall$與$\exist$是所有邏輯符號中優先級最高的，也就是若$\forall x P(x) \or Q(x)$，他代表著$(\forall x P(x)) \or Q(x)$，而非$\forall x (P(x) \or Q(x))$



#### Introduce - 綑綁變數

如果量詞用在變數$x$上，則我們說變數$x$為一個綑綁變數，否則他就是自由變數。

一個命題函數所有變數都必須為綑綁變數，則這個命題變數才會變成一命題。

無論是存在量化、全稱量化都可以使用



##### Example 1

在敘述$\exist x (x + y = 1)$中，我們可以知道$x$是綑綁變數，因為前面的存在量詞是對$x$的

但是沒有任何對$y$的量化，因此$y$為一個自由變數。



##### Example 2

在敘述$\exist x(P(x) \and Q(x)) \or \forall x R(x)$，所有的變數都是綑綁變數

第一個存在量詞對括號內所有的$x$進行綑綁，而第二個存在量詞對命題函數$R$的變數$x$進行綑綁。



##### Example 3

在敘述$\exist x(P(x) \and Q(x)) \or \forall y R(y)$，所有變數都是綑綁變數

第一個存在量詞對括號內所有的$x$進行綑綁，而第二個存在量詞對命題函數$R$的變數$y$進行綑綁。



#### Introduce - 關於量化的邏輯等價

##### Definition - 量化的邏輯等價

關於量詞與謂語的邏輯等價，若兩邊敘述若為且若擁有相同的真值，則我們稱他為邏輯等價。

不用考慮謂語如何替代敘述，或者在命題函數中的定義域為何。



##### Example

證明$\forall x (P(x) \and Q(x))$與$\forall P(x) \and \forall Q(x)$邏輯等價。



若要證明$\forall x (P(x) \and Q(x))$與$\forall P(x) \and \forall Q(x)$邏輯等價

則我們假設$a \in D(x)$，其中$D(x)$代表$x$的定義域，那麼如果$\forall x (P(x) \and Q(x))$是true，則$P(a) \and Q(a)$都為true。

達成與邏輯為正的條件即為$P(a)$與$Q(a)$皆為true，則與邏輯才會成立。

接著，假設$\forall x P(x) \and \forall x Q(x)$為true，且$a \in D(x)$

那麼為了達成與邏輯的條件，$P(a)$應為true，$Q(a)$也應為true。

故$P(a) \and Q(a)$應為true，而$a \in D(x)$，則代表所有在$D(x)$的變數$a$都可以使得$P(a) \and Q(a)$為true

故我們可以把$a$改寫成$\forall x (P(x) \and Q(x))$

因此，我們可以得知，$\forall x (P(x) \and Q(x))$與$\forall x P(x) \and \forall x Q(x)$邏輯等價。



#### Introduce - 邏輯非的量化表達式

##### Introduce - 全稱量化的邏輯非

思考以下的敘述

「在這間教室所有人都修過微積分」

若我們利用謂語取代敘述的部分，則我們可以令$P(x)$為「$x$修過微積分」，而$x$的定義域限定為在這間教室的人

故敘述可以表達成$\forall x P(x)$



而若不是所有人都修過微積分，則必定在教室有一個人$x$使得$P(x)$為false。

因此，我們可以表達成，若不是所有人都修過微積分，則我們可以用存在量化來表示

也就是$\exist x \neg P(x)$



因此，我們可以知道，$\neg(\exist x \neg P(x)) \equiv \forall x P(x)$

兩邊邏輯等價同取邏輯非，則$\neg \neg (\exist x \neg P(x)) \equiv \neg \forall x P(x)$

也就是$\exist x \neg P(x) \equiv \neg \forall x P(x)$



##### Introduce - 存在量化的邏輯非

思考以下敘述

「在這間教室，至少有一個人修過微積分」

若我們利用謂語取代敘述的部分，則我們可以令$P(x)$為「$x$修過微積分」，而$x$的定義域限定為在這間教室的人

故敘述可以表達成$\exist x P(x)$



而若不是至少有一個人修過微積分，則必定在定義域內所有的$x$都能使$\exist x P(x)$為false。

因此，我們可以表達成，若沒有人修過微積分，則我們可以用全稱量化來表示

也就是$\forall x \neg P(x)$



因此我們可以知道，$\neg(\forall x \neg P(x)) \equiv \exist x P(x)$

兩邊邏輯等價同取邏輯非，則$\neg \neg(\forall x \neg P(x)) \equiv \neg \exist x P(x)$

也就是$\forall x \neg P(x) \equiv \neg \exist x P(x)$



##### Table - 量化表達式的德摩根定律

| 量化表達式       | 取邏輯非後的量化表達式 |
| ---------------- | ---------------------- |
| $\forall x P(x)$ | $\exist x \neg P(x)$   |
| $\exist x P(x)$  | $\forall x \neg P(x)$  |



##### Example

求$\forall x(x^2 > x)$與$\exist x (x^2=2)$的反邏輯。



對於所有的$x$，$x^2 > x$皆成立

而他的反邏輯即為存在一個$x$使得$x^2 > x$不成立

故我們可以寫成存在一個$x$使得$x^2 \le x$

因此，$\neg \forall x(x^2 > x) \equiv \exist x (x^2 \le x)$



存在一個$x$使得$x^2 = 2$成立

而他的反邏輯即為使所有的$x$讓$x^2 = 2$不成立

故我們可以寫成讓所有的$x$使得$x^2 \neq 2$

因此，$\neg \exist x (x^2 = 2) \equiv \forall x (x^2 \neq 2)$

$x$的值取決於定義域。



### 1.5 嵌套限定詞

#### Introduce - 嵌套量詞

在1.4的章節，我們通常都只會用到一個量詞，而量詞是可以被嵌套的。

舉個例子，就像這樣：$\forall x \exist y (x + y = 0)$，一層一層套上的量詞

而我們也可以改個表達方式，令$Q(x)$為$\exist y P(x, y)$，而$P(x, y)$為$x+y = 0$

則利用$\forall x Q(x)$，就能表達$\forall x \exist y (x + y = 0)$

也就能表達在定義域$D(x)$內的所有$x$，都存在一個$y \in D(y)$使得$x + y = 0$



#### Introduce - 嵌套量詞的順序

##### Example 1

若我們考慮$\forall x \forall y (x + y = y + x)$，則他唸起來會像

「對於每一對的$(x, y)$，$\forall x \forall y (x + y = y + x)$均成立。」

而若我們變換一下順序，寫作$\forall y \forall x (x + y = y + x)$，則他唸起來會像

「對於每一對的$(y, x)$，$\forall y \forall x (x + y = y + x)$均成立。」

因此，我們可以知道，兩個不同的全稱量詞對換是不會影響命題本身的。



##### Example 2

1. 若我們考慮$\exist x \forall y(x + y = 0)$，且$x, y$的定義域為所有實數

   則他唸起來會像，存在一個$x$，使得每一種$y$都能符合$x + y = 0$

   這個命題很明顯是false，因為不存在任何一個$x$，使得每一種$y$都能符合$x + y = 0$。

2. 若我們考慮$\forall x \exist y (x + y = 0)$，且$x, y$的定義域為所有實數

   則他唸起來會像，對於每一個屬於實數的$x$，存在一種$y$能符合$x + y = 0$

   這個命題就會是true，因為只要使$y = -x$，就能使敘述成立。

因此，兩者對調是會影響命題本身的。



##### Example 3

令$Q(x, y, z)$代表敘述$x + y = z$，若$x, y, z$的定義域為所有實數，試求$\forall x \forall y \exist z Q(x, y, z)$和$\exist z \forall x \forall y Q(x, y, z)$的真值。

1. 若我們考慮$\forall x \forall y \exist z Q(x, y, z)$，則他唸起來會像，對於所有的$x$與所有的$y$，存在一個$z$，使得$x + y = z$

   這樣是合理的，無論$x$與$y$的值為多少，兩個實數相加必定為另一個實數，故$\forall x \forall y \exist z Q(x, y, z)$的真值為true

2. 若我們考慮$\exist z \forall x \forall y Q(x, y, z)$，則他唸起來會像，存在一個$z$使得對於所有的$(x, y)$，都能符合$x + y = z$

   這樣是不合理的，因為找不到一種$z$，使得任意的$(x, y)$對符合$x + y = z$，故$\exist z \forall x \forall y Q(x, y, z)$的真值為false
   

綜合上述，兩者的量詞互換，會影響到命題的結果。



##### Table - 兩個嵌套量詞的意義

![image-20210304225538828](https://i.imgur.com/Aqo4GLE.png)



#### Introduce - 嵌套量詞的負邏輯

負邏輯一樣可以用在嵌套量詞上。

##### Example 

請找出$\forall x \exist y (xy = 1)$的負邏輯命題



命題翻譯會變成，對於所有的$x$，存在一個$y$使得$xy = 1$

那麼對於這個命題加上負邏輯，則變成了存在一個$x$，使得所有可能的$y$，讓$xy = 1$不成立。

故我們可以寫成$\exist x \forall y \neg(xy = 1)$

而$\neg(xy = 1)$又可以寫成$(xy \neq 1)$

故整個式子可以寫成$\exist x \forall y (xy \neq 1)$



### 1.6 推論規則

#### Introduce - 肯定前件

若$P \equiv T$，且$P \rightarrow Q \equiv T$，則$Q \equiv T$



##### Example

你考到了100分。

若你考到100分，就會得到A。

所以，你會得到A。



#### Introduce - 否定後件

若$\neg Q \equiv T$，且$P \rightarrow Q \equiv T$，則$\neg P \equiv T$



##### Example

你沒有得到A。

若你考到100分，就會得到A。

所以你沒有考到100分。



#### Introduce - 三段論證

若$P \rightarrow Q \equiv T$，且$Q \rightarrow R \equiv T$，則$P \rightarrow R \equiv T$



##### Example

若你難過，就吃東西

若你吃東西，就可能會變胖

所以你難過就可能會變胖。



#### Introduce - 選言三段論

若$P \or Q \equiv T$，且$\neg P \equiv T$，則$Q \equiv T$



##### Example

我要嘛選擇睡覺，要嘛選擇讀書。

我沒在睡覺。

所以我在讀書。



#### Introduce - 添加律

若$P \equiv T$，則$P \or Q \equiv T$



##### Example

若我在睡覺。

所以我可能在睡覺或者在讀書。



#### Introduce - 簡化律

若$P \and Q  \equiv T$，則$P \equiv T$



##### Example

外面是晚上而且外面在下雨

所以外面是晚上。



#### Introduce - 連言

若$P \equiv T$，且$Q \equiv T$，則$P \and Q \equiv T$



##### Example

外面是晚上。

外面在下雨。

所以外面是晚上，而且外面在下雨。



#### Introduce - 預解律

若$P \or Q \equiv T$，且$\neg P \or R \equiv T$，則$Q \or R \equiv T$



##### Example

外面是晚上或者外面在下雨。

且外面是白天或者外面在放晴。

則外面在下雨或者外面在放晴。



#### Introduce - 全稱實例化

若$\forall x P(x) \equiv T$，則若$c \in D(x)$，則$P(c) \equiv T$



##### Example

所有資工系的學生都修過微積分

若小碩是資工系的學生

則小碩修過微積分



#### Introduce - 全稱普遍化

若$c \in D(x)$，且$P(c) \text{ for an arbitrary c}$，則$\forall x P(x) \equiv T$



##### Example

若小碩是資工系的學生

所有資工系的學生都修過微積分

則小碩修過微積分



#### Introduce - 存在實例化

若$\exist x P(x) \equiv T$，則$P(c) \equiv T \text{ for some element c}$



#### Introduce - 存在普遍化

若$P(c) \equiv T \text{ for some element c}$，則$\exist x P(x) \equiv T$



### 1.7 Introduce to proof

#### Introduce - 定理

定理是一個可以被證明的敘述。



#### Introduce - 公理

公理是一個不需要證明，假設正確的敘述。



##### Example

$\forall x,y \in \mathbb{R}$，$x + y \in \mathbb{R}$是一個公理。



#### Introduce - 引理

引理是較不重要的敘述，用來協助證明其他的結果。



#### Introduce - 系理

系理是一個定理，由另一個定理推導出另一個顯而易見的定理。



#### Introduce - 猜想/假說

猜想(假說)是一個定理，被提出但沒有人能夠證明正確與否。



##### Example

費馬大定理：$x^n + y^n = z^n$

當$n \in \mathbb{Z}$且$n > 2$時，$(x, y, z)$沒有整數解。



#### Example

試證明，若$n \in odd$，則$n^2 \in odd$

我們可以寫成$\forall n (P(n) \rightarrow Q(n))$，$P(n)$代表$n$是奇數，而$Q(n)$代表$n^2$是奇數。

假設$n \in odd$，則$n = 2k+1, k \in \mathbb{Z}$

則$n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$

則我們可以知道$2k^2+2k$必定是某個整數

由於偶數乘以任何整數均為偶數，故偶數+1必為奇數

故$n^2$必為奇數。



#### Introduce - 反證法

若$P \rightarrow Q$證明較為困難，則證明與$P \rightarrow Q$等價的$\neg Q \rightarrow \neg P$。



##### Example

試證明，若$n \in \mathbb{Z}$，且$3n + 2$是奇數，則$n$是奇數。



我們可以寫成$\forall n (P(n) \rightarrow Q(n))$，$P(n)$代表$3n+2$是奇數，$Q(n)$代表$n$是奇數。

則我們利用反證法，證明$\forall n(\neg Q(n) \rightarrow \neg P(n))$，也就是證明對於所有的整數$n$，若$n$是偶數，則$3n+2$是偶數。

則$n$可以寫成$2k$的形式，因此$3n + 2 = 6k + 2$，$k \in \mathbb{Z}$

由於偶數乘以任何整數均為偶數，且偶數加上任何偶數均為偶數

故我們可以證明，若$n$是偶數，則$3n+2$是偶數。

故若$n \in \mathbb{Z}$，且$3n + 2$是奇數，則$n$是奇數。



#### Introduce - 空泛證明

若$P \equiv F$，則證明完成。



##### Example

試證明，如果$0 > 1$，則$0^2 > 0$



我們可以寫成$P \rightarrow Q$，其中$P$為$0 > 1$，且$Q$為$0^2 > 0$

但$P \equiv F$，則$Q$不可能發生，證畢。



#### Introduce - 平庸證明

若$Q \equiv T$，則證明完成。



##### Example

設$a, b \in \mathbb{Z}$，若$a \ge b$，則$a^0 \ge b^0$



我們可以寫成$\forall a \forall b(P(a, b) \rightarrow Q(a,b))$，其中$P(a, b)$為$a \ge b$，且$Q(a, b)$為$a^0 \ge b^0$

則由於無論$a, b$為何，$a^0 = b^0$，故$\forall a \forall b Q(a, b) \equiv T$，故$\forall a \forall b(P(a, b) \rightarrow Q(a,b)) \equiv T$



#### Introduce - 歸謬證明法

有兩種用途

| 用途                      | 假設                          | 矛盾                            |
| ------------------------- | ----------------------------- | ------------------------------- |
| $P$ is true               | $\neg P$ is true              | $\neg P \rightarrow F$          |
| $P \rightarrow Q$ is true | $P$ is true, $\neg Q$ is true | $(P \and \neg Q) \rightarrow F$ |



### 1.8 Exhaustive Proof

#### Example 1

$(n + 1)^3 \ge 3$，$n \in \mathbb{Z}^+, n \le 4$



若$n = 1$，則$2^3 = 8 \ge 3$，

若$n = 2$，則$3^3 = 27 \ge 3$

若$n = 3$，則$4^3 = 64 \ge 3$

若$n = 4$，則$5^3 = 125 \ge 3$

故$(n + 1)^3 \ge 3$成立。



#### Example 2

若$n \in \mathbb{Z}$，則$n^2 \ge n$



設$\forall n P(n)$代表對於所有實數$n$，$n^2 \ge n$

分成三個case分開做處理。

$n = 0$，$0 = 0$，故$P(0)$成立。

$n \ge 1$，已知$n \ge 1$，則兩邊同乘以$n^2 \ge n$，故$n^2 \ge n$成立。

$n \le 1$，已知$n^2 \ge 0$，故$n^2 \ge n$

故$\forall n P(n)$成立



#### Introduce - 建構式證明

建構式證明可以分成存在證明或不存在證明。



##### Example 1

請證明可以找到一個整數，這個整數可以用兩個以上不同的立方和所組成。



我們可以找到一個數字$1729$，且$1729 = 10^3 + 9^3$且$1729 = 12^3 + 1^3$，故證明完畢。



##### Example 2

請證明可以找到一個無理數$x$與$y$，使得$x^y$為有理數。



分成兩個case

若$\sqrt{2}^\sqrt{2}$是有理數，則$x = \sqrt{2}, y = \sqrt{2}$

若$\sqrt{2}^\sqrt{2}$是無理數，則$x = \sqrt{2}^\sqrt{2}, y = \sqrt{2}$，$x^y = \sqrt{2}^{\sqrt{2}\cdot \sqrt{2}} = \sqrt{2}^2 = 2$

則這兩者其中之一可以符合命題。



#### Introduce - 存在證明

存在一個$x$，使得$P(x)$為true，且除了$x$以外的$y$，使得$P(x)$為false。

$\exist x (P(x) \and \forall y (y \neq x \rightarrow \neg P(y)))$



#### Introduce - 反例

##### Example

試證明，每個正整數，是三個整數的平方和。



若正整數為$1$，則我們找不到任意一組$(x, y, z) \in \mathbb{Z}$，使得$x^2 +  y^2 + z^2 = 1$，故假說錯誤。



## 2. Basic Structures: Sets, Functions, Sequences, Sums, and Matrices

### 2.1 Sets

#### Definition - 1

A set is unordered collection of distinct objects, called elements or members of the set.

$a \in A$, $a$ is an element of $A$.

$a \not \in A$, $a$ is not an element of $A$.

##### Example

$\{a, b\} = \{b, a\}$

$\text{{a, a, b}} = \text{{a, b}}$

$(a, b) \neq (b, a)$



#### Introduce -  Roster

##### Example 1

The set of all vowels in  English alphabet.

$V = \{a, e, i, o, u\}$



##### Example 2

The set of positive integers less than 100.

$\text{{1, 2, 3, ... 99, 100}}$



#### Introduce - Set Builder Notation

$\text{{x | x has property P}}$, is read "the set of all x such that x has property P".



##### Example 1

The set of all odd positive integers less than 10.

$O =  \{1, 3, 5, 7, 9...\}$

$O = \text{{x | x is an odd positive integers less than 10}}$

$O = \{{2x+1\ |\ 0 \le x \le 4}\}$



##### Example 2

The set $\mathbb{Q}^+$ of all positive rational integers.

$\mathbb{Q}^+ = \{{x\in\mathbb{R}\ |\ x = \dfrac{a}{b}\text{ for some positive integers p and q.}}\}$



##### Example 3

The set of all natural integers.

$\mathbb{N} = \{0, 1, 2, 3, ...\}$



##### Example 4

The set of all integers.

$\mathbb{Z} = \{..., -2, -1, 0, 1, 2, ...\}$



##### Example 5

The set of all positive integers.

$\mathbb{Z}^+ = \{0, 1, 2, ...\}$



##### Example 6

The set of all rational numbers.

$\mathbb{Q} = \{\dfrac{p}{q}\ |\ p \in \mathbb{Z}, q \in \mathbb{Z}, q \neq 0\}$



#### Definition - 2

Two sets are equal if and only if they have the same elements.

$A = B \iff (x \in A \rightarrow x \in B)$



##### Example

$\{1, 3, 5\} = \{3, 5, 1\}$

$\{1, 3, 3, 3, 5, 5, 5, 5\} = \{1, 3, 5\}$



#### Definition - 3

Empty Set has no element, $\varnothing$



#### Definition - 4

Singleton Set has only one element.

$\{\varnothing\}$



#### Introduce - Venn Diagrams

![image-20210315095124977](https://i.imgur.com/U69Rj6V.png)

$U = \text{{a, b, c, d, e, f, g ...}}$

$V = \text{{a, e, i, o, u}}$



#### Definition - 5

The set $A$ is a subset of set $B$, $B$ is a superset of set $A$ iff every element of $A$ is also an element of $B$.

$A \subseteq B$, $B \supseteq A$

$\forall x(x \in A \rightarrow x \in B)$



#### Theorem - 1

For every set $S$, $\varnothing \subseteq S$, $S \subseteq S$

$\{\} \subseteq \{\}$

$\{\} \subseteq \{a\}$

$\{a\} \subseteq \{a\}$

$\{\} \subseteq \{a, b\}$

$\{a\} \subseteq \{a, b\}$

$\{b\} \subseteq \{a, b\}$

$\{a, b\} \subseteq \{a, b\}$

If the set have $n$ element, it will have $n!$ different subset.



#### Introduce - Proper Subset

$A \subset B \iff \forall x(x \in A \rightarrow x \in B) \and \exist x(x \in B \and x \not \in A)$