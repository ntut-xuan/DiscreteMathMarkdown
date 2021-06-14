# 離散數學 - 筆記



Author: 國立臺北科技大學 109級資工系 黃漢軒

參考書籍：

- Kenneth H. Rosen, Discrete Mathematics and Its Applications Seventh Edition
- Kenneth H. Rosen, 謝良瑜, 陳志賢, 離散數學 第七版

本筆記純粹以自用為主不做任何商業行為，若筆記侵權將會迅速移除，請聯繫 sigtuantw@gmail.com 。



> 2021/05/27 筆記突破80000字
>
> 2021/06/05 筆記突破90000字
>
> 2021/06/09 筆記突破100000字 



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

令$p$與$q$為命題，$p$與$q$的邏輯與，我們表示為$p \land q$，念作"$p$ and $q$"。

當$p$與$q$都為True時，$p \land q$才會true，反之為false。



##### Example

Find the conjunction of the propositions $p$ and $q$ where $p$ is the proposition “Rebecca’s PC has more than 16 GB free hard disk space” and $q$ is the proposition “The processor in Rebecca’s PC runs faster than 1 GHz.”



The conjunction of the propositions $p$ and $q$ is 

"Rebecca’s PC has more than 16 GB free hard disk space, and the processor in Rebecca’s PC runs faster than 1 GHz."



##### Table - 邏輯與的真值表

![image-20210115201510053](https://i.imgur.com/p2VL2Fy.png)



#### Definition - 邏輯或

令$p$與$q$為命題，$p$與$q$的邏輯或，我們表示為$p \lor q$，念作"$p$ or $q$"。

當$p$與$q$都為false時，$p \lor q$為false，反之為true。



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



##### Table - 若且唯若的真值表

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

So that the English sentence be translated into $A \rightarrow (B \lor \neg C)$



### 1.3 命題等價

#### Introduce - 恆真式

恆真式代表複合命題恆為true。



##### Example

$(p \lor \neg p)$

無論$p$是True或者False，他都恆為True，稱為tautology(恆真式)



#### Introduce - 矛盾式

矛盾式代表負和命題恆為false。



##### Example

$(p \land \neg p)$

無論$p$是True或者False，他都恆為False，稱為contradiction



#### Definition - 邏輯等價

令$p$和$q$為複合命題，邏輯等價的定義為$p \leftrightarrow q$為恆等式，寫作$p \equiv q$



##### Example 

證明$p \rightarrow q$和$\neg p \lor q$為邏輯等價。



我們可以窮舉真值表，來證明兩者為邏輯等價

令$A = p \rightarrow q$，$B = \neg p \lor q$，則

| $p$  | $q$  | $A = p \rightarrow q$ | $B = \neg p \lor q$ | $A \leftrightarrow B$ |
| ---- | ---- | --------------------- | ------------------ | --------------------- |
| 0    | 0    | 1                     | 1                  | 1                     |
| 0    | 1    | 1                     | 1                  | 1                     |
| 1    | 0    | 0                     | 0                  | 1                     |
| 1    | 1    | 1                     | 1                  | 1                     |



#### Recall - 德摩根定律

$\neg (p \land q) \equiv \neg p \lor \neg q$

$\neg (p \lor q) \equiv \neg p \land \neg q$



##### Example 2

證明 $\neg (p \lor q)$ 與 $\neg p \land \neg q$ 邏輯等價。



設$A=\neg(p \lor q)$，$B = \neg p \land \neg q$

我們可以窮舉真值表，來證明兩者為邏輯等價

| $p$  | $q$  | $A=\neg(p \lor q)$ | $B = \neg p \land \neg q$ | $A \leftrightarrow B$ |
| ---- | ---- | ----------------- | ------------------------ | --------------------- |
| 0    | 0    | 1                 | 1                        | 1                     |
| 0    | 1    | 0                 | 0                        | 1                     |
| 1    | 0    | 0                 | 0                        | 1                     |
| 1    | 1    | 0                 | 0                        | 1                     |



##### Example 3

證明 $p \rightarrow q$ 和 	$\neg p \lor q$ 邏輯等價。



設$A = p \rightarrow q$，$B = \neg p \lor q$

我們可以窮舉真值表，來證明兩者為邏輯等價。

| $p$  | $q$  | $A = p \rightarrow q$ | $B = \neg p \lor q$ | $A \leftrightarrow B$ |
| ---- | ---- | --------------------- | ------------------ | --------------------- |
| 0    | 0    | 1                     | 1                  | 1                     |
| 0    | 1    | 1                     | 1                  | 1                     |
| 1    | 0    | 0                     | 0                  | 1                     |
| 1    | 1    | 1                     | 1                  | 1                     |



##### Example 4

證明 $p \lor (q \land r)$ 和 $(p \lor q) \land (p \land r)$ 邏輯等價。



我們可以窮舉真值表，來證明兩者為邏輯等價。

| $p$  | $q$  | $r$  | $(q \land r)$ | $(p \lor q)$ | $(p \land r)$ | $p \land (q \lor r)$ | $(p \land q) \land (p \land r)$ | $p \land (q \lor r) \leftrightarrow (p \land q) \land (p \land r)$ |
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

$p \land T \equiv p$

$p \lor F \equiv p$



#### Recall - 支配律

$p \land F \equiv F$

$p \lor T \equiv T$



#### Recall - 冪等律

$p \land p \equiv p$

$p \lor p \equiv p$



#### Recall - 雙非律

$\neg(\neg p) \equiv p$



#### Recall - 交換律

$p \land q \equiv q \land p$

$p \lor q \equiv q \lor p$



#### Recall - 結合律

$(p \lor q) \lor r \equiv p \lor (q \lor r)$

$(p \land q) \land r \equiv p \land (q \land r)$



#### Recall - 分配律

$p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$

$p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$



#### Recall - 吸收律

$p \lor (p \land q) \equiv p$

$p \land (p \lor q) \equiv p$



#### Recall - 否定律

$p \land \neg p \equiv F$

$p \lor \neg p \equiv T$



#### Recall - 一些有關實質蘊含的邏輯等價

$p \rightarrow q \equiv \neg p \lor q$

$p \rightarrow q \equiv \neg q \rightarrow \neg p$

$p \lor q \equiv \neg p \rightarrow q$

$p \land q \equiv \neg(p \rightarrow \neg q)$

$\neg(p \rightarrow q) \equiv p \land \neg q$

$(p \rightarrow q) \land (p \rightarrow r) \equiv p \rightarrow (q \land r)$

$(p \rightarrow r) \land (q \rightarrow r) \equiv (p \lor q) \rightarrow r$

$(p \rightarrow q) \land (p \rightarrow r) \land p \rightarrow (q \lor r)$

$(p \rightarrow r) \lor (q \rightarrow r) \equiv (p \land q) \rightarrow r$



#### Recall - 一些有關若且唯若的邏輯等價

$p \leftrightarrow q \equiv (p \rightarrow q) \land (q \rightarrow p)$

$\displaystyle p \leftrightarrow q \equiv \neg p \leftrightarrow \neg q$

$p \leftrightarrow q \equiv (p \land q) \lor (\neg p \land \neg q)$

$\neg(p \leftrightarrow q) \equiv p \leftrightarrow \neg q$



#### Introduce - 建構新的邏輯等價

如果$p$與$q$邏輯等價，且$q與r$邏輯等價，那麼我們就可以說$p$與$r$邏輯等價。



##### Example 1

證明 $\neg (p \rightarrow q) \equiv p \land \neg q$ 邏輯等價



首先，$p \rightarrow q \equiv \neg p \lor q$，所以$\neg (p \rightarrow q) \equiv \neg(\neg p \lor q) \equiv p \land \neg q$

因此$\neg (p \rightarrow q) \equiv p \land \neg q$，證畢



##### Example 2

利用一連串的邏輯等價，證明 $\neg (p \lor (\neg p \land q)) \equiv \neg p \land \neg q$



利用德摩根定律，得到$\neg (p \lor (\neg p \land q)) \equiv \neg p \land \neg(\neg p \land q)$

再次利用德摩根定律，得到$\neg p \land \neg(\neg p \land q) \equiv \neg p \land(p \lor \neg q)$

利用分配律，$\neg p \land(p \lor \neg q) \equiv (p \land \neg p) \lor (\neg p \land \neg q) \equiv F \lor (\neg p \land \neg q) \equiv (\neg p \land \neg q)$

因此，$\neg (p \lor (\neg p \land q)) \equiv \neg p \land \neg q$，證畢



##### Example 3

證明 $(p \land q) \rightarrow (p \lor q)$為恆等式



利用$p \rightarrow q \equiv \neg p \lor q$的特性，改寫為$(p \land q) \rightarrow (p \lor q) \equiv \neg(p \land q) \lor (p \lor q)$

利用德摩根定律，改寫為$\neg(p \land q) \lor (p \land q) \equiv (\neg p \lor \neg q) \lor (p \lor q)$

利用交換律，$(\neg p \lor p) \lor(\neg q \lor q) \equiv T \lor T \equiv T$

故$(p \land q) \rightarrow (p \lor q)$為恆等式，證畢。



#### Introduce - 滿足命題

滿足命題的定義是，若有一個複合命題$P$，若能找到一組變數能夠使$P$為true，則$P$能夠被滿足。



##### Example

判斷以下三個複合命題$P$是否能夠被滿足。

1. $(p \land \neg q) \lor (q \land \neg r) \land (r \lor \ \neg p)$
2. $(p \land q \land r) \lor (\neg p \land \neg q \land \neg r)$
3. $(p \lor \neg q) \land (q \lor \neg r) \land (r \lor \neg p) \land (p \lor q \lor r) \land (\neg p \lor \neg q \lor \neg r)$



第一個命題：若$p,q,r$其中有一個是true，則可以滿足命題：。

第二個命題：若$p,q,r$都為true或者都為false，則可以滿足命題。

第三個命題：

考慮到

$(p \lor \neg q) \land (q \lor \neg r) \land (r \lor \neg p)$必須要是true，則$p, q, r$都必須要是true，或者$p, q, r$都必須要是false。

$(p \lor q \lor r) \land (\neg p \lor \neg q \lor \neg r)$必須要是true，則$p, q, r$都不能是true，或者都不能是false。

因此，兩者矛盾，故$(p \lor \neg q) \land (q \lor \neg r) \land (r \lor \neg p) \land (p \lor q \lor r) \land (\neg p \lor \neg q \lor \neg r)$不能被滿足。



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



我們可以把真值表達成$P(1) \land P(2) \land P(3) \land P(4)$

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

所以我們可以寫成$P(1) \lor P(2) \lor P(3) \lor P(4)$

由於我們可以知道，$4^2 = 16 > 10$ ，因此$P(4)$為true

故$P(1) \lor P(2) \lor P(3) \lor P(4)$為true

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

第三個例子，若$z > 0$，則$z^2 = 2$，則我們可以寫成$(z > 0) \land (z^2 = 2)$

且至少一個$z$都要符合這個敘述，因此$\exist z[(z > 0) \land (z^2 = 2)]$



##### Introduce - 量詞的優先級

$\forall$與$\exist$是所有邏輯符號中優先級最高的，也就是若$\forall x P(x) \lor Q(x)$，他代表著$(\forall x P(x)) \lor Q(x)$，而非$\forall x (P(x) \lor Q(x))$



#### Introduce - 綑綁變數

如果量詞用在變數$x$上，則我們說變數$x$為一個綑綁變數，否則他就是自由變數。

一個命題函數所有變數都必須為綑綁變數，則這個命題變數才會變成一命題。

無論是存在量化、全稱量化都可以使用



##### Example 1

在敘述$\exist x (x + y = 1)$中，我們可以知道$x$是綑綁變數，因為前面的存在量詞是對$x$的

但是沒有任何對$y$的量化，因此$y$為一個自由變數。



##### Example 2

在敘述$\exist x(P(x) \land Q(x)) \lor \forall x R(x)$，所有的變數都是綑綁變數

第一個存在量詞對括號內所有的$x$進行綑綁，而第二個存在量詞對命題函數$R$的變數$x$進行綑綁。



##### Example 3

在敘述$\exist x(P(x) \land Q(x)) \lor \forall y R(y)$，所有變數都是綑綁變數

第一個存在量詞對括號內所有的$x$進行綑綁，而第二個存在量詞對命題函數$R$的變數$y$進行綑綁。



#### Introduce - 關於量化的邏輯等價

##### Definition - 量化的邏輯等價

關於量詞與謂語的邏輯等價，若兩邊敘述若且唯若擁有相同的真值，則我們稱他為邏輯等價。

不用考慮謂語如何替代敘述，或者在命題函數中的定義域為何。



##### Example

證明$\forall x (P(x) \land Q(x))$與$\forall P(x) \land \forall Q(x)$邏輯等價。



若要證明$\forall x (P(x) \land Q(x))$與$\forall P(x) \land \forall Q(x)$邏輯等價

則我們假設$a \in D(x)$，其中$D(x)$代表$x$的定義域，那麼如果$\forall x (P(x) \land Q(x))$是true，則$P(a) \land Q(a)$都為true。

達成與邏輯為正的條件即為$P(a)$與$Q(a)$皆為true，則與邏輯才會成立。

接著，假設$\forall x P(x) \land \forall x Q(x)$為true，且$a \in D(x)$

那麼為了達成與邏輯的條件，$P(a)$應為true，$Q(a)$也應為true。

故$P(a) \land Q(a)$應為true，而$a \in D(x)$，則代表所有在$D(x)$的變數$a$都可以使得$P(a) \land Q(a)$為true

故我們可以把$a$改寫成$\forall x (P(x) \land Q(x))$

因此，我們可以得知，$\forall x (P(x) \land Q(x))$與$\forall x P(x) \land \forall x Q(x)$邏輯等價。



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

若$P \lor Q \equiv T$，且$\neg P \equiv T$，則$Q \equiv T$



##### Example

我要嘛選擇睡覺，要嘛選擇讀書。

我沒在睡覺。

所以我在讀書。



#### Introduce - 添加律

若$P \equiv T$，則$P \lor Q \equiv T$



##### Example

若我在睡覺。

所以我可能在睡覺或者在讀書。



#### Introduce - 簡化律

若$P \land Q  \equiv T$，則$P \equiv T$



##### Example

外面是晚上而且外面在下雨

所以外面是晚上。



#### Introduce - 連言

若$P \equiv T$，且$Q \equiv T$，則$P \land Q \equiv T$



##### Example

外面是晚上。

外面在下雨。

所以外面是晚上，而且外面在下雨。



#### Introduce - 預解律

若$P \lor Q \equiv T$，且$\neg P \lor R \equiv T$，則$Q \lor R \equiv T$



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
| $P \rightarrow Q$ is true | $P$ is true, $\neg Q$ is true | $(P \land \neg Q) \rightarrow F$ |



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

$\exist x (P(x) \land \forall y (y \neq x \rightarrow \neg P(y)))$



#### Introduce - 反例

##### Example

試證明，每個正整數，是三個整數的平方和。



若正整數為$1$，則我們找不到任意一組$(x, y, z) \in \mathbb{Z}$，使得$x^2 +  y^2 + z^2 = 1$，故假說錯誤。



## 2. 基礎結構: 集合、函數、序列、總和、與矩陣

### 2.1 集合

#### Definition - 集合

集合是一個不需按照順序排列，且集合內部所有元素均不相等的物件。

$a \in A$, $a$ 是集合 $A$ 的元素之一。

$a \not \in A$, $a$ 不是集合 $A$ 的元素之一。



##### Example

$\{a, b\} = \{b, a\}$

$\text{{a, a, b}} = \text{{a, b}}$

$(a, b) \neq (b, a)$



#### Introduce -  窮舉法

如果窮舉出集合內的所有物件是可能的，我們可以窮舉出集合內的所有物件。



##### Example 1

所有母音的集合。

$V = \{a, e, i, o, u\}$



##### Example 2

所有小於100的正整數的集合。

$O = \text{{1, 2, 3, ... 99, 100}}$



#### Introduce - 集合建構式符號

$\text{{x | x has property P}}$，念作「所有符合條件$P$元素$x$的集合」。



##### Example 1

所有小於10的正整數奇數集合。

$O =  \{1, 3, 5, 7, 9...\}$

$O = \text{{x | x is an odd positive integers less than 10}}$

$O = \{{2x+1\ |\ 0 \le x \le 4}\}$



##### Example 2

所有正的有理數，且為整數的集合$\mathbb{Q}^+$。

$\mathbb{Q}^+ = \{{x\in\mathbb{R}\ |\ x = \dfrac{a}{b}\text{ for some positive integers p and q.}}\}$



##### Example 3

所有自然數的整數集合。

$\mathbb{N} = \{0, 1, 2, 3, ...\}$



##### Example 4

所有整數的集合。

$\mathbb{Z} = \{..., -2, -1, 0, 1, 2, ...\}$



##### Example 5

所有正整數的集合。

$\mathbb{Z}^+ = \{0, 1, 2, ...\}$



##### Example 6

所有有理數的集合。

$\mathbb{Q} = \{\dfrac{p}{q}\ |\ p \in \mathbb{Z}, q \in \mathbb{Z}, q \neq 0\}$



#### Definition - 集合相等

若兩個集合的所有元素相等，則我們說這兩個集合相等。

$A = B \iff (x \in A \rightarrow x \in B)$



##### Example

$\{1, 3, 5\} = \{3, 5, 1\}$

$\{1, 3, 3, 3, 5, 5, 5, 5\} = \{1, 3, 5\}$



#### Definition - 空集合

空集合沒有任何元素，寫作 $\varnothing$。



#### Definition - 單元素集合

單元素集合只有一個元素。



##### Example

$\{\varnothing\}$ 是一個單元素集合。



#### Introduce - 文氏圖

我們可以用文氏圖來表示一個集合。



##### Example

![image-20210315095124977](https://i.imgur.com/uouK3oM.png)

$U = \text{{a, b, c, d, e, f, g ...}}$

$V = \text{{a, e, i, o, u}}$



#### Definition - 子集合

若且唯若集合$A$的每個元素都為集合$B$的元素，則我們說$A$是$B$的子集合，且$B$為$A$的父集合。

可以表示成$(A \subseteq B \land B \supseteq A) \iff \forall x(x \in A \rightarrow x \in B)$



#### Theorem - 1

對於每一個集合 $S$, $\varnothing \subseteq S$, $S \subseteq S$

$\{\} \subseteq \{\}$

$\{\} \subseteq \{a\}$

$\{a\} \subseteq \{a\}$

$\{\} \subseteq \{a, b\}$

$\{a\} \subseteq \{a, b\}$

$\{b\} \subseteq \{a, b\}$

$\{a, b\} \subseteq \{a, b\}$

如果一個集合有$n$個元素，則他會有$n!$種不同的子集合。



#### Introduce - 真子集

若$A$是$B$的真子集，則對於所有在集合$A$的$x$也都在集合$B$，且$B$存在一個元素不在集合$A$。

可以寫作，$A \subset B \iff \forall x(x \in A \rightarrow x \in B) \land \exist x(x \in B \land x \not \in A)$。



#### Definition - 有限集合與無限集合

如果一個集合有剛好$n$個元素，且$n$存在，則我們說這個集合是有限的，否則這個集合是無限的。



#### Definition - 集合的勢

若有一個集合$A$，我們定義「集合的勢」為集合內部的元素數量，寫作$|A|$。



##### Example 1

$|\varnothing| = 0$



##### Example 2

令集合$S$為擁有所有字母的集合，則$|S| = 26$



##### Example 3

$|\{1, 2, 3\}| = 3$



##### Example 4

$|\{\varnothing\}|= 1$



##### Example 5

若$S$為所有整數的集合，則$|S|$為無限。



#### Introduce - 冪集

若存在一個集合有集合$A$的所有子集，我們寫作$\wp(A)$。

如果集合$A$有$N$個元素，則$|\wp(A)| = 2^N$。



##### Example

若$A=\{a, b\}$，則$\wp(A) = \{\{\varnothing\}, \{a\}, \{b\}, \{a, b\}\}$



#### Introduce - 多元組

- 一個有序且長度為$n$的多元組包含了元素$(a_1, a_2, a_3, ... a_n)$，且$a_1$是第一個元素，$a_n$是最後一個元素。

- 兩個長度為$n$的多元組$A, B$，我們先用$A_i$表示多元組$A$的第$i$個元素。

  若兩個多元組的每一項都相同，也就是$A_1 = B_1, A_2 = B_2, ... ,A_n = B_n$，則兩個多元組就是相同的。

- 長度為$2$的多元組我們稱作有序對。
- 若有兩個有序對$(a, b)$與$(c, d)$，則若$a = c$且$b = d$，則兩個有序對才相同。



##### Example

若有兩個長度為$n$的多元組$A, B$。

$A = (1, 2, 3, 4, 5)$，$B = (5, 4, 3, 2, 1)$，則$A \neq B$

$A = (1, 2, 3, 4, 5)$，$B = (1, 2 ,3, 4)$，則$A \neq B$

$A = (1, 2, 3, 4, 5)$，$B = (1, 2 ,3, 4, 5)$，則$A = B$



#### Introduce - 笛卡兒積

兩個集合$A, B$相乘，我們稱作笛卡爾積，寫作$A \times B$。

$A \times B$是一個集合，包含了所有不同的有序對$(a, b)$，其中$a \in A$，$b \in B$

我們可以寫成這樣：$A \times B = \{(a, b) | a \in A \land b \in B\}$



##### Example

若集合$A = \{a, b\}$，集合$B = \{1, 2\}$

則$A \times B = \{(a, 1), (a, 2), (b, 1), (b, 2)\}$



#### Introduce - 笛卡兒積的子集合

在笛卡爾積的子集合$R$，我們可以說與集合$A$和集合$B$都有關係。



#### Introduce - 多個集合的笛卡兒積

若我們有$m$個集合$A_1, A_2, A_3, ..., A_M$，則笛卡爾積寫作$A_1 \times A_2 \times  ...\times A_M$。

則$A_1 \times A_2 \times  ...\times A_M = (a_1, a_2, ... ,a_n)$，為一個有序多元組的集合，其中$a_i \in A_i, i = 1, 2, ..., n$。



##### Example

若$A = \{0, 1\}$，$B = \{1, 2\}$，$C = \{0, 1, 2\}$，求$A \times B \times C$



$A × B × C = \{(0,1,0), (0,1,1), (0,1,2),(0,2,0), (0,2,1), (0,2,2),(1,1,0), (1,1,1), (1,1,2), (1,2,0), (1,2,1), (1,2,2)\}$



#### Introduce - 量詞的真值集

給定一個量詞$P$與定義域$D$，我們定義量詞$P$的真值集為所有使得$P$為true且在定義域$D$的元素。

我們可以把真值集寫作$\{x \in D | P(x)\}$。



##### Example

給定定義域$D$為所有整數與$P(x)$為$|x| = 1$，找出$P(x)$的真值集。

則$P(x)$的真值集為$\{-1, 1\}$。



### 2.2 集合運算子

#### Introduce - 聯集

$A$與$B$為集合，若$A$與$B$取聯集，則我們可以表示成$A \cup B = \{x | x \in A \lor x \in B\}$。

![image-20210318201511613](https://i.imgur.com/4E0HEfG.png)



##### Example

若$A = \{1, 2, 3\}$，且$B = \{3, 4, 5\}$，則$A \cup B = \{1, 2, 3, 4, 5\}$





#### Introduce - 交集

$A$與$B$為集合，若$A$與$B$取交集，則我們可以表示成$A \cap B = \{x | x \in A \land x \in B\}$

![image-20210318201634099](https://i.imgur.com/8kYIVY9.png)

如果$A \cap B = \varnothing$，則$A$與$B$的關係為互斥的。



##### Example 1

若$A = \{1, 2, 3\}$，且$B = \{3, 4, 5\}$，則$A \cap B = \{3\}$



##### Example 2

若$A = \{1, 2, 3\}$，且$B = \{4, 5, 6\}$，則$A \cap B = \varnothing$



#### Introduce - 補集

令$A$是一個集合，則$A$的補集(通常叫做宇集$U$)，寫作$\overline{A}$，為$U - \overline{A}$的集合。

定義為$\overline{A} = \{x \in U | x \not \in A\}$

$A$的補集有時表示成$A^c$。



##### Example

如果宇集$U$代表小於$100$的正整數，則求$\{x | x > 70\}$的補集。



$\{x | x \le 70\}$



#### 

#### Introduce - 差集

令$A$與$B$為一個集合。

$A$與$B$的差集，可以表示成$A - B$，代表集合$A$不包含集合$B$的東西。

可以被定義為$A - B = \{x | x \in A \land x \not \in B\} = A \cap \overline{B}$



##### Example

令$A = \{1, 2, 3\}$，$B = \{3, 4, 5\}$，求$A - B$



$A - B = \{1, 2\}$



#### Introduce - 兩個集合交集的勢

利用排容原理。

$|A \cup B| = |A| + |B| - |A \cap B|$



##### Example

令$A = \{1, 2, 3\}$，$B = \{3, 4, 5\}$，求$|A \cup B|$



$|A \cup B| = |A| + |B| - |A \cap B| = |3| + |3| - |5| = 1$



#### Introduce - 對稱差

若有兩個集合$A$與$B$，則$A$與$B$的對稱差寫作$A \oplus B$。

定義為$A \oplus B = (A-B) \cup (B-A)$



##### Example

若$U = \{0, 1 ,2, 3, 4, 5, 6, 7, 8, 9\}$，$A = \{1, 2, 3, 4, 5\}$，$B = \{3, 4, 5, 6, 7\}$，求$A \oplus B$



$A \oplus B = (A - B) \cup (B - A) = \{1, 2\} \cup \{6, 7\} = \{1, 2, 6, 7\}$



#### Introduce - 集合特徵

- 恆等律
  - $A \cup \varnothing = A$，$A \cap U = A$
- 支配律
  - $A \cup U = U$，$A \cap \varnothing = \varnothing$
- 冪等律
  - $A \cup A = A$，$A \cap A = A$
- 補餘律
  - $\overline{(\overline{A})} = A$
- 交換律
  - $A \cup B = B \cup A$，$A \cap B = B \cap A$
- 連鎖律
  - $A \cup (B \cup C) = (A \cup B) \cup C$
  - $A \cap (B \cap C) = (A \cap B) \cap C$
- 分配律
  - $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
  - $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$
- 德摩根定律
  - $\overline{A \cup B} = \overline{A} \cap \overline{B}$，$\overline{A \cap B} = \overline{A} \cup \overline{B}$
- 吸收律
  - $A \cap (A \cup B) = A$，$A \cap (A \cup B) = A$
- Complement laws
  - $A \cup \overline{A} = U$，$A \cap \overline{A} = \varnothing$

### 2.3 函數

#### Definition - 函數

令$A$與$B$為一個非空集合，一個函數從$A$映射$B$，寫作$A \rightarrow B$。

代表每一個集合$A$的元素都剛好指向一個集合$B$的元素，寫作$f(a) = b$。

其中$b$為集合$B$的相異元素，被集合$A$的元素所映射。



#### Introduce - 笛卡耳積的函數

一個$A \rightarrow B$，可以用來表示$A \times B$的子集合，寫作

$\forall x(x \in A \rightarrow \exist y(y \in B \land (x, y) \in f))$

以及

$\forall x, y_1, y_2[[(x, y_1) \in f \land (x, y_2) \in f] \rightarrow y_1 = y_2]$



#### Introduce - 映射、像與原像

給你一個集合$A$與集合$B$，我們說$f$是由$A$映射$B$所組成，則

$A$被稱為$f$的定義域

$B$被稱為$f$的值域

如果$f(a) = b$，則$b$被稱為$f$在$a$的像，$a$被稱為$b$的像原

當兩個函數有相同的定義域，相同的域值，還有兩個函數的像與像原映射相同，則兩個函數相同。



#### Introduce - 單射

函數$f$被稱做一對一函數，或者稱做單射，也就是對於所有在定義域的$a, b$，若且唯若$f(a) = f(b)$，則$a = b$。

函數$f$如果是一對一函數，則這個函數是個單射函數。



#### Introduce - 滿射

若有兩集合$A, B$，若且唯若所有元素$b \in B$，存在一個$a \in A$，使得$f(a) = b$，則稱做這個函數為滿射函數。



#### Introduce - 對射

若一個函數是一對一函數，且函數滿射，則我們稱作這個函數是一對一對應函數或叫做對射函數。



#### Introduce - 反函數

令$f$是一個集合$A$對集合$B$的對射函數，$f$的反函數寫作$f^{-1}$。

反函數$f^{-1}$代表集合$B$對集合$A$的函數，定義為若且唯若$f^{-1}(y) = x$則$f(x) = y$。



#### Introduce - 複合函數

令$f$為集合$B$對集合$C$的函數，且$g$為集合$A$對集合$B$的函數，$f$與$g$的複合函數，寫作$f \circ g$，代表一個集合$A$對集合$C$的函數，定義為$(f \circ g)(x) = f(g(x))$。



#### Introduce - 函數的圖形

令$f$為一個集合$A$對集合$B$函數，函數$f$的圖形即為每一對的$(a, b)$，即為

$\{(a, b) | a \in A \land f(a) = b\}$



#### Introduce - 一些重要的函數

底函數代表將小於等於$x$之最大整數指派給實數$x$，記為$\lfloor x \rfloor$

頂函數代表將大於等於$x$之最小整數指派給實數$x$，記為$\lfloor x \rfloor$

階乘函數$f: \mathbb{N} \rightarrow \mathbb{Z}^+$，記為$f(n) = n! = 1 \times 2 \times .... \times n$，其中$n \in \mathbb{Z}^+$。



##### Table - 頂函數與升函數

![image-20210322170033159](https://i.imgur.com/8qsQOXA.png)



#### Introduce - 部分函數

令$f$為一個集合$A$對集合$B$函數。

若$f$的定義域$D(f) \subseteq A$，且$f$的值域$R(f) \subseteq B$，則我們稱$f$為一部分函數。



### 2.4 數列與總和

#### Definition - 序列

- 序列是有序的表列，例如$1, 3, 5, 7, 9$，或者$1, 4, 9, 16, 25$。
- 序列是一個整數子集的函數。
- 我們使用符號$\{a_n\}$來描述序列。

##### Example

考慮序列$a_n$，其中$a_n = \dfrac{1}{n}$

由$a_1$開始，可記為$a_1, a_2, a_3, a_4, ...$

前幾項為$1, \dfrac{1}{2}, \dfrac{1}{3}, \dfrac{1}{4}...$



#### Introduce - 幾何數列

一個幾何數列可以表示成：$a, ar, ar^2, ar^3, ... ,ar^n$，其中$a$為首項，$r$為公比。



##### Example

若有一序列$a_n = (-1)^n$，則我們說這是一個幾何數列，因為$a_n$的前幾項為$1, -1, 1, -1 ...$，即為$a=1$，$r = -1$。



#### Introduce - 算術數列

一個算術數列可以表示成：$a, a+d, a+2d, a+3d, ..., a+nd$，其中$a$為首項，$d$為公差



##### Example

若有一序列$a_n = 1 + 3n$，則我們說這是一個算術數列，因為$a_n$的前幾項為$1, 4, 7, 10...$，即為$a = 1$，$r = 3$。



#### Definition - 字串

- 字串為有限字元數所組成的序列。
- 一個不含任何項的字串稱作空字串。



#### Introduce - 遞迴關係式

遞迴關係，也就是差分方程式，是一種遞推地定義一個序列的方程式：序列的每一項目是定義為前一項的函數。



##### Example - 斐波納契數列

一個Fibonacci Sequence可以由以下的性質定義

$F_0 = 0$

$F_1 = 1$

$F_n = F_{n-2} + F_{n-1}$



因此，斐波納契數列的序列為

$\{0, 1, 1, 2, 3, 5, 8, 13, 21 ...\}$



### 2.5 集合的勢

#### Definition - 勢

- 令A與B為兩個集合，若且唯若A與B對射，則集合A與集合B的勢是相同的，寫作$|A| = |B|$。

- 令A與B為兩個集合，若且唯若A與B單射，則集合A的勢小於等於集合B的勢，寫作$|A| \le |B|$。

  如果集合A的勢與集合B的勢不同，則$|A| < |B|$。

- 一個集合如果是有限的，或者與正整數集合的勢相同，則我們說這個集合是可數的，否則就是不可數的。

  例如一個實數集合是個不可數的集合。

- 如果一個無限的集合是可數的，他的勢為$ℵ_0$，寫作$|S| = ℵ_0$，且唸做"aleph null"。

- 一個無限集合的勢，若且唯若可以將所有的元素列成一個數列，則我們說這個無限集合的勢是可數的。

  原因是一個無限集合的勢，可以寫作一個對射函數，且函數的index是正整數，故我們可以寫成這樣的形式：

  $f(1) = a_1, f(2) = a_2, ... f(n) = a_n$

  故根據「一個集合如果是有限的，或者與正整數集合的勢相同，則我們說這個集合是可數的」，我們可以知道無限集合的勢，若且唯若可以將所有的元素列成一個數列，則我們說這個集合是無限的。



#### Introduce - 希爾伯特旅館悖論

一個有無限間房間的旅館，每一個房間均住滿人，我們要怎麼樣能夠再容納一個旅客？



假設我們有無限多個客人，我們將每個客人$j$編號成$a_j$，新的客人我們表示成$a_0$，則我們可以寫成這樣的形式

$f(1) = a_1, f(2) = a_2, f(3) = a_3, f(4) = a_4, ..., f(n) = a_n, ...$



我們可以將第$i$房的人，請他移駕至第$i+1$房，這樣就會使第一間房間空出來。

$g(1) = a_0, g(2) = a_1, g(3) = a_2, g(4) = a_3,..., g(n) = a_{n-1}, ...$



可以顯而易見的知道這樣分配不會使房間編號撞號。



##### Example  - 證明集合是可數的(1)

證明正偶數整數集合$E$是可數的。



令$f(x) = 2x$，則我們可以將其列成序列，也就是

$f(1) = 2, f(2) = 4, f(3) = 6, f(4) = 8, ..., f(n) = 2n$

我們可以證明這個函數是對射，假設$t$為偶正整數，則它可以寫成$2k$的形式，故每一個$t$存在唯一一個$k$，使得$f(k) = t$

我們可以證明這個函數是一對一函數，假設存在$f(n) = f(m)$，必定存在$2n = 2m$，也就是存在$n = m$

故若$n = m$，才能使得$f(n) = f(m)$

根據勢的定義，「一個無限集合的勢，若且唯若可以將所有的元素列成一個數列，則我們說這個無限集合的勢是可數的。」

因此$f(x) = 2x$是可數的。



##### Example  - 證明集合是可數的(2)

證明整數集合$Z$是可數的。



將集合$Z$列成：$0, 1, -1, 2, -2, 3, -3 ... $

我們可以寫成以下的部分函數：$f(x) = \left\{ \begin{array}\ f(x) = -(x-1)/2 & x \in \text{odd} \\ f(x) = x/2 & x \in \text{even} \end{array}\right.$



## 4. 數論與密碼學

### 4.1 可除性與模算術

#### Definition - 除法

- 如果$a$與$b$是整數，且$a \neq 0$，則我們說$b$能夠被$a$整除，如果存在一個整數$c$，使得$b = ac$。
- 如果$b$能夠被$a$整除，則我們說$a$是$b$的因數或者被除數，且$b$為$a$的倍數。
- 我們用$a | b$來表示$b$能夠被$a$整除。
- 如果$a|b$，則$b/a$為一個整數。
- 如果$a$沒辦法整除$b$，則我們表示為$a \not |\ \ b$



#### Theorem 1

令$a, b, c$為整數，且$a \neq 0$，則如果$a | b$和$a|c$，則$a|(b+c)$



##### Proof

如果$a|b$，則我們可以說存在一個整數$s$，使得$as = b$

如果$a|c$，則我們可以說存在一個整數$t$，使得$at = c$

因此$b+c = as+at = a(s+t)$，因為$s+t$為整數，由此可證如果$a | b$和$a|c$，則$a|(b+c)$



#### Theorem 2

令$a, b, c$為整數，且$a\neq 0$，則如果$a|b$，那麼對於任意$c$，符合$a|bc$



##### Proof

如果$a|b$，則我們可以說存在一個整數$s$，使得$as = b$

將等號兩邊同乘以$c$，得到$asc = bc$

由於兩個整數相乘為整數，故我們依然可以找到一個整數$d = sc$，使得$ad = bc$

由此可證如果$a|b$，那麼對於任意$c$，符合$a|bc$。



#### Theorem 3

令$a, b, c$為整數，且$a\neq 0$，則如果$a|b$且$b|c$，那麼$a|c$



##### Proof

如果$a|b$，則我們可以說存在一個整數$s$，使得$as = b$

如果$b|c$，則我們可以說存在一個整數$t$，使得$bt = c$，也就是$ast = c$

由於兩個整數相乘為整數，故我們依然可以找到一個整數$d = st$，使得$ad = c$

由此可證如果如果$a|b$且$b|c$，那麼$a|c$。



#### Corollary 1

如果$a, b, c$為整數，且$a \neq 0$，$a|b$和$a|c$，那麼$a|mb+nc$，其中$n, m \in \mathbb{Z}$



#### Introduce - 除法算法

如果$a \in \mathbb{Z}$，且$d \in \mathbb{Z}^+$，那麼存在唯一$q, r \in \mathbb{Z}$，其中$0 \le r < d$，使得$a = dq + r$。

其中$a$被稱為被除數，$d$被稱為除數，$q$被稱做商，$r$被稱做餘數。



我們可以用$\text{mod}$與$\text{div}$來取得商與餘數，定義

$q =  \text{a div d}$

$r = \text{a mod d}$



#### Introduce - 同餘關係

如果$a, b$為整數，且$m$為一正整數，則如果$m$可以整除$a-b$，我們說$a$與$b$同餘模$m$，可以用$a \equiv b \pmod m$來表示。

兩個整數$a, b$能夠同餘模$m$，若且唯若$a$除以$m$與$b$除以$m$的餘數相同。

如果$a$除以$m$與$b$除以$m$的餘數不同，那麼我們表示為$\displaystyle a \not\equiv b \pmod m$



#### Theorem 4

令$m$為一正整數，整數$a, b$能夠同餘於$m$，若且唯若存在一個$k$使得$a = b + km$



##### Proof

若$a \equiv b \pmod m$，那麼$m | (a-b)$

因此，會存在一個$k$，使得$mk = a-b$，因此$a = mk+b$

反之，若存在一個$k$使得$a = b+km$，那麼$km = a-b$，因此可以得知$m | (a-b)$和$a \equiv b \pmod m$



#### Introduce - 兩個不同的表示法(mod m) 與 mod m

- $a \equiv b \pmod m$與$a \text{ mod } m = b$是不同的東西
  - $a \text{ mod } m = b$, 代表函數的關係。
  - $a \equiv b \pmod m$, 代表一個整數集合的關係。



#### Theorem 5

令$a, b$為整數，令$m$為正整數，則$a \equiv b \pmod m$ 若且唯若 $a \text{ mod } m = b \text{ mod } m$。



##### Proof

如果$a \equiv b \pmod m$，則我們可以說$a - b = me, e \in \mathbb{Z}$，因此$a = me + b$

那麼令$d = b \text{ mod } m$，我們可以表示成$b = mr + d, r \in \mathbb{Z}, , 0 \le d < m$

因此$a = me + mr + d = m(e+r) + d$

我們可以說$(e+r)$是$a/m$的商，$d$為$a/m$的餘。

故$a \mod m = d = b \mod m$



#### Theorem 6

令$m$為正整數，如果$a \equiv b \pmod m$和$c \equiv d \pmod m$，那麼$(a + c) \equiv (b+d) \pmod m$且$ac \equiv bd \pmod m$



##### Proof

如果$a \equiv b \pmod m, c \equiv d \pmod m$，那麼存在$s, t \in \mathbb{Z}$，使得$a = sm + b$，且$c = tm + d$

故$a + c = (s+t)m + (b+d)$，且$ac = stm^2 + sdm + tbm + bd = m(stm+sd+tb)+bd$

因此$(a + c) \equiv (b+d) \pmod m$，$ac \equiv bd \pmod m$



#### Introduce - 同餘的代數運算

- 令$a, b$為整數，若$a \equiv b \pmod m$，則$ac  \equiv bc \pmod m$

  ※可以根據Theorem 6，令$d = c$。

- 令$a, b$為整數，若$a \equiv b \pmod m$，則$a + c \equiv b + c \pmod m$

  ※可以根據Theorem 6，令$d = c$。

- 除法並不保證能夠用在同餘上。



#### Corollary 2

令$m$為正整數，令$a, b$為整數，則

$(a + b) \text{ mod } m = ((a \text{ mod } m) + (b \text{ mod } m)) \text{ mod } m$ 

$(ab) \text{ mod } m = ((a \text{ mod } m)(b \text{ mod } m)) \text{ mod } m$



##### Proof

根據模的定義，則$a \equiv (a \text{ mod } m) \pmod m$，$b \equiv (b \text{ mod } m) \pmod m$

By Theorem 6，可知$a+b \equiv (a \text{ mod } m)+(b \text{ mod } m) \pmod m$

以及$ab \equiv (a \text{ mod } m)(b \text{ mod } m) \pmod m$



#### Definition - 模的算術運算元

令$\mathbb{Z}_m$為所有小於$m$的非負整數集合，則

- $a +_m b$，用來表示$(a+b) \text{ mod } m$
- $a \cdot_m b$，用來表示$(ab) \text{ mod } m$
- 模的算術運算元有許多性質
  - 封閉性：如果$a, b \in \mathbb{Z_m}$，則$a +_m b \in \mathbb{Z}_m$和$a \cdot_m b \in \mathbb{Z}_m$。
  - 結合律：如果$a, b, c, \in \mathbb{Z}_m$，則$(a +_m b) +_m c = a +_m (b +_m c)$，且$(a \cdot_m b) \cdot_m c = a \cdot_m (b \cdot_m c)$
  - 交換律：如果$a, b \in \mathbb{Z}_m$，則$a +_m b = b +_m a$，且$a \cdot_m b = b \cdot_m a$
  - 單位元素：如果$a \in \mathbb{Z}_m$，則$a +_m 0 = a$，且$a \cdot_m 1 = a$
  - 加法反元素：如果$a \neq 0$且$a \in \mathbb{Z}_m$，則$a +_m (m-a) = 0$，且$0 +_m 0 = 0$
  - 分配律：如果$a, b, c, \in \mathbb{Z}_m$，那麼$a \cdot_m (b +_m c)  = (a \cdot_m b) +_m (a \cdot_m c)$，$(a +_m b)\cdot_m c = (a\cdot_m c)+(b\cdot_mc)$



### 4.2 整數表示與演算法



#### Theorem 1

令$b$為一個大於1的正整數，如果$n$為一正整數，則他可以表示成$n = a_kb^k + a_{k-1}b^{k-1} + ... + a_1b + a_0 b^0$

其中$k$為非負整數，$a_0, a_1 ...$為一非負整數，且小於$b$，且$a_k \neq 0$。

$a_j$，$j = 0, 1, ... , k$為以$b$為底數的各個位數。



### 4.3 質數與最大公因數

#### Definition - 質數

一個正整數$p > 1$，若$p$的因數只有它自己與$1$，則我們說這個數字$p$是質數。

若$p > 1$，且$p$的因數不只有它自己與$1$即為合數。



#### Theorem 1

任何大於$1$的正整數都可以用質數的乘積來分解，且分解的結果為唯一。

且結果我們通常會用非遞減的形式呈現。



##### Example

$100 = 2\times 2\times 5\times 5= 2^2 \times 5^2$

$641 = 641$

$999 = 3 \times 3 \times 3 \times 37 = 3^3 \times 37$

$1024 = 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 = 2^{10}$



#### Introduce - 厄拉托西尼篩法

厄拉托西尼篩法可以在一定的範圍內找到所有質數，舉個例子，我們可以用厄拉托西尼篩法找1~100的所有質數。

1. 刪除所有2的倍數的數字，除了2。
2. 刪除所有3的倍數的數字，除了3。
3. 刪除所有5的倍數的數字，除了5。
4. 刪除所有7的倍數的數字，除了7。
5. 這樣一來，所有剩下的數字都不能被2、3、5、7給整除，因此質數為$\{2,3,5,7,11,15,1719,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89, 97\}$



#### Theorem 2

質數的個數是無限的。



##### Proof

令$P = p_1 p_2 p_3 p_4 ... 	p_n$，且$q = P+1$，則$q$是質數或不是質數，兩者必居其一。

如果$q$是質數，那麼至少有一個質數不在有限質數集$p1, p2, p3 ... p_n$中。

如果$q$是合數，那麼存在一個質數因子$p$整除$q$，如果$p$在我們的質數集合$P$中，則$p$必然整除$P$。

但是，已知$p$整除$P+1$，如果$p$同時整除$P$和$q$，則$P$必然整除$P$與$q$之差，也就是$(P+1) - P = 1$

但是沒有質數能整除$1$，即有$p$整除$q$，就不存在$p$整除$P$，因此$p$不在有限質數集合$P$中。

這就證明了：對於任何一個有限的質數集，總有一個質數不在其中，所以質數一定是無限的。



#### Theorem 3

定義$\pi(x) = \dfrac{x}{\ln(x)}$為質數計數函數，也就是小於$x$的質數個數。

則若$x \rightarrow \infty$，$\displaystyle \lim_{x\rightarrow \infty} \dfrac{\pi(x)}{\dfrac{x}{\ln(x)}} \approx 1$

這個定理告訴我們，若要尋找所有不超過$x$的質數，則他的數量會趨近於$\dfrac{x}{\ln(x)}$

若我們要從所有小於$x$的正整數中挑中質數，則他的機率為$\dfrac{x}{\ln(x)} \div x = \dfrac{1}{\ln(x)}$



#### Definition - 最大公因數

令$a, b$為兩整數，且$a, b \neq 0$，若存在一個最大的整數$d$使得$d | a$且$d|b$，則$d$被稱做$a, b$的最大公因數。

最大公因數$a, b$被寫作$gcd(a,  b)$。



#### Definition - 互質

令$a, b$為兩整數，若$gcd(a, b) = 1$，則我們說$a, b$互質。



#### Definition - 兩兩互質

若有一整數數列$a_1, a_2, a_3, a_4, ... ,a_n$，若$gcd(a_i, a_j) = 1, 1 <= i < j <= n$，則我們說這個數列兩兩互質。



#### Introduce - 利用質因數分解尋找最大公因數

假設$a = p_1^{a_1} p_2^{a_2} p_3^{a_3} ... p_n^{a_n}$，且$b = p_1^{b_1} p_2^{b_2} p_3^{b_3} ... p_n^{b_n}$

則兩數的$gcd(a, b) = p_1^{\min(a_1, b_1)} p_2^{\min(a_2, b_2)} p_3^{\min(a_3, b_3)} ... p_n^{\min(a_n, b_n)} $



#### Definition - 最小公倍數

令$a, b$為兩正整數，若存在一個$d$使得$a|d$且$b|d$，則我們說$d$為$a, b$的最小公倍數。

最小公倍數$a, b$被寫作$lcm(a, b)$

我們可以用質因數分解來尋找最小公倍數，也就是

假設$a = p_1^{a_1} p_2^{a_2} p_3^{a_3} ... p_n^{a_n}$，且$b = p_1^{b_1} p_2^{b_2} p_3^{b_3} ... p_n^{b_n}$

則兩數的$lcm(a, b) = p_1^{\max(a_1, b_1)} p_2^{\max(a_2, b_2)} p_3^{\max(a_3, b_3)} ... p_n^{\max(a_n, b_n)} $



#### Theorem 4

令$a, b$為正整數，則$ab = gcd(a, b) \times lcm(a, b)$



##### Proof

待補



#### Introduce - 歐幾里得演算法

我們可以用歐幾里得演算法來計算$a, b$的最大公因數

論點建立在$gcd(a, b) = gcd(b, c), a>b$，其中$c$為$a$除以$b$的餘數。



#### Introduce - 歐幾里得演算法的正確性

##### 引理1

令$a = bq + r$，其中$a, b, q, r \in \mathbb{Z}$，則$gcd(a, b) = gcd(b, r)$。

##### 證明

假設$d$能夠整除$a, b$，則$d$也可以整除$a- bq= r$，因此，若$gcd(a, b) = d_1$，則$gcd(b, r)=d_1$

假設$d$能夠整除$b, r$，則$d$也可以整除$bq+r=a$，因此，若$gcd(b, r) = d_2$，則$gcd(a, b) =d_2$

因此，$gcd(a, b) = gcd(b, r)$。



### Introduce - 歐幾里得演算法

歐幾里得演算法可以用來計算兩個整數$(a, b)$的最大公因數。

概念建立在$\gcd(a, b) = \gcd(b, c)$，其中$a > b$且$c$為$a$除$b$的餘數。



#### Example

Find $\gcd (91, 287)$



$287 = 91 \times 3 + 14$

$91 = 14\times 6 + 7$

$14 = 7\times 2 + 0$



因此$\gcd(91, 287) = \gcd(91, 14) = \gcd(14, 7) = 7$



### Introduce - 引理 1

令$a = bq+r$，其中$a, b, q, r \in \mathbb{R}$，則$\gcd(a, b) = \gcd(b, r)$



#### Proof

假設$d$可以整除$a, b$，則$d$也可以整除$a - bq = r$。

因此若$a, b$存在一公因數，則此公因數也是$b, r$的公因數。

假設$d$可以整除$b, r$，則$d$也可以整除$bq + r = a$。

因此若$a, b$存在一公因數，則此公因數也是$b, r$的公因數。

因此，$\gcd(a, b) = \gcd(b, r)$



### Introduce -  歐幾里得演算法的正確

假設$a, b$為正整數，且$a \ge b$，令$r_0 = a, r_1 = b$，則我們可以透過除法定理得到以下步驟。

$r_0 = r_1q_1 + r_2$

$r_1 = r_2q_2 + r_3$

$r_2 = r_3q_3 + r_4$

重複多次後

$r_{n-2} = r_{n-1}q_{n-1} + r_n$

$r_{n-1} = r_nq_n$

則我們可以知道，餘數隨著步驟越來越多，得到以下結果：

$r_0 > r_1 > r_2 > r_3 ... \ge 0$

則根據引理1，得到

$\gcd(a, b) = \gcd(r_0, r_1) = \gcd(r_1, r_2) = ... =\gcd(r_{n-1},r_n) = \gcd(r_n, 0) = r_n$

因此最大公因數發生在最後一個非零的餘數。



### Introduce - 貝祖定理

如果$a, b$為正整數，則存在一組$s,t $使得$gcd(a, b) = as + bt$



#### Example

$\gcd(6, 14) = 2 = 6\times (-2) + 14\times 1$



#### Example

利用歐幾里得演算法，將$\gcd(252, 198) = 18$利用線性組合找出$s, t$，使得$252s + 198t = \gcd(252, 198) = 18$



$252 = 198 \times 1 + 54$

$198 = 54\times 3 + 36$

$54 = 36\times 1 + 18$

$36 = 18 \times 2 + 0$

又

$18 = 54 - 36$

$= 54 - (198-54\times 3) = 54\times 4 - 198$

$= (252-198)\times 4 - 198 = 4\times 252 - 5\times 198$

故我們可以找到$s = 4, t = -5$，使得$\gcd(252, 198) = 4\times 252 - 5\times 198$



我們可以整理成以下的表格

| $j$  | $r_j$ | $r_{j+1}$ | $q_{j+1}$ | $r_{j+2}$ |
| ---- | ----- | --------- | --------- | --------- |
| 0    | 252   | 198       | 1         | 54        |
| 1    | 198   | 54        | 3         | 36        |
| 2    | 54    | 36        | 1         | 18        |
| 3    | 36    | 18        | 2         | 0         |



### Introduce - 歐幾里得擴展演算法

若我們已經找到足夠的$q$，則我們可以將$s, t$擴展成以下的遞迴式。

$s_j = s_{j-2} - q_{j-1}s_{j-1}$和$t_j = t_{j-2}-q_{j-1}t_{j-1}, j \ge 2$

其中$s_0 = 1, s_1 = 0, t_0 = 0, t_1 = 1$



#### Example

利用歐幾里得擴展，尋找出$s, t$使得$\gcd(252,198) = 252\times s + 198\times t$



$s_2 = s_0 - q_1 s_1 = 1 - 1\times 0 = 1$

$t_2 = t_0 - q_1t_1 = 0 - 1\times1 = -1$

$s_3 = s_1 - q_2s_2 = 0 - 3\times1 = -3$

$t_3 =t_1 - q_2t_2 = 1 - 3\times (-1) = 4$

$s_4 = s_2 - q_3s_3 = 1 - 1\times (-3) = \color{red}{4}$

$t_4 = t_2 - q_3 t_3 = -1 - 1\times 4 = \color{red}{-5}$



因此，我們可以知道$s = 4, t = -5$時符合$\gcd(252, 198) = 4\times 252 - 5\times 198 = 18$



### Introduce - 引理 2

如果$a, b, c$為正整數，且$\gcd(a, b) = 1$而且$a | bc$，則$a | c$



#### Proof

假設$\gcd(a, b) = 1$，且$a | bc$，則

根據貝祖定理，存在一組$(s, t)$使得$\gcd(a, b) = as + bt = 1$

將等號兩邊同乘以$c$，則得到$asc + btc = c$

已知$a|bc$，代表存在一個$r$使得$bc = ar$，將等號兩邊同乘$t$，可以得到$btc = art \Longleftrightarrow  btc = a(rt)$，故$a|btc$

又已知$asc$可被$a$整除($asc/a = sc, sc \in \mathbb{R})$，故$a | asc, a|btc \Rightarrow a|c$



### Introduce - 引理3

假設$p$是質數，且$p | a_1 a_2 a_3 ... a_n$，則對於某些$i$，$p | a_i$



### Introduce - 質數分解的唯一性

若一個數字可被質數分解，且分解的結果為非遞增的方式排列，則這個結果為唯一。



#### Proof

假設有些大於1的自然數可以用多種方式寫成多個質數的乘積

則假設$n$為最小可以用多種方式寫成多個質數的乘積的數字。

因此我們可以將$n$寫成$n = p_1p_2p_3p_4...p_s = q_1q_2q_3q_4...q_t$，$p, q$為質數。

根據引理$3$，假設$p$是質數，且$p | a_1 a_2 a_3 ... a_n$，則對於某些$i$，$p | a_i$

因此$q_1q_2q_3 ... q_t$存在一個數字使得$p_1$可以整除，假設為$q_1$

又若要使得$p_1 |q_1$，只存在於$p_1 = q_1$。

所以$n' = p_2p_3p_4p_5...p_s = q_2q_3q_4q_5...q_t$

但$n$是最小的一個，不應該存在比$n$更小的數字$n'$能夠用多種方式寫成多個質數的乘積

故與$n$的最小性矛盾，因此唯一性得證。



### Theorem 5

在先前有介紹過同餘的除法代數運算並不適用於每一種結果，在這邊會介紹同餘的除法代數運算。

令$m$為一正整數，且$a, b, c$為整數，則若$ac \equiv bc \pmod m$和$\gcd(c,m) = 1$，則$a \equiv b \pmod m$。



#### Proof

若$ac \equiv bc \pmod m$，則$ac = mr + bc$，$ac - bc = mr$，$r = \dfrac{(ac-bc)}{m} = \dfrac{ac}{m}-\dfrac{bc}{m}$

利用引理2可知

若$m | ac$且$\gcd(m, c)$，則$m | a$

若$m | bc$且$\gcd(m, c)$，則$m | b$

又因$m | a, m | b$，則$a \equiv b \pmod m$



### 4.4 求解同餘方程式

#### Introduce - 線性同餘

當$m$為正整數，$a, b$為整數，而$x$為變數時，$ax \equiv b \pmod m$稱為線性同餘。



#### Definition - 反元素

若存在一個整數$\overline{a}$，使得$\overline{a}a \equiv 1$，則我們說$\overline{a}$為模$m$的反元素。



#### Theorem 1

若$a$與$m$為互質整數，且$m > 1$，則$a$在模$m$下的反元素存在，此外，在模$m$下，此反元素是唯一的。



##### Proof (存在性)

利用定理：若$\gcd(a, m) = 1$，則存在兩整數$s, t$使得$as + mt = 1$，也可以看成$as + mt \equiv 1 \pmod m$

由於$mt \equiv 0 \pmod m$，因此$as \equiv 1 \pmod m$

因此，$s$是$a$在模$m$的反元素。



#### Introduce - 找出反元素

我們可以用歐幾里得演算法與貝祖定理來找出反元素。

首先我們必須要證明$\gcd(a, b) = 1$，再利用貝祖定理做回推。



##### Example 1

尋找3模7的反元素。

根據歐幾里得演算法：

$7 = 3\times 2 + 1$

$3 = 1\times 3 + 0$

因此我們能夠證明$\gcd(7, 3) = 1$



接著利用貝祖定理進行回推，可得$-2\times 3 + 1\times 7 = 1$

因此可以得到貝祖係數$s = -2, t = 1$

因此，$-2$是3模7的反元素，而所有結果為$-2$模7同餘的整數皆為3模7的反元素。



##### Example 2

尋找101模4620的反元素。

根據歐幾里得演算法：

$4620 = 101\times 45 + 75$

$101 = 75\times 1 + 26$

$75 = 26\times 2 + 23$

$26 = 23\times 1 + 3$

$23 = 3\times 7 + 2$

$3 = 2\times 1 + 1$

$2 = 1\times 2 + 0$

故我們可以證明$\gcd(101, 4620) = 1$



利用這個來反推貝祖係數

$1 = 3 - 2\times 1$

$= 3 - (23 - 3\times 7) = 3\times 8 - 23$

$= (26-23)\times 8 - 23 = 8\times 26 - 9\times 23$

$= 8\times 26 - 9\times(75-26\times 2) = 26\times 26 - 9\times 75$

$= (101-75)\times 26 - 9\times 75 = 101\times 26 - 35\times 75$

$= 101\times 26 - 35\times(4620-101\times 45)$

$= 101\times 1601 - 35\times 4620$

故我們可以得到$s = 1601, t = -35$

故我們說1601為101模4620的反元素。



#### Introduce - 中國剩餘定理

令$m_1, m_2, m_3, ..., m_n$為兩兩互質的正整數，而$a_1, a_2, a_3, ..., a_n$為任意正整數，則下列系統

$\left\{\begin{array}\ x \equiv a_1 \pmod {m_1} \\ x \equiv a_2 \pmod {m_2} \\ x \equiv a_3 \pmod {m_3} \\ . \\. \\. \\ x \equiv a_n \pmod {m_n} \end{array}\right.$

在$m = m_1 m_2 m_3 m_4 ... m_n$有唯一解，其中$0 \le x < m$，而其他解都在$x$模$m$的情況下同餘。



##### Proof

我們設$M_k = m/m_k$，其中$k = 1, 2, 3 ... n$，也就是說$M_k$為除了$m_k$以外的所有兩兩互質正整數乘積。

當$i \neq k$時，$M_k$與$m_k$沒有公因數，故$\gcd(M_k, m_k) = 1$

根據Theorem 1，可知存在一個反元素使得$M_k y_k \equiv 1 \pmod{m_k}$

令$x = a_1M_1y_1 + a_2M_2y_2 + ... +a_nM_ny_n$，因為$M_j \equiv 0 \pmod{m_k}$，其中$j \neq k$

因此，對所有的$k = 1, 2, 3, ..., n$，得到$x \equiv a_k M_k y_k \equiv a_k \pmod{m_k}$，因此$x$即為方程式系統的解。



##### Example

求解下列同餘方程式系統。

$\left\{\begin{array}\ x \equiv 2 \pmod 3 \\ x \equiv 3 \pmod 5 \\ x \equiv 2 \pmod 7 \end{array}\right.$



$m = 3\times 5\times 7$

則

$M_1 = 5\times 7 = 35$，$35 y_1 \equiv 1 \pmod 3$，得到$y_1 = 2$

$M_2 = 3\times 7 = 21$，$21 y_2 \equiv 1 \pmod 5$，得到$y_2 = 1$

$M_3 = 3\times 5 = 15$，$15y_3 \equiv 1 \pmod 7$，得到$y_3 = 1$

因此$x = 35\times2\times 2 + 21\times 1\times 3 + 15\times 1\times 2 = 233 \equiv 23 \pmod{105}$

故$x = 23$為這個系統的最小正整數解。



#### Introduce - 回朔代換

我們可以用回朔代換來解中國剩餘問題。

已知$a \equiv b \pmod m$，則我們可以知道存在一個$k$使得$a = k\times m + b$，$k \in \mathbb{Z}$

因此我們可以假設並且代換。



##### Example

利用回朔代換的方法來找到所有的整數$x$，使得$x \equiv 1 \pmod 5$，$x \equiv 2 \pmod 6$，$x \equiv 3 \pmod 7$



假設$x = 5t + 1, t\in\mathbb{Z}$，則我們可知$5t+1 \equiv 2 \pmod 6 \Longleftrightarrow 5t \equiv 1\pmod 6$

- 利用尋找反元素的方法求得貝祖係數

  $\gcd(5, 6) = 1$，因此我們可以寫成

  $6 = 5\times 1 + 1$

  所以$6\times 1 - 5\times 1 = 1$

  因此我們可以知道貝祖係數為$(-1, 1)$，可知$t \equiv -1 \pmod 6$，因此我們假設$t \equiv 5$。

我們假設$t = 6u + 5$，利用代換回$5t+1$可得$x = 30u+26$

接著我們假設$30u +26 \equiv 3 \pmod 7 \Longleftrightarrow 30u \equiv 4 \pmod 7$

- 利用尋找反元素的方法求得貝祖係數

  $\gcd(30, 7) = 1$，因此我們可以寫成

  $30 = 7\times 4 + 2$

  $7 = 2\times 3 + 1$

  所以$7 - 2\times 3 = 1$

  再代換得到$7 - (30-7\times 4)\times 3 = 1 \Longleftrightarrow 7\times13-30\times3 = 1$

  因此我們可以知道貝祖係數為$(13, -3)$，則可知$u \equiv 13 \equiv 6 \pmod 7$

我們假設$u = 7v + 6$，利用代換可知$x = 30(7v+6)+26 = 210v+206$

因此我們可以知道$x \equiv 206 \pmod{210}$



#### Introduce - 費馬小定理

如果$p$是質數，且$a$是整數，$p \not |\space \space  a$，那麼$a^{p-1} \equiv 1 \pmod p$

費馬小定理可以幫助我們求得指數非常大的數字模$p$的結果，見以下範例。



##### Example

計算出$7^{222} \text{ mod } 11$



$7^{222} \text{ mod } 11 = [(7^{22})^{10}\times 7^2]\ \text{ mod } 11 = [1^{10}\times7^2] \text{ mod }11 = 5$



#### Introduce - 底數為2偽質數

根據費馬小定理，因為$2^{n-1} \equiv 1 \pmod n$，則$n>2$皆為質數。

但根據這個模的結果，$n$未必會是質數（下面會給一個反例）。

若存在一個合數使得$2^{n-1} \equiv 1 \pmod n$成立，則我們說$n$為底數為$2$的偽質數。



##### Example

$341$是底數為$2$的偽質數。



$341 = 11\times 13$，因此$\gcd(2, 341) = 1$。

因此根據費馬小定理$2^{340} \equiv 1 \pmod {341}$。



#### Introduce - 底數為b的偽質數

令$b$為一正整數，如果$n$為合數且使得$b^{n-1} \equiv 1 \pmod n$成立，則我們說$n$是底數為$b$的偽質數。



#### Introduce - 卡邁爾數 (Optional)

令$n$為一正合數，若對於所有符合$\gcd(b, n)=1$的$b$，使得$b^{n-1} \equiv 1 \pmod n$，則我們說$n$為卡邁爾數。



##### Example

$561$是一個卡邁爾數



$561 = 3\times 11\times 17$，且若$\gcd(b, 561) = 1$，則$\gcd(b, 3) = 1, \gcd(b, 11) = 1, \gcd(b, 17) = 1$

因此我們使用費馬小定理，得到$b^2 \equiv 1 \pmod 3$，$b^{10} \equiv 1 \pmod {11}$，$b^{16} \equiv 1 \pmod {17}$

得到$b^{560} = (b^2)^{280} \equiv 1 \pmod 3$，$b^{560} = (b^{10})^{56} \equiv 1 \pmod {11}$，$(b^{16})^{35} \equiv 1 \pmod {17}$

因此$b^{560} \equiv 1 \pmod {561}$成立，所以$561$是卡邁爾數。



#### Introduce - 原根

對於一個質數$p$, 定義模$p$下的原根如下: 

若$r$為$\mathbb{Z}_p$中的一個元素，設有一集合$A = \{r^k \text{ mod } p | 0<k<p\}$，且集合$A$與集合$\mathbb{Z}_p$中的非零整數一一對應，則我們說$r$為模$p$的原根。



##### Example

$2$為模$11$的原根。



$2^1 \mod 11 = 2$，$2^2 \mod 11 = 4$，$2^3 \mod 11 = 8$，$2^4 \mod 11 = 5$

$2^5 \mod 11 = 10$，$2^6 \mod 11 = 9$，$2^7 \mod 11 = 7$，$2^8 \mod 11 = 3$

$2^9 \mod 11 = 6$，$2^{10} \mod 11 = 1$



#### Introduce - 離散對數

假設$p$是一個質數，$r$是一個模$p$下的原根，而$a$是介於$1$和$p-1$之間的一個整數。

如果$r^e \mod p = a$，其中$0 \le e < p$，則我們說$e$是以$r$為底$a$模$p$的離散對數，寫作$\log_r a = e$

($p$為已知的質數)



##### Example 1

試找出以$2$為底的$3$模$11$的離散對數。



$\because 2^8 \mod 11 = 3$

$\therefore \log_2 3 = 8$



##### Example 2

試找出以$2$為底的$5$模$11$的離散對數。



$\because 2^4 \mod 11 = 5$

$\therefore \log_2 5 = 4$



### 4.5 同餘應用


#### Introduce - 雜湊函數

雜湊函數的概念是，使用者丟入key後，會透過雜湊函數產生出一個不可逆的值(value)。

且雜湊函數是蓋射，故對於一個key，對應到一個value，但有可能多個key對應到同一個value，這就是雜湊碰撞。



我們可以用這樣的函數來表示雜湊函數，也就是

$h(k) = k \mod m$



當發生碰撞時，我們可以用線性探測來排除，也就是

$h(k, i) = (h(k)+i) \mod m$，而$i$從$0$跑到$m-1$



#### Introduce - 偽隨機數

我們用線性同餘法來製作出偽隨機數。

我們會需要三個要素：模數$m$，乘數$a$，增加的數字$c$，以及種子$x_0$

則我們可以用以下的遞迴式來製作偽隨機數。

$x_{n+1} \equiv (ax_n + c) \mod m$

產出來的偽隨機數範圍會在$0\sim m-1$。

如果我們需要介於$0$到$1$的偽隨機數，我們可以將產出來的偽隨機數除以模數$m$，也就是$x_i/m$



##### Example

假設$m=9$，$a=7$，$c=4$，$x_0 = 3$，找出偽隨機數的數列。

則$x_1 \equiv (7\times 3 + 4) \pmod 9 \equiv 7 \pmod 9$

$x_2 \equiv (7\times 7 + 4) \pmod 9 \equiv 8 \pmod 9$

$x_3 \equiv (7\times 8 + 4) \pmod 9 \equiv 6 \pmod 9$

$x_4 \equiv (7\times 6 + 4) \pmod 9 \equiv 1 \pmod 9$

$x_5 \equiv (7\times 1 + 4) \pmod 9 \equiv 2 \pmod 9$

$x_6 \equiv (7\times 2 + 4) \pmod 9 \equiv 0 \pmod 9$

$x_7 \equiv (7\times 0 + 4) \pmod 9 \equiv 4 \pmod 9$

$x_8 \equiv (7\times 4 + 4) \pmod 9 \equiv 5 \pmod 9$

$x_9 \equiv (7\times 5 + 4) \pmod 9 \equiv 3 \pmod 9$

因此偽隨機數的序列會是$\{7,8,6,1,2,0,4,5,3,7,8,6,1,2,0,4,5,3...\}$



### 4.6 密碼學

#### Introduce - 凱薩密碼

凱薩密碼是指將一串英文的每個單字遞增或遞減m次(例如A->B, B->C，或者B->A, A->Z)，作法如下。



1. 把所有英文字母用$\mathbb{Z}_{26}$作替代，也就是用0~25替代每一個英文字母
2. 加密函數就是$f(p) = (p+m) \mod 26$，因此$f(p)$的值域也為0~25
3. 接著把所有的整數轉回英文字母。



如果凱薩密碼要進行還原，則我們只需要將所有字母位移的部分移回去。

因此我們可以得到解密函數$f^{-1}(p) = (p - m) \mod 26$

對於凱薩密碼來說，$m$就是解開凱薩密碼的鑰匙。



##### Example

嘗試用凱薩加密法加密「MEET YOU IN THE PARK」。



先將「MEET YOU IN THE PARK」轉成數字，也就是「12 4 4 19  24 14 20  8 13  19 7 4  15 0 17 10」

接著假設$m=3$，那我們將每個數字套用加密函數，得到加密後的訊息「15 7 7 22  27 17 23  11 16  22 10 7  18 3 20 13」

接著將訊息還原成英文字母，也就是「PHHW BRX LQ WKH SDUN」



#### Introduce - 仿射密碼法

我們可以用$f(p) = (ap+b) \mod 26$來增加其安全性。

設定整數$a, b$讓$f(p)$變成雙射函數，函數$f(p)$為雙射函數若且唯若$\gcd(a, 26) = 1$

這樣的函數叫做仿射轉換，而這樣的加密方式被稱為仿射密碼法。



解密這樣的密碼法，首先我們設有一整數$c$，且$c = (ap+b)\mod 26$

已知$\gcd(a, 26) = 1$，則我們可以利用同餘方程式，得到$c \equiv (ap+b) \pmod{26}$

接下來的目標式解出$p$，所以我們將等式兩端減去$b$，得到$(c-b) \equiv ap \pmod{26}$

則由於$\gcd(a, 26) = 1$，所以可以找到一個反元素$\overline{a}$使得$a\overline{a} \equiv 1 \pmod{26}$

我們在等式兩端乘上$\overline{a}$，得到$\overline{a}(c-b) \equiv a\overline{a} p \pmod{26}$

得到$\overline{a}(c-b) \equiv p \pmod{26}$



##### 仿設密碼法的密碼分析

分析位移密碼法最主要的工具是計算密文中字母出現的頻率。

若出現的次數最多的字母為E，則有可能就是從E去做位移的，因此我們可以考慮從E下手。

若還原出來的東西毫無意義，可以選擇其他的字母嘗試進行還原。





#### Introduce - 區塊密碼法

我們可以把字串分成一個一個區塊，針對於每個區塊去進行加密，見以下的轉換密碼法。



#### Introduce - 轉換密碼法

轉換密碼法是區塊密碼法的其中一種。

利用一個集合$\{1, 2, 3, ... , m\}$的排列函數$\sigma$當成密鑰。

首先先將訊息字母分成$m$個字的區塊，如果不滿$m$個字可以隨意在尾端加上幾個字。

接下來對於每一個區塊中的字母$p_1p_2p_3...p_m$，編碼成$c_1c_2c_3...c_m = p_{\sigma(1)}p_{\sigma(2)}p_{\sigma(3)}...p_{\sigma{(m)}}$

解碼時則必須要找到$\sigma^{-1}$。



##### Example

根據集合$\{1, 2, 3, 4\}$的排列函數$\sigma(1) = 3, \sigma(2) = 1, \sigma(3) = 4$以及$\sigma(4) = 2$執行轉換密碼法。

(a) 將明文$\text{PIRATE ATTACK}$編碼

(b) 將明文$\text{SWUE TRAE OEHS}$解碼



將$\text{PIRATE ATTACK}$分成$m$個字的區塊，得到$\text{PIRE TEAT TACK}$

接著利用排列函數做替換，得到$\text{IEPR ETTA AKTC}$，即為加密後的密文。



利用排列函數來反向替換，把明文$\text{SWUE TRAE OEHS}$進行解密，得到$\text{USEU ATER HOSE}$



#### Introduce - 密碼系統

一個密碼系統包含了五個集合$(\text{P, C, K, E, D})$，其中$\text{P}$為明文字串所形成的集合，$\text{C}$為密文字串所形成的集合。

$\text{K}$為密鑰空間，$\text{E}$為編碼函數所形成的集合，而$\text{D}$為解碼函數所形成的集合。

$E_k$表示在$E$中與密鑰$k$相關的編碼函數

對於所有的明文字串$p$，$D_k(E_k(p)) = p$。



#### Introduce - 私密金鑰密碼系統

在私密金鑰密碼系統中，如果知道加密的密鑰，則便能很快地找到解密的密鑰。

例如，使用平移密碼，只要找出平移的數量$k$，反向操作一次就能找到解密的訊息。

在使用私密金鑰系統時，秘密互通的兩方都必須各自擁有密鑰，且擁有密鑰的人都能解開訊息。

因此秘密通訊的兩人必須要私下交換對方的加密金鑰，而類似平移密碼法或者仿射密碼法皆很容易被解開。



#### Introduce - 公開金鑰密碼系統

為了避免互通訊息的每一方都需要私下交換對方的加密金鑰，而衍伸出了公開金鑰密碼系統。

在公開金鑰密碼系統，知道訊息如何加密並無助於解密，且在此系統下，每個人都知道加密的金鑰，但是解密金鑰則是秘密的。

只有指定的接收者能獲得解密金鑰，並且用其解開訊息。

而若非指定的接收者鑰獲得解密金鑰，則需要需要經過非常複雜的運算，才能得到解密金鑰，光是用電腦運算就需要10億年的時間。



#### Introduce - RSA加密系統

在RSA加密系統中，每個人都能使用公開的金鑰$(n, e)$來編碼，其中$n = pq$，$p, q$為兩個長達200位的質數。

而使用來做底數的$e$與$(p-1)(r-1)$互質，為了產生一個有效的金鑰，則需要兩個很大的質數來進行加密。

經過這個加密的$n$近乎400位數，因此要在有限的時間內質因數分解這個$n$近乎不可能。

因此若沒有解密金鑰，則要快速獲得金鑰基本上是很困難的事情。



#### Introduce - RSA加密法

在使用公開金鑰$(n, e)$的RSA加密法中，首先訊息$M$被轉換成一個整數字串，每個字母轉換成一個兩位數的整數。

將這些數字字串分割成$2N$的區塊$m$，形成較大的整數，其中$2N$是一個小於$n$的偶數。

如果$M$的長度不足$2N$，則可以在尾端加入許多多餘字母。

經過以上的步驟後，我們有數字區塊$m_1m_2 m_3 m_4...m_k$，其中$k$為正整數。

接下來對於每一個區塊，我們利用以下的函數加密：

$C = m^e \mod n$

將密文以數字區塊的方式丟給指定的接收者，由於RSA把一個一個區塊加密，所以RSA也是一種區塊加密法。



#### Introduce - RSA解密法

如果知道$(p-1)(q-1)$下$e$的反元素，也就是解密金鑰$d$，那麼就能很快地找出明文。

$d$必定會存在，因為$\gcd(e, (p-1)(q-1)) = 1$，因此反元素存在。

也就是若$de \equiv 1 \pmod{(p-1)(q-1)}$，則存在一個$k$，使得$de = 1 + k(p-1)(q-1)$

因此$C^d \equiv (M^e)^d = M^{de} = M^{1+k(p-1)(q-1)} \pmod n$

根據費馬小定理（若$\gcd(M, p) = \gcd(M, q)$均成立，則在大部分的情況下都會成立）

則有$M^{p-1} \equiv 1 \pmod p$，與$M^{q-1} \equiv 1 \pmod p$

則$C^d \equiv M \cdot (M^{(p-1)})^{k(q-1)} \pmod p \equiv M \cdot 1 = M \pmod p$

$C^d \equiv M \cdot (M^{(q-1)})^{k(p-1)} \pmod q \equiv M \cdot 1 = M \pmod q$

因為$\gcd(p, q) = 1$，根據中國剩餘定理，存在唯一一個$M$，使得$C^d \equiv M \pmod {pq}$



#### Introduce - 密鑰交換

在這邊討論一種方法，能夠使得接收方與傳送方不需要分享任何資訊，便能透過公開管道來交換密鑰。

假設接收方與傳送方要分享一個共同的金鑰，則他們的交換方法有以下幾個步驟，均在集合$\mathbb{Z}_p$中。

1. 接收方與傳送方決定好一個質數$p$與一個原根$a$
2. 傳送方選擇一個數字$k_1$，計算$a^{k_1} \mod p$，然後把值傳送給接收方
3. 接收方選擇一個數字$k_2$，計算$a^{k_2} \mod p$，然後把值傳送給傳送方
4. 接收方計算$(a^{k2})^{k1}$
5. 傳送方計算$(a^{k1})^{k2}$
6. 最後，他們能夠擁有共同的金鑰，因為$(a^{k2})^{k1} \pmod p = (a^{k1})^{k2} \pmod p$

要從$a^{k2} \pmod p$推出$k2$，與從$a^{k1} \pmod p$推出$k1$，必須反推解出離散對數問題。

在$p$與$a$非常大的情況下，計算基本上無法執行，因此利用公開訊息推出私密訊息是近乎不可能的。





#### Introduce - 數位簽章

假設傳送方的RSA公開金鑰為$(n, e)$，而私密金鑰為$d$，則他能使用函數$E_{(n, e)} (x) = x^e \mod n$為明文$n$加密。

而收到密文$y$後，便可以使用$D_{(n, e)} (y) = y^d \mod n$解密。

當傳送方要將訊息$M$傳送給接收方，則他可以使用像RSA的分塊方式。

先將訊息轉成數字後，分塊成數個區塊$m_1, m_2, m_3, ... , m_k$，其中$0 \le m_i \le n$，$i = 1, 2, 3, ... , k$。

接下來將他的解密函數運作在所有的區塊上，得到$D_{(n, e)}(m_i)$，傳送給接收方。

當接收方接收到了加密後的訊息後，只需要利用公開的加密函數來解密，得到$E_{(n, e)}(D_{(n, e)}(x)) = x$

因此這樣就能確定訊息來自傳送方了。



## 5. 歸納與遞迴

### 5.1 數學歸納法

#### Introduce - 數學歸納法的原理

為了證明對於所有的$P(n)$為真，$n \in \mathbb{Z}, n > 0$，則我們需要完成兩個步驟：

1. 基礎步驟：證明$P(1)$為真
2. 歸納步驟：證明$P(k) \rightarrow P(k+1)$，$k \in \mathbb{Z}, k > 0$為真。

在歸納證明中，$p(k)$為歸納假設，我們必須要假設$P(k)$為真，接著證明$P(k+1)$也為真。

數學歸納法可以被轉成以下的推論：

$(P(1) \and \forall k (P(k) \rightarrow P(k+1))) \rightarrow \forall n P(n)$，其中這個推論的定義域為正整數。

在數學歸納的證明，我們並不會假設所有的$P(k)$皆為真，我們會假設$P(k)$為真，來證明$P(k+1)$也為真。

在數學歸納的證明，起始的數字也不一定會是$1$，可以是某個整數$b$。



##### Example 1

證明$\displaystyle \sum^n_{i=1} = \dfrac{n(n+1)}{2}$



基礎步驟：證明$P(1)$為真，把$1$帶進去後得到$\dfrac{1(1+1)}{2} = 1$

歸納步驟：假設$P(k)$為真，則$1 + 2 + ... + k + (k+1) = \dfrac{k(k+1)}{2} + (k+1)$

$= \dfrac{k(k+1)+2(k+1)}{2} = \dfrac{(k+1)(k+2)}{2}$

因此，對於所有的正整數$n$，$P(n)$為真。



##### Example 2

猜出一個式子能夠證明前$n$個正整數奇數的和，然後證明式子是正確的



$1=1$，$1+3=4$，$1+3+5=9$，$1+3+5+7=16$

因此我們可以猜，若$n$代表前$n$個奇數的和，則$P(n)=n^2$



利用數學歸納法來證明式子是正確的

基礎步驟：$P(1)=1$

歸納步驟，假設$P(k)$為真

$1+3+5+7+...+(2k-1)+(2k+1) = [1+3+5+...+(2k-1)]+(2k+1)$

$= k^2+(2k+1)$ (因為歸納假設)

$= k^2+2k+1$

$= (k+1)^2$

因此，對於所有正整數$k$，$P(k)$皆為真，因此前$n$個正整數奇數的和為$n^2$。



##### Example 3

利用數學歸納法來證明對於所有的正整數$n$，$n<2^n$



令$P(n)$為$n<2^n$的命題，則

基礎步驟：$P(1)$為真，因為$1<2$

歸納步驟：假設$P(k)$為真，則對於任意的$k$，使得$k<2^k$

證明$P(k+1)$，則$k+1 < 2^k + 1 \le 2^k+2^k = 2\times 2^k = 2^{k+1}$

因此對於所有的正整數$n$，$n<2^n$。



##### Example 4

利用數學歸納法證明，對於所有$n\ge 4$，$2^n < n!$



令$P(n)$為$2^n<n!$的命題，則

基礎步驟：$P(4)$為真，因為$2^4=16<4!=24$

歸納步驟：假設$P(k)$為真，得到任意的$k\ge4$使得$2^k < k!$

為了證明$P(k+1)$為真，我們得到$2^{k+1}=2\times 2^k$

根據歸納假設，得到$2^{k+1} < 2\times k! < (k+1)\times k! < (k+1)!$

因此，對於任意的$k\ge4$，$2^n<n!$均成立。



##### Example 5

利用數學歸納法證明對於任意的正整數$n$，$n^3-n$可被$3$整除。



令$P(n)$為$n^3-n$的命題，則

基礎步驟：$P(1)$為真，因為$1^3-1 = 0$，$0 \mod 3 = 0$

歸納步驟：假設$P(k)$為真，那麼$k^3-k$可被$3$整除

為了證明$P(k+1)$為真，有

$(k+1)^3-(k+1) = k^3+3k^2+3k+1 - k-1 = k^3+3k^2+2k$

$= (k^3-k)+3k^2+3k = (k^3-k)+3(k^2+k)$

根據歸納假設，已知$(k^3-k)$可被$3$整除，第二項為三的倍數，因此也必定能被$3$整除。

因此，對於任意的正整數$n$，$P(n)$均成立。



##### Example 6

利用數學歸納法來證明如果$S$是有限集合，有$n$個元素，且$n$為非負整數，則$S$有$2^n$個子集合。



令$P(n)$為一命題，代表如果$S$是有限集合，有$n$個元素，且$n$為非負整數，則$S$有$2^n$個子集合。

基礎步驟：$P(0)$為真，因為$2^0=1$，空集合的子集合只有自己本身。

歸納步驟：假設$P(k)$為真，那麼令$T$為一集合，有$k+1$個元素，那麼$T = S \cup \{a\}$

其中$a \in T$，且$S = T - \{a\}$，那麼$|S| = k$

如果$T=S\cup\{a\}$，那麼$T$的子集有兩種可能：包含$a$或者不包含$a$

透過之前的歸納假設已知$S$的子集合有$2^k$個，則我們可以知道$T$的子集合數量為$2\times 2^k = 2^{k+1}$

因此，對於任意的非負整數$n$，$P(n)$均成立。



##### Example 7

證明在$2^n\times 2^n$的棋盤上，刪去一個方格後可以用三格板填滿棋盤。



設$P(n)$的命題為在$2^n\times 2^n$的棋盤上，刪去一個方格後可以用三格板填滿棋盤。

基礎步驟：$P(1)$為真，列出所有可能的三格板填滿方式，均多一格

![image-20210510092935632](https://i.imgur.com/0Hi8V3v.png)

歸納步驟：假設一個任意的正整數$k$，$P(k)$為真，則

我們考慮$2^{k+1}\times 2^{k+1}$其中一個方格被刪去了，我們分割棋盤變成四個$2^k\times 2^k$的棋盤

![image-20210510093116599](https://i.imgur.com/t7z53Vu.png)

如果我們能夠刪去這四個棋盤的其中一格，那麼根據$P(k)$，$2^{k+1} \times 2^{k+1}$能被填滿

一個棋盤已經被刪去了，我們可以用一塊三格板來占走這三個棋盤，如下

![image-20210510094030478](https://i.imgur.com/BL0HMLm.png)

這樣，四個棋盤都至少被占走一格，根據歸納假設可以知道這四個棋盤被占走一格，因此能夠被填滿

因此，$2^{k+1}\times 2^{k+1}$可以被三格板填滿



##### Example 8

利用數學歸納法，證明對於所有大於等於$12$的數字$n$，可以用$4$與$5$來湊成。



令$P(n)$為一命題，代表對於數字$n$，可以用$4$和$5$來湊成。

基礎步驟：$P(12)$為真，因為可以用3個$4$來湊成。

歸納步驟：假設$P(k)$為真，為了要證明$P(k+1)$為真，我們考慮兩種情況：

1. 如果$k+1$是偶數，那麼當我們全部都用$4$來湊時，會剛好或者多$2$。

   由於數字$n$大於等於12，因此若全部用$4$來湊，則$4$的數量必定大於等於$3$

   因此我們可以把其中兩個$4$替換成兩個$5$，得到多$2$的結果。

2. 如果$k+1$是奇數，那麼當我們全部都用$4$來湊時，會多$1$或者多$3$

   由於數字$n$大於等於12，因此若全部用$4$來湊，則$4$的數量必定大於等於$3$

   因此若是多$1$，只需把其中一個$4$換成$5$即可。

   若是多$3$，只需把其中$3$個$4$換成$5$即可。

綜合以上，可以得到無論$k+1$是奇數或是偶數，$P(k+1)$均成立。

因此，若$n \ge 12$，$P(n)$皆成立。



#### Introduce - 數學歸納法的正確性

數學歸納法能夠正確，主要來自於良序規則，也就是對於所有的非空正整數集合，至少會存在一個最小元素。

數學歸納法的證明如下：

1. 假設知道$P(1)$為真，且對於所有正整數來說，$P(k) \rightarrow P(k+1)$為真。

2. 假設這裡有至少一個正整數$n$能使$P(n)$為假，則我們假設有一正整數非空集合$S$能夠使$P(n)$為假。

3. 根據良序定理，$S$至少有一個最小元素，叫做$m$

4. 我們知道$m$不可能為$1$，因為$P(1)$為真

5. 因為$m$為正整數且大於$1$，所以$m-1$也必定為正整數，因為$m-1 < m$，所以$m-1$必定不在$S$內

   所以$P(m-1)$必定為真

6. 但是對於所有的正整數$k$，$P(k) \rightarrow P(k+1)$為真，所以$P(m)$必定為真，會與$P(m)$為假的結論矛盾。

7. 因此，對於所有的正整數$n$，$P(n)$必定為真。



#### Introduce - 數學歸納證明的模板

1. 將需要證明的命題表示為「對於所有的$n\ge b$，$P(n)$」的形式，$b$為一個固定的整數
2. 寫下基礎步驟，證明$P(b)$為真，注意選擇正確的$b$，這樣就完成了證明的第一步
3. 寫下歸納步驟
4. 明確列出歸納假設，形式是「假設$P(k)$為真，對於任意固定的整數$k \ge b$
5. 列出在歸納假設的前提下需要證明的命題，即寫出$P(k+1)$的含意
6. 採用$P(k)$證明$P(k+1)$，確保對於所有$k$，$k \ge b$，$P(k)$均為真，$k$也有可能等於$b$。



### 5.2 強歸納法

#### Introduce - 強歸納法

證明對於所有的正整數$n$，$P(n)$均為真

其中$P(n)$是一命題，需要完成以下兩個步驟

基礎步驟：證明$P(1)$是真的

歸納步驟：證明對於所有的正整數$k$，$[P(1) \land P(2) \land ... \land P(k)] \rightarrow P(k+1)$為真



##### Example 1

假設有一個無限階梯，我們已知我們可以抵達第一階，就能抵達第二階，利用數學證明法來證明我們可以抵達每一階。



設$P(n)$為一命題，代表我們可以踏上第$n$階階梯

基礎步驟：$P(1)$為真，因為我們可以踏上第一階。

歸納步驟：我們假設$P(k)$為真，代表我們可以踏上前$k$階階梯，那麼對於所有大於等於$2$的正整數$k$，我們可以抵達$k+1$階，只要我們能夠踏上$k-1$階，根據歸納假設可知我們可以抵達$k$階，因此我們可以抵達$k+1$階。

因此，我們可以抵達所有的階梯。



##### Example 2

證明對於大於$1$的整數，$n$可以寫成質數的乘積。



令$P(n)$為一命題，代表整數$n$可以寫成質數的乘積。

基礎步驟：$P(2)$為真，因為$2 = 2$，$2$為質數

歸納步驟：假設$P(k)$為真，則代表$P(j)$皆為真，其中$2 \le j \le k$ 

為了要證明$P(k+1)$為真，則

如果$k+1$是質數，那$P(k+1)$必為真

如果$k+1$不是質數，那麼$k+1$可以寫成兩個數$a, b$乘積的和，也就是$k+1 = a\times b$，也就是$2 \le a, b \le k+1$

根據歸納假設，可以知道$P(a), P(b)$皆為真，因此$k+1$可以被寫成質數的乘積。

因此，$P(k+1)$為真



#### Introduce - 歸納法的使用時機

強歸納法可以取代數學歸納法，但是有的時候很難用強歸納法來證明，用數學歸納法歸納比較簡單的話，就用數學歸納法。



#### Axiom - 良序公理

任何一個非空的非負整數集合都有最小元素。



##### Example

利用良序關係證明除法定理，也就是假設$a$為整數，$d$為一正整數，則存在唯一$q, r$使得$a=  dq + r$，其中$0 \le r < d$



設$S$是$a - dq$的非負整數集合，其中$q$是整數。

這個集合非空，因為$-dq$可以很大，只要$q<0$時取絕對值是很大的整數即可

根據良序關係，$S$有最小元素$r = a - dq_0$，其中$r$是非負整數，並且$r$必定小於$d$

為了證明$r$必定小於$d$，我們可以先假設$r \ge d$的情況，所以可以知道$a = dq_0 + r = dq_0 + d = d(q_0 + 1)$

所以$a - d(q_0+1) = a-dq_0-d = r-d \ge 0$，由於$r - d \ge 0$，因此不符合$r$是最小元素。

因此$r$必定小於$d$，也因此存在滿足$0 \le r < d$的整數$r$和$q$。



### 5.3 遞迴定義和結構歸納法

#### Definition - 遞迴

遞迴分成兩個步驟

1. 基礎步驟：定值$f(0)$
2. 給定一個規則，用之前的結果來計算出這個值

遞迴函數$f(n)$也可以寫成序列$a_0, a_1, a_2, ... ,a_n$，其中$f(i) = a_i$



##### Example 1

假設$f(0) = 3$，$f(n+1) = 2f(n) + 3$，找出$f(1), f(2), f(3), f(4)$



$f(1) = 2f(0) + 3 = 9$

$f(2) = 2f(1) + 3 = 21$

$f(3) = 2f(2) + 3 = 45$

$f(4) = 2f(3) + 3 = 93$



##### Example 2

寫出一個遞迴式，用來找到$f(n) = n!$



1. 定值$f(0) = 1$
2. 我們定義，$f(n+1) = (n+1) \times f(n)$



因此，$f(0) = 1$，$f(1) = (0+1)\times f(0) = 1$，$f(2) = (1+1)\times f(1) = 2$，$f(3) = (2+1)\times f(2) = 6$....



#### Introduce - 斐波納契數

斐波納契數的定義如下：$f(0) = 0$，$f(1) = 1$，則$f(n) = f(n-1) + f(n-2)$



##### Example 1

找出斐波納契數的$f(2), f(3), f(4), f(5)$

$f(2) = f(1) + f(0) = 1$

$f(3) = f(2) + f(1) = 2$

$f(4) = f(3) + f(2) = 3$

$f(5) = f(4) + f(3) = 5$



##### Example 2

證明當$n \ge 3$時，$f_n \ge \alpha^{n-2}$，其中$\alpha = \dfrac{1+\sqrt{5}}{2}$



設$P(n)$為一命題，代表$f_n \ge \alpha^{n-2}$，欲證明$n \ge 3$時$P(n)$皆為真。

基礎步驟：已知$\alpha < 2 = f_3$，則$\alpha^2 = \dfrac{(3+\sqrt{5})}{2} < 3 = f_4$

因此$P(3)$與$P(4)$都為真。

歸納步驟：假設$P(k)$為真，則$P(j)$皆為真，其中$3 \le j \le k$，$k \ge 4$。

欲證明$P(k+1)$為真，則$f_{k+1} > \alpha^{k-1}$，已知$\alpha$為$x^2-x-1=0$的解，則$\alpha^2 - \alpha - 1 = 0$。

因此$a^{k-1} = a^2 \times a^{k-3} = (a+1)a^{k-3} = a^{k-2} + a^{k-3}$

根據歸納假設，得知$f_{k-1} > a^{k-3}$，$f_k > a^{k-2}$

因此$f_{k+1} > f_k + f_{k-1} > \alpha^{k-2} + \alpha^{k-3} = \alpha^{k-1}$，得證。



#### Introduce - 拉密定理

令$a, b$為正整數，滿足$a \ge b$，則歐幾里得演算法求出$\gcd(a, b)$使用的除法將會小於等於$b$的十進位位數的$5$倍。



利用歐幾里得求出$\gcd(a, b)$時，會使用以下的等式：

$r_0 = r_1 q_1 + r_2$，$0 \le r_2 < r_1$

$r_1 = r_2 q_2 + r_3$。$0 \le r_3 < r_2$

重複多次後

$r_{n-2} = r_{n-1}q_{n-1} + r_n$，$0 \le r_n < r_{n-1}$

$r_{n-1} = r_n q_n$

我們使用了$n$次除法定理，我們可以保證商數$q_1, q_2, q_3 ... q_{n-1}$都至少為$1$。

又因為$r_{n-1} > r_n$，故我們可以保證$q_n \ge 2$。



則可以得到以下的結論

$r_n \ge 1 = f_2$

$r_{n-1} \ge 2r_n \ge 2 f_2 = f_3$

$r_{n-2} \ge r_{n-1} + r_n \ge f_3 + f_2 = f_4$

以此類推

$r_2 \ge r_3 + r_4 \ge f_{n-1} + f_{n-2} = f_n$

設$b = r_1$，得到$b = r_1 \ge r_2 + r_3 \ge f_n + f_{n-1} = f_{n+1}$



從斐波納契數Example2可以知道，當$n > 2$時，$f_{n+1} > \alpha^{n-1}$，其中$\alpha = (1+\sqrt{5})/2$，因此得出$b \ge \alpha^{n-1}$

因為$\log_{10} \alpha \approx 0.208 > 1/5$，所以可以得到$\log_{10} b > (n-1) \log_{10} \alpha > (n-1)/5$

因此，$5\times \log_{10}b > n-1$。假設$b$有$k$個10進制位數，則$b < 10^5$，也就是$\log_{10} b < k$。

得出$n-1 < 5k$，因為$k$是整數，則$n \le 5k$，得證。



因為$b$的十進位數為$\lfloor\log_{10} b\rfloor + 1$，故我們需要除小於等於$5(\log_{10}b + 1)$次才能得到結果

因為$O(5(\log_{10} b + 1)) = O(\log b)$，可知當$a > b$時，歐幾里得演算法需用$O(\log b)$次除法求出$\gcd(a, b)$的結果。



#### Introduce - 以遞迴的方式定義的集合與結構

集合的遞迴定義也有兩個部分，即基礎步驟與遞迴步驟。

在基礎步驟裡，必須指定初始的集合元素，在遞迴步驟裡必須提供已知元素形成新元素的規則。

遞迴定義也可能包含排除規則：以遞迴方式所定義的集合，除了基礎步驟所指定的元素以及應用遞迴步驟所產生的元素以外，不包含任何其他的元素。

因此除非元素從基礎步驟或者遞迴步驟中弄出來，否則他並不會出現在集合中。



##### Example 1

令$S$是正整數的子集合，遞迴定義為

基礎步驟：$3 \in S$

遞迴步驟：若$x \in S$且$y \in S$，則$x + y \in S$



根據基礎步驟，在$S$裡找到的元素是$3$，而第一次應用遞迴步驟得到$3 + 3 = 6 \in S$

第二次得$3 + 6 = 6 + 3 = 9 \in S$，$6 + 6 = 12 \in S$，以此類推。



#### Introduce - 字串

由字母集$\Sigma$所遞迴建構出的字串集$\Sigma^*$如下

1. 基礎步驟：$\lambda \in \Sigma^*$，其中$\lambda$是空字串
2. 遞迴步驟：如果$w \in \Sigma^*$而且$x \in \Sigma$，則$wx \in \Sigma^*$



##### Example

設$\Sigma = \{0, 1\}$，則字串集$\Sigma^*$有這些字串，$0, 1, 00, 01, 10, 11 ...$



#### Introduce - 字串串接

兩個字串可以透過串接運算子來做串接。

設有一字母集$\Sigma$與接下來由遞迴建構出的字串集$\Sigma^*$

則我們可以定義運算元$\cdot$如下：

1. 基礎步驟：如果$w \in \Sigma^*$，則$w \cdot \lambda = w$
2. 遞迴步驟：如果$w_1 \in \Sigma^*$、$w_2 \in \Sigma^*$且$x \in \Sigma$，則$w_1 \cdot(w_2 x) = (w_1 \cdot w_2) x$

通常來說，我們會把$w_1 \cdot w_2$寫作$w_1 w_2$

如果$w_1 = abcd, w_2 = efgh$，則串接$w_1$與$w_2$的結果$w_1 \cdot w_2 = w_1w_2 = abcdefgh$



#### Introduce - 字串長度

給定一個遞迴定義$l(w)$，代表字串$w$的長度，定義如下：

1. 基礎步驟：$l(\lambda) = 0$
2. 遞迴步驟：如果$w \in \Sigma^*$且$x \in \Sigma$，則$l(wx) = l(w) + 1$



#### Introduce - 平衡括號

給定一個遞迴定義，用來產生平衡括號集$P$

平衡括號的定義是每個左括號一定有一個對應的右括號

例如$()()()()$是合法的平衡括號，或者$(())()()$也是，但是$)()($不是

平衡括號集的定義如下：

1. 基礎步驟：$() \in P$
2. 遞迴步驟：如果$w \in P$，則$w(), (w), ()w \in P$



#### Introduce - 命題邏輯的合式公式

定義包含$T$、$F$、命題變數，以及運算符號形成的集合$\{\neg, \land, \lor, \rightarrow, \leftrightarrow\}$中的運算符號之命題邏輯的合式公式集合，來代表複合命題。

基礎步驟：$T$、$F$和$s$都是合式公式，其中$s$是命題變數

遞迴步驟：如果$E$、$F$都是合式公式，則$(\neg E)$、$(E \land F)$、$(E \lor F)$，$(E \rightarrow F)$，$(E \leftrightarrow F)$都是合式公式。

例如$((p \lor q) \rightarrow (q \land F))$是合式公式，但$pq \land$不是合式公式。



#### Introduce - 有根樹圖

有根樹圖的集合可以依照下列的步驟以遞迴的方式加以定義。

一個有根樹圖的組成包含稱為根點的特殊頂點，以及其他頂點和連接這些頂點的邊所形成的集合。

基礎步驟：單一頂點$r$是有根樹圖。

遞迴步驟：假設$T_1、T_2、...、T_n$是有根樹圖，其根點分別為$r_1、r_2、...、r_n$

則從某個不屬於有根樹圖$T_1、T_2、...、T_n$的根$r$所開始的圖，再加上每一個從$r$連到頂點$r_1、r_2、...、r_n$的邊

所得的結果仍然是有根樹圖。



#### Introduce - 二元樹

二元樹圖是一種特殊形態的有根樹圖。

在二元樹圖定義的遞迴步驟中，新的樹圖都是由兩個二元樹圖結合而成的，原先的兩個樹圖分別標示為左子樹圖與右子樹圖。



#### Introduce - 延伸二元樹圖

延伸二元樹圖的集合可以用遞迴的方式定義。

基礎步驟：單個節點是延伸二元樹

遞迴步驟：若存在兩個互斥延伸二元樹$T_1, T_2$，頂點各為$R_1, R_2$

則存在一個新的延伸二元樹$T$，頂點為$R$，連接左子樹$T_1$的頂點$R_1$與右子樹$T_2$的頂點$R_2$，且兩個延伸二元樹非空。



#### Introduce - 滿二元樹圖

滿二元樹圖的集合可依下列步驟以遞迴的方式定義。

基礎步驟：存在僅含單一頂點$r$的完全二元樹。

遞迴步驟：如果$T_1$、$T_2$是滿二元樹圖，則存在滿二元樹圖

其組成是根點$r$，再加上連接這個根點與佐子樹圖$T_1$和右子樹圖$T_2$所含每個根點的邊。



### 5.4 遞迴演算法

#### Definition - 遞迴演算法

藉由把問題簡化到更小輸入的相同問題來解決問題的演算法，稱為遞迴演算法。



##### Example

求出計算$n!$的遞迴演算法，其中$n$為非負整數。



基礎步驟：$0!=1$

遞迴步驟：如果$f(n) = n!$，則$f(n) = (n) \times f(n-1)$

因此我們可以寫成以下的遞迴程式

```c
int factorial(int n){
	if(n == 0) return 1;
	else return n * factorial(n-1);
}
```



#### Introduce - 證明遞迴演算法的正確性

數學歸納法與由其變化而得的強歸納法，皆都能用來證明遞迴演算法的正確性，即是對所有可能的輸入，都能得到想要的輸出。



##### Example

給定以下演算法，證明以下的遞迴演算法能夠正確的算出實數之冪次。

```
procedure power(a: nonzero real number, n: nonnegative integer){
	if n = 0 then return 1
	else return a * power(a, n-1);
	{output is a^n}
}
```

基礎步驟：若$n=0$，則結果為$1$，這個步驟是正確的因為對於任意的實數$a$，$a^0=1$。

歸納步驟：假設對所有的$a \neq 0$，和任意的非負整數$k$而言，$power(a, k) = a^k$，也就是說演算法執行出來的$a^k$是正確的。

現在證明$a^{k+1}$是正確的，因為$k+1$是正整數，演算法執行$power(a, k+1) = a \cdot power(a, k)$。

根據歸納甲說，$power(a, k) = a^k$，因此$power(a, k+1) = a\cdot a^k = a^{k+1}$，得證。



## 6. 計數

### 6.1 計數的基礎

#### Introduce - 乘法法則

假設一個程序可以分解成兩個連續的任務。如果完成第一個任務有$n$種方法，在完成第一個任務後，有$m$種方法完成第二個任務，則完成這整個程序共有$mn$種方法。



##### Example 1

一間只有兩位員工的新公司，租下一個有12間辦公室的房子，有幾種不同的方式能將這兩個雇員安排於不同的辦公室?



考慮第一個員工，他有12間辦公室可以選擇，則當他選擇其中一間後，第二個員工只剩下11間辦公室可以選擇。

根據乘法法則，可以知道共有132種選擇將辦公室分配給這兩位員工。



##### Example 2

長度為7的二進位字串有多少個？



考慮到每個bit的選擇不是1就是0，因此七個bit，每個bit可以選擇1或者0。

根據乘法定理，數量為$2\times2\times2\times2\times2\times2\times2=2^7=128$



#### Introduce - 加法法則

如果一種任務有兩種方式可以完成，一個方式有$n$種方法，另一個方式有$m$種方法，則完成此任務的方法有$n+m$種。



##### Example 1

假設要從數學教師或主修數學的學生中選一個人擔任校委會代表。

如果有37位數學教師與83位主修數學的學生，則有多少種不同的選擇?



我們有37種方式可以從數學教師中挑出一個擔任校委會代表，以及有83種方式可以從主修數學的學生挑出一個擔任校委會的代表。

因此共有$37+83=120$種方法。



##### Example 2

一名學生可以從三份清單中選擇一個計劃來完成任務，這三份清單分別包含23、15、19種計畫，則可以選擇的計畫有多少種？



這名學生可以從第一份清單中選擇23種可能的計畫來完成，從第二份清單中選擇15種可能的計畫來完成，以及從第三份清單選擇19種可能的計畫來完成。

因此共有23+15+19=57種計畫可以選擇。



#### Introduce - 更複雜的計數問題

有很多的複雜計數問題無法單獨用加法法則或乘法法則來解決，見以下。



##### Example 

一個註冊表單的要求是一個6到8字元構成的登入密碼。

其中密碼由大寫字母與數字所組成，且要求至少要包含一個數字，求密碼的所有組合。



考慮所有的可能，減去沒有含數字的可能，就代表至少會含一個數字。

因此，考慮所有合法密碼$P_n$的數量，其中$n$代表字串的長度。



$P_6 =  36^6 - 26^6 = 1867866560$

$P_7 = 36^7-26^7=70332353920$

$P_8 = 36^8-26^8=2612282842880$

因此所有的可能$P = P_6+P_7+P_8=2684483063360$



#### Introduce - 減法法則 (兩個集合的排容原理)

若有項任務能以兩種方式完成，分別有$n$種與$m$種方法數，則完成此項任務的所有方法數量共有$n+m$再減去兩種方法中相同的方法。



##### Example 1

以字元1開始或者以字串00結束的8位元字串有多少個?



考慮以1開始的八位元字串，共有$2^7=128$個

考慮以00結束的八位元字串，共有$2^6=64$個

考慮以1開始且以00結束的八位元字串，共有$2^5=32$個

因此所有的可能$P = 128+64-32=160$種。



#### Introduce - 除法定理

若完成某項任務的所有方式總共有$n$個步驟，而每個方式都需要$d$個步驟，則完成此任務的方法有$n/d$種方式。



##### Example

將四個人安排坐在一張圓桌，若每個人左右坐的人相同時，視為同一種方式，則一共有多少種不同的安排方式？



任意選擇圓桌的一個位置，設定這張椅子的編號為1，接下來以順時鐘連續標記座位。

將人安排在1號座位有四種方法，2號座位有三種方法，3號座位有兩種方法，4號座位有一種方法。

所以共有4!=24種方式來安排四個人入座一個圓桌。

但無論把人先安排在1號、2號、3號、4號都沒差，因此24/4=6種不同的方法。



#### Introduce - 樹狀圖

樹狀圖可以用來解決計數問題。

一棵樹包含根結點，以及分支出去的子節點，到無法分支的節點稱為葉節點。

使用樹狀圖求解時，所有的葉節點必須是獨一無二的。



##### Example

不含連續兩個1的四位元字串共有多少個?



<img src="https://i.imgur.com/qjcIDNL.png" alt="image-20210527130015016" style="zoom:67%;" />

答案是8。



### 6.2 鴿洞原理

#### Theorem - 鴿洞原理

若$k$為一正整數，如果有$k+1$個東西放進$k$個箱子內，則至少會有一個箱子包含$2$個或更多東西，



#### Corollary 1

一個函數$f$由含有$k+1$，或更多個元素的集合對應至只有$k$個元素的集合，一定不會是一對一的。



##### Proof

如果每個箱子最多都只有一個物品，則物品總數最多為$k$個，與$k+1$個物品矛盾。



##### Example 1

在367個人中，一定至少有2個人的生日是在一年的同一天，因為一年至多只有366天。



##### Example 2

在27個英文詞彙，一定至少有2個詞彙是以同一個字母開始，因為英文字母只有26個。



##### Example 3

如果考試分數是從0至100，則在班上至少需要101個人，才會存在兩個人分數相同。



##### Example 4

證明對每一個整數n，有一個n的倍數僅由0和1組成。



令$n$為一個整數，考慮1、11、111、1111、...、111...111等$n+1$個整數的序列，也就是序列最後面的元素有$n+1$個$1$

因為一個數除以$n$的餘數有$n$個可能，所以序列中有$n+1$個整數，根據鴿洞原理可以知道至少會存在兩個數字模$n$的餘數相同。

將這兩個數字相減就能得到一個可以被$n$整除的數字，而兩個都用1組出的數字相減位數只會有1或0的可能。

因此每一個整數n，必定有一個$n$的倍數僅由0和1組成。



#### Introduce - 廣義的鴿洞原理

如果$N$個物件放入$k$個箱子，則至少有一個盒子包含至少$\lceil N/k \rceil$個物件。



##### Proof

假設沒有盒子包含超過$\lceil N/k \rceil-1$個物件，則物件總數最多是

$k(\lceil N/k \rceil-1) < k((N/k+)-1) = N$

這裡與物品有$N$個東西矛盾。



##### Example 1

在100個人中，至少有$\lceil 100/12 \rceil = 9$人在同一個月份裡出生。



##### Example 2

如果成績分為A、B、C、D、F五種標準，在一個離散數學班裡，最少要多少位學生才能保證至少有6位學生得到相同的分數？



已知$\lceil N/5 \rceil = 6$，能找到符合最小的整數$N = 26$，因此需要$26$個學生才能保證至少有6位學生得到相同的分數。



#### Introduce - 蘭姆西數字

假設一個團體有6個人，其中任意2個人不是敵人就是朋友。

證明這6個人中要不存在3人彼此都是朋友的小團體，要不存在一個3人都是敵人的小團體。



##### Example 1

令A是六個人中的其中一人，則其他五人中至少三人是A的朋友，或至少三人是A的敵人。

因為當五個物件被分成兩個集合時，根據廣義鴿洞原理，其中一個集合至少有$\lceil 5/2 \rceil = 3$個元素

在第一種情況中，假設B、C、D是A的朋友，若B、C、D有兩個人也是朋友，則這兩個人和A構成彼此是朋友的三人組。

在第二種情況中，假設B、C、D是A的敵人，若B、C、D有兩個人也是敵人，則這兩個人和A構成彼此是敵人的三人組。



### 6.3 排列與組合

#### Theorem - 排列

若$n$與$r$為正整數，則從含有$n$個元素的集合中選取$r$個元素來做排列的方法數有

$P(n, r) = n(n-1)(n-2)...(n-r+1) = \dfrac{n!}{(n-r)!}$

##### Proof

利用乘法定理來進行證明，在排列的第一位有$n$個選擇，第二位有$n-1$個選擇，第三位有$n-2$個選擇...

直至選取第$r$位時，集合中只剩下$n-r+1$個選擇。

完全不取物件出來的排列方式只有一種，所以$P(n, 0) = 1$



##### Example 1

從五個學生中，選出三人排出一列來拍照有幾種方法？將這五個學生排成一列來拍照有多少種方法？



$P(5, 3) = \dfrac{5!}{3!} = 4\times 5 = 20$

$P(5, 5) = \dfrac{5!}{0!} = 5! = 120$



##### Example 2

在字母ABCDEFGH的排列中，包含字母ABC的排列有幾種？



因為ABC必須排在一起，所以其實這題只有六個物件(ABC)、D、E、F、G、H

將這6個物品做排列，也就是$P(6,6) = 6! = 720$



#### Introduce - r-排列

自一個集合中取出$r$個元素來排列稱做$r-$排列。



##### Example

令$S = \{a, b, c\}$，則所有$S$的$2-$排列有：$\{a, b\}, \{a, c\}, \{b, a\}, \{b, c\}, \{c, a\}, \{c, b\}$，共有有$P(3, 2) = 6$種可能



#### Theorem - 組合

當$n$為非負整數，$r$為整數，其中$0 \le r \le n$，則一個包含$n$個相異元素的集合

其組合的個數為$C(n, r) = \dfrac{n!}{r!(n-r)!} = \dfrac{(n)(n-1)...(n-r+1)}{r!}$

且$C(n, r) = C(n, n-r)$



##### Proof

由於組合無論順序，先找到其排列，除以$r$個元素所有可能的排列的總數即為組合數量（除法定理）。

也就是$P(n, r) / P(r, r) = C(n, r)$



已知$C(n, r) = \dfrac{n!}{r!(n-r)!}$，$C(n, n-r) = \dfrac{n!}{(n-r)!(n-(n-r))!} = \dfrac{n!}{r!(n-r)!}$

因此$C(n, r) = C(n, n-r)$



##### Example 1

從一副52張的撲克牌中取出五張牌有幾種可能的組合？若選取47張牌有幾種方法？



取出五張牌不需要排列，因此使用組合$C(52, 5) = \dfrac{52!}{47!5!} = \dfrac{52\times51\times50\times49\times48}{5!} = 2598960$

選取47張牌，可以知道$C(52,47) = \dfrac{52!}{47!5!} = \dfrac{52\times51\times50\times49\times48}{5!} = 2598960$



##### Example 2

一個有10個隊員的網球隊，要挑出五個球員來參加比賽，可以有幾種不同的方式？



轉換問題成在10個元素的集合中，所有挑出五個元素的子集合個數，也就是$C^{10}_5 = 252$



#### Definition - 組合證明

一個等式的組合證明是一種利用計數論證的證明方式。

證明等式兩端都是在計算某種物件的數量，只是使用方法不同，或者說明有一種雙射的對應關係存在於等式兩端的物件。

這兩種證明的形態分別稱作二重計數證明或是雙射證明。



##### Proof

首先使用雙射證明法求證對所有整數$n$與$r$，當$0 \le r \le n$，$C(n, r) = C(n, n-r)$。

假設$S$為包含$n$個元素的集合，每個由包含$r$個元素之$S$子集合$A$對應到包含$n-r$個元素的集合$\overline{A}$的函數都是雙射函數。

這樣一來，我們便證得$C(n, r) = C(n, n-r)$，因為有雙射關係的兩集合之元素個數相同。



使用二重計數證明求證對於所有整數$n$與$r$，當$0 \le r \le n$，$C(n,r) = C(n, n-r)$。

根據定義，包含$r$個元素的子集合$A$有$C(n, r)$個。每個這樣的子集合$A$都決定出哪些元素不在$A$中，也就是在$\overline{A}$中。

因為$S$中包含$r$個元素之子集合補集有$n-r$個元素，所以應該有$C(n, n-r)$個包含$r$個元素之子集合，所以$C(n, r) = C(n, n-r)$



### 6.4 二項式係數及其等式

#### Introduce - 二項式係數

在$n$個元素中選出$r-$組合的方法數為$\displaystyle \binom{n}{r}$，這個數也稱作二項式係數。

因為這些數將出現在二項展開式的係數中，例如$(a+b)^n$。



#### Theorem - 二項式定理

令$x$與$y$為變數，而$n$為非負整數，則

$(x+y)^n = \displaystyle \sum^n_{j=0} \binom{n}{j} x^{n-j}y^j = \binom{n}{0}x^n+\binom{n}{1}x^{n-1}y+...+\binom{n}{n-1}xy^{n-1}+\binom{n}{n}y^n$



##### Example 1

求出$(x+y)^4$的展開式。



$(x+y)^4 = \displaystyle \sum^4_{j=0} \binom{4}{j} x^{4-j}y^j = \binom{4}{0}x^4 + \binom{4}{1}x^3y + \binom{4}{2}x^2y^2 + \binom{4}{3}xy^3 + \binom{4}{4}y^4$

$= x^4+4x^3y+6x^2y^2+4xy^3+y^4$



##### Example 2

求出$(x+y)^{25}$展開式中$x^{12}y^{13}$的參數。



$\displaystyle \binom{25}{13} = \dfrac{25!}{12!13!} = 5200300$



##### Example 2

求出$(2x-3y)^{25}$展開式中$x^{12}y^{13}$的係數。



將式子轉化成$(2x+(-3y))^{25}$

因此在$x^{12}y^{13}$的係數為$\displaystyle \binom{25}{12}\times 2^{12} + (-3)^{13} = -\dfrac{25!}{12!13!}\times 2^{12}\times 3^{13}$



#### Corollary 1

令$n$為非負整數，則$\displaystyle \sum^{n}_{k=0} \binom{n}{k} = 2^n$



##### Proof

利用二項式定理，令$x = 1, y = 1$

則$\displaystyle 2^n = (1+1)^n = \sum^n_{k=0}\binom{n}{k}1^{k}1^{n-k} = \sum^n_{k=0}\binom{n}{k}$



#### Corollary 2

令$n$為正整數，則$\displaystyle \sum^{n}_{k=0} (-1)^k \binom{n}{k} = 0$



##### Proof

利用二項式定理，令$x=1, y = -1$

則$\displaystyle 0^n = (1+(-1))^n = \sum^{n}_{k=0} \binom{n}{k} (-1)^k 1^{n-k} = \sum^n_{k=0} \binom{n}{k}(-1)^k$



#### Corollary 3

令$n$為非負整數，則$\displaystyle \sum^n_{k=0} 2^k \binom{n}{k} = 3^n$



##### Proof

利用二項式定理，令$x= 1, y = 2$

則$\displaystyle 3^n = (1+2)^n = \sum^n_{k=0}\binom{n}{k}1^{n-k}2^k  =\sum^n_{k=0}\binom{n}{k} 2^k$



#### Theorem - 帕斯卡等式

令$n$與$k$為正整數，其中$n \ge k$，則$\displaystyle \binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$



##### Proof

假設$T$為包含$n+1$個元素的集合，且$a \in T$，$S = T - \{a\}$

其中$T$有$\displaystyle \binom{n+1}{k}$個包含$k$個元素的不同子集合。

將這些子集合分成兩類

其中一個為包含$a$與$k-1$個$S$中的元素，數量為$\displaystyle \binom{n}{k-1}$

另一個為不包含$a$，包含$k$個$S$中的元素，數量為$\displaystyle \binom{n}{k}$

因此得到$\displaystyle \binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}$



#### Introduce - 帕斯卡三角形

上面的等式可以寫成一個三角形，如下。

![image-20210601150415074](https://i.imgur.com/x7NpGxo.png)



#### Theorem - 凡德蒙德等式

令$m$、$n$、$r$為非負整數，而且$r$不能大於$m$與$n$，則$\displaystyle \binom{m+n}{r} = \sum^r_{k=0} \binom{m}{r-k} \binom{n}{k}$



##### Proof

假設在一個集合有$m$個元素，第二個集合有$n$個元素，則在這兩個元素取$r$個元素的方法有$\displaystyle \binom{n+m}{r}$個。

另外一種方法，若在第一個集合取出$k$個元素，第二個集合取出$r-k$個元素，其中$0 \le k \le r$

則在第一個集合取出$k$個元素有$\displaystyle \binom{n}{k}$個方法，在第二個集合取出$r-k$個元素有$\displaystyle \binom{m}{r-k}$個方法。

利用乘法法則，則上面的選取方法有$\displaystyle \binom{n}{k} \binom{m}{r-k}$種方法。

窮舉所有的$k$利用加法定理加起來，即為$\displaystyle \binom{n+m}{r}$的方法數，因此$\displaystyle \binom{n+m}{r} = \sum^r_{k=0} \binom{n}{k} \binom{m}{r-k}$



#### Corollary 4

若$n$為非負整數，則$\displaystyle \binom{2n}{n} = \sum^n_{k=0} \binom{n}{k}^2$



##### Proof

令$n = r = m$，套入凡德蒙德等式，得$\displaystyle \binom{n+n}{n}= \sum^n_{k=0} \binom{n}{n-k} \binom{n}{k}$

因為$\displaystyle \binom{n}{n-k} = \binom{n}{k}$，則$\displaystyle \binom{2n}{n}= \sum^n_{k=0} \binom{n}{k}^2$



#### Theorem - 朱世傑恆等式

令$n$和$r$為非負整數，且$r \le n$，則$\displaystyle \binom{n+1}{r+1} = \sum^n_{j=r} \binom{j}{r}$

##### Proof

利用數學歸納法來證明。

基礎步驟：令$n = r$，則有$\displaystyle \sum^r_{j=r} \binom{j}{r} = \binom{r}{r} = 1 = \binom{r+1}{r+1}$

歸納步驟：假設$P(k)$代表$\displaystyle \binom{k+1}{r+1} = \sum^{k}_{j=r} \binom{j}{r}$為真，其中$k \ge r$

則證明若$n=k+1$，$\displaystyle \binom{k+2}{r+1} = \binom{k+1}{r} + \binom{k+1}{r+1} = \binom{k+1}{r} + (\sum^{k}_{j=r} \binom{j}{r}) = \sum^{k+1}_{j=r} \binom{j}{r}$

根據歸納步驟，得到$\displaystyle \binom{k+2}{r+1} = \sum^{k+1}_{j=r}$，因此$P(k) \rightarrow P(k+1)$為真，證畢。



### 6.5 一般化的排列與組合

#### Theorem - 重複排列

有$n$個元素的集合中，允許重複的$r-$排列共有$n^r$種



##### Proof

在$r-$排列中，每個位置有$n$個選擇，根據乘法法則，可以得到所有方法數為$n^r$。





##### Example

利用大寫英文字母能形成多少個長度為$r$的字串



根據乘法法則，大寫字母有26個，每個位置可以放的字母有26個可能，因此方法數總共有$26^r$個



#### Theorem - 重複組合

在包含$n$個元素的集合中，允許重複之$r-$的組合的個數為$C(n+r-1, r) = C(n+r-1, n-1)$



##### Proof

以元素的數量來考慮組合的數量。

我們先假設從四個元素中挑選總共六個數量的方法數，可以知道

這樣是一種選取方式：第一個元素中挑選2個，第二個元素中挑選1個，第三個元素中挑選1個，第四個元素中挑選2個

因此可以把問題規約成星號與直線做排列。

以上面的例子來做範例，我們可以考慮成這樣的形式：`**|*|*|**`

無論怎麼排列，都會有$n-1$個隔板，以及$r$個星星

我們可以把問題規約成在$n-1+r$個位置中，選取$n-1$個位置來擺放隔板，或者選取$r$個位置來擺放星星。

因此方法數即為$C(n-1+r, r) = C(n-1+r, n-1)$



##### Example 1

假設某餅乾店中有4種不同口味的餅乾。若不計挑選時的順序，選取6塊餅乾有幾種方法？



問題可以規約成在4個元素中，重複選出6個元素的方法有幾個。

因此我們可以利用重複組合，得到$C(6+4-1, 6) = C(9, 6) = 84$



##### Example 2

下面方程組有幾種解？

$x_1 + x_2 + x_3 = 11$



考慮到很多個1，總共需要11個，把這些1分成三堆來做組合。

因此問題變成了，有11個1與2個隔板，可以選擇放隔板或者放1來算出方法數

也就是$C(11+3-1, 2) = c(11+3-1, 11) = C(13, 2) = 78$



#### Theorem - 不可區分物件的排列

若$n$個物件中，第一種相同的物件有$n_1$個，第二種相同的物件有$n_2$個，....，第$k$種相同的物件有$n_k$個

則此$n$個物件的排列方法數有$\dfrac{n!}{n_1!n_2!n_3!...n_k!}$



##### Proof

將此$n$個物件排成一列。

首先挑選出$n_1$個位置來放第一種物件，方法數為$C(n, n_1)$，此時剩下$n-n_1$個位置可以放置新的物件。

接下來選出$n_2$個位置來放第二種物件，方法數為$C(n-n_1, n_2)$，此時剩下$n-n_1-n_2$個位置可以放置新的物件。

以此類推後可以利用乘法法則，得到總方法數為



$C(n, n_1)C(n-n_1, n_2)...C(n-n_1-n_2-...-n_{k-1}, n_k)$

$= \dfrac{n!}{n_1!(n-n_1)!} \dfrac{(n-n_1)!}{n_2!(n-n_1-n_2)!} ... \dfrac{n-n_1-...-n_{k-1}}{n_k!0!}$

$= \dfrac{n!}{n_1!n_2!n_3!...n_k!}$



##### Example 

將單字SUCCESS的字母重新排列，將形成多少不同的字串？



$\dfrac{7!}{3!2!1!1!} = 420$



#### Theorem - 將不同物件分配至不同箱子中

將$n$個物件分配到$k$個不同的箱子，使得第$i$個箱子中有$n_i$個物件的方法數為$\dfrac{n!}{n_1!n_2!...n_k!}$，其中$i = 1, 2, ..., k$



##### Proof

考慮到第一個箱子有$n_1$個物件，分配方法數量是$C(n, n_1) = \dfrac{n!}{(n-n_1)!n_1!}$

考慮到第二個箱子有$n_2$個物件，分配方法數量是$C(n-n_1, n_2) = \dfrac{(n-n_1)!}{(n-n_1-n_2)!n_2!}$

利用乘法定理，可以得到

$C(n, n_1) \times C(n - n_1, n_2) \times ... \times C(n_k, n_k) = \dfrac{n!}{(n-n_1)!n_1!}\times \dfrac{(n-n_1)!}{(n-n_1-n_2)!n_2!} ... \dfrac{n_k!}{n_k! 0!} = \dfrac{n!}{n_1!n_2!...n_k!}$



##### Example

將一副標準的52張撲克牌分給四個人，一人五張，會有多少種不同的情形？



將問題轉化成，共有四個人，一人五張，剩下的丟回牌組(32張)。

因此所有方法為：$\dfrac{52!}{5!5!5!5!32!} = 1478262843475644110602240$



#### Introduce - 將相同物件分配至不同箱子中

將$n$個相同物件分配至$k$個不同的箱子的方法數為$C(n+k-1, n)$。



##### Example

將10個相同的球放進8個不同的箱子中，共有幾種方法？



問題等於8個元素的集合中找出$10-$組合的方式，所以可能的情況為$C(8+10-1, 10) = C(17, 10) = 19448$



#### Introduce - 不同物件與相同箱子

令$S(n, j)$表示將$n$個不同的物件分配至$k$個相同的箱子中，且沒有箱子是空的，其中$S(n, j)$稱為第二類斯特林數，其定義如下。

$\displaystyle S(n, j) = \dfrac{1}{j!} \sum^{j-1}_{i=0} (-1)^i \binom{j}{i} (j-i)^n$

將$n$個物件放至$k$個相同的箱子的方法數為$S(n, 1)+S(n, 2)+...+S(n, k)$，也就是

$\displaystyle \sum^k_{i=1} S(n, j) = \sum^k_{i=1} \dfrac{1}{j!} \sum^{j-1}_{i=0} (-1)^i \binom{j}{i} (j-i)^n$



##### Proof

待補。



#### Introduce - 相同物件與相同箱子

將$n$個相同的物件分配至$k$個相同的箱子中，就是將$n$個分成$j$個小於$k$的正整數$a_1, a_2, a_3 ... a_j$

其中$a_1 \ge a_2 \ge a_3 ... \ge a_j$使得$a_1 + a_2 + ... + a_j = n$。



### 6.6 產生組合與排列

#### Introduce - 產生排列

任何一個包含$n$個元素的集合都能與集合$\{1, 2, 3, ..., n\}$做個一對一個對應關係。

任何一種$n$個元素的排列方式，都能對應於一個由整數$1$到$n$的排列，且能產生此集合的$n!$種排列。



#### Introduce - 字典順序

若有兩排列$a, b$長度皆為$n$。

對某個$k$，$1 \le k \le n$，$a_1 = b_1, a_2 = b_2 ... a_{k-1} = b_{k-1}$，但$a_k < b_k$，則稱排列$a_1 a_2 ... a_n$大於排列$b_1 b_2 ... b_n$。

也就是在兩種排列中，在第一次出現不同數字的位置上，數字較大的排列小於數字較小的排列。



##### Example

在集合$\{1, 2, 3, 4, 5\}$的排列中，23415排在23514前面，因為第一次出現不相同數字的第三個位置4小於5

同理，41532排在52143之前。



#### Introduce - 利用字典順序產生下一個較大排列

若有一排列$a_1a_2a_3...a_n$

假設$a_{n-1} < a_n$，則我們只需要調換這兩個整數，就可以找到下一個較大的排列。

舉個例子，231456，可知5<6，因此調換這兩個數字得到231465，就是下一個較大的排列。

假設$a_{n-1} > a_n$，那就考慮倒數第三個數字，若$a_{n-2} < a_{n-1}$，就重新安排最後三個數字來得到下一個較大的排列。

將$a_{n-1}$與$a_n$中較小的數字安排於第$n-2$個位置，剩下兩個數字依照遞增的方式排列，例如234165下一個排列即為231516。



##### Example 1

依字典順序方式362541的下一個較大排列是什麼？



可以知道，我們必須得要考慮第3個數字。

在5、4、1中選一個大於2的最小整數，也就是4，安排在第3個位置。

因此得到$364125$為下一個較大排列。



##### Example 2

求出所有由1, 2, 3依據字典順序所得的排列。



首先拿到123。

因為$2 < 3$，因此我們可以調換這兩個數字，得到132為次大排列。

接著因為$3 > 2$

因此我們必須要考慮第一個數字，從2、3找到一個大於1的最小整數與其交換後將後兩個位置遞增排序，得到213為次大排列。

因為$1 < 3$，因此我們可以調換這兩個數字，得到231為次大排列。

接著因為$3 > 1$

因此我們必須要考慮第一個數字，從1、3找到一個大於1的最小整數與其交換後將後兩個位置遞增排序，得到312為次大排序。

因為$1 < 2$，因此我們可以調換這兩個數字，得到321為次大排序。



#### Introduce - 產生組合

組合不過只是一個子集合，因此我們可以用$\{a_1, a_2, ... a_n\}$之子集合與長度為$n$的位元字串的對應關係來產生組合。

假設有一個字元字串為$s=s_1s_2s_3...s_n$，若$s_i = 0$，則$a_i$不在此子集合內，反之則$a_i$在此集合內。

產生所有組合的方式可以產生一組字元字串，從$s$皆為0慢慢累加1至$s$皆為1，共有$2^n$種。



##### Example

求出1000100111的下一個位元字串。



$1000100111 + 1 = 1000101000$



#### Introduce - 產生r-組合

每一個$r-$組合都能用一個序列來表現，此序列包含依遞增方式排列的子集合，也就是此$r-$組合能夠用這個序列的字典順序排列出來。

在字典順序中，最前面的r-組合是$\{1, 2, ..., r-1\}$，最後面的組合為$\{n+r-1, n+r-2, ..., n-1, n\}$

產生$a_1a_2...a_r$的下一個$r-$組合，首先得要找到最後一個$a_i$的位置，其中$a_i \neq n-r+i$

然後以$a_{i+1}$替換$a_i$，當$j=i+1, i+2, ..., r$時，以$a_i+j-i+1$來替換$a_j$。



##### Example 

在集合$\{1, 2, 3, 4, 5,6\}$中，找出$\{1, 2, 5, 6\}$的下一個$4-$組合。



已知最後一個出現$a_i$的地方為$i=2$。

因此，我們令$a_2 = a_2+1 = 3$，接著$a_3 = 2 + 3 - 2 + 1 = 4$，$a_4 = 2+4-2+1=5$

得到下一個較大的$4-$組合為$\{1, 3, 4, 5\}$



## 9. 關係

### 9.1 關係與其性質

#### Definition - 二元關係

令$A$與$B$為集合，一個由$A$到$B$的二元關係是$A \times B$的子集合。



由$A$到$B$的二元關係是個有序對集合$R$，每個有序對的第一個分量來自$A$，第二個分量來自集合$B$。

我們使用符號$a\ \text{R}\ b$來表示$(a, b) \in R$，而$a \not{\text{R}}\  b$表示$(a, b) \not \in R$

當我們說$(a, b)$屬於$R$時，則我們說$a$與$b$有關係。





##### Example 1

令$A$為學校中的學生集合，$B$為開授課程所形成的集合。

令關係$R$包含$(a, b)$，表示學生$a$選修課程$b$。

例如，若Xuan與Uriah都選修了計算機程式設計，則有序對 (Xuan, 計算機程式設計) 和 (Uriah, 計算機程式設計) 都屬於關係R。

若Xuan還選修了離散數學，則 (Xuan, 離散數學) 也在關係R中。

若Uriah沒有選修離散數學，則 (Uriah, 離散數學) 不在關係R中。



##### Example 2

若A為臺灣所有區所形成的集合，而B為臺灣所有縣市的集合。

若區A位於縣市B中，則定義元素$(a, b)$在關係$R$中。

例如：(新化區, 台南市)，(烏日區, 台中市)，(大安區, 台北市)，(新莊區, 新北市) 和 (左營區, 高雄市) 都在關係 $R$ 中

但 (板橋區, 台北市)，(新市區, 高雄市) 就不在關係 $R$ 中，因為板橋區在新北市，新市區在台南市。



#### Introduce - 將函數視為一種關係

由集合$A$到集合$B$的函數$f$，指派唯一一個$B$中的元素給每一個$A$中的元素，則$f$的元素即為有序對$(a, b)$，其中$b = f(a)$。

因為$f$之圖形為$A \times B$的子集合，所以是一個由$A$到$B$的關係。



反之，若$R$為$A$到$B$的關係，使得每個$A$中的元素指出現在有序對的第一個分量中一次，則可定義出一個函數，使得$R$為其圖形。

由指派唯一一個$B$中的元素$b$給每一個$A$中的元素$a$，使得$(a, b) \in R$，便能觀察出此性質。



關係能用來呈現集合$A$和$B$元素間一對多的關聯性。

其中某個$A$的元素對應到多個$B$的元素，而函數表現的是每個$A$的元素只與一個$B$有關係。



#### Definition - 集合上的關係

一個在集合$A$上的關係，是指由$A$到$A$的關係，也就是$A \times A$的子集合。



##### Example 1

令$A$為集合$\{1, 2, 3, 4\}$，哪些序對屬於關係$R = \{(a, b) | b\ \text{mod}\ a = 0\}$?



稍微列舉一下，可知$R = \text{{(1, 1), (1, 2), (1, 3), (1, 4), (2, 2), (2, 4), (3, 3), (4, 4)}}$



##### Example 2

考慮下面整數集合上的關係：

$R_1 = \{(a, b) | a \le b\}$

$R_2 = \{(a, b)|a > b\}$

$R_3 = \{(a, b) | a = b \lor a = -b\}$

$R_4 = \{(a, b) | a = b\}$

$R_5 = \{(a, b) | a = b + 1\}$

$R_6 = \{(a, b) | a + b \le 3\}$

哪一個關係包含下列每一個有序對(1, 1), (1, 2), (2, 1), (1, -1)和(2, 2)?



考慮(1, 1)，可以知道(1, 1)在關係$R_1, R_3, R_4, R_6$中

考慮(1, 2)，可以知道(1, 2)在關係$R_1, R_6$中

考慮(2 ,1)，可以知道(2, 1)在關係$R_2, R_5, R_6$中

考慮(1, -1)，可以知道(1, -1)在關係$R_2, R_3, R_6$中

考慮(2, 2)，可以知道(2, 2)在關係$R_1, R_3, R_4$中

因此沒有一個關係包含上述所有有序對。



##### Example 3

在包含$n$個集合的關係上，共有多少個不同的關係？



在集合$A$上的關係是$A\times A$的子集合，也就是當$A$有$n$個元素時，$A\times A$有$n^2$個元素。

一個包含$m$個元素的集合共有$2^m$個子集合，所以$A\times A$有$2^{n^2}$個子集合。



#### Definition - 反身性

對於所有的$a \in A$，若$(a, a) \in R$，則稱集合$A$上的關係$R$為反身性的 (reflexive)，



##### Example 1

考慮下面集合$\{1, 2, 3, 4\}$上的關係：

$R_1 = \{(1, 1), (1, 2), (2, 1), (2, 2), (3, 4), (4, 1), (4, 4)\}$

$R_2 = \{(1, 1), (1, 2), (2, 1)\}$

$R_3 = \{(1, 1), (1, 2), (1, 4), (2, 1), (2, 2), (3, 3), (4, 1), (4, 4)\}$

$R_4 = \{(2, 1), (3, 1), (3, 2), (4, 1), (4, 2), (4, 3)\}$

$R_5 = \{(1, 1), (1, 2), (1, 3), (1, 4), (2, 2), (2, 3), (2, 4), (3, 3), (3, 4), (4,4)\}$

$R_7 = \{(3, 4)\}$

哪一個關係是反身性的?



可以觀察到，$R_3, R_5$是有反身性的，因為他們包含所有$(a, a)$的有序對。

##### 

##### Example 2

正整數上的「整除」關係是否為反身性的？



因為對所有正整數$a$而言，$a|a$，所以「整除」關係是反身性的。



##### Example 3

在含有$n$個元素之集合上的關係中，有多少具不同的反身性？



在集合$A$上的關係是一個$A \times A$的子集合，因此$R$中的元素由$A \times A$個$n^2$元素中取出。

若$R$是反身性的，則$n$個$(a, a)$的有序對一定得包含在$R$中，其中$a \in A$。

剩下的$n(n-1)$個$(a, b)$，其中$a, b\in R, a \neq b$的元素不一定要在$R$中。

根據乘法定理，共有$2^{n(n-1)}$個不同的反身性關係。



#### Definition - 對稱性與非對稱性

設有一集合$A$與一關係$R$，若對所有的$a, b \in A$，當$(a, b) \in R$時，$(b, a) \in R$，則集合$A$上的關係$R$有對稱性。

若對所有的$a, b \in A$，當$(a, b) \in R$與$(b, a) \in R$時$a=b$，則集合$A$上的關係$R$有反對稱性。

對稱性可以寫成$\forall a\forall b((a, b) \in R \rightarrow (b, a) \in R)$，而反對稱性可以寫成$\forall a \forall b ((a, b) \in R \land (b, a) \in R \rightarrow (a = b))$



##### Example 1

參考以下的關係，找出對稱性與反對稱性。

$R_1 = \{(a, b) | a \le b\}$

$R_2 = \{(a, b)|a > b\}$

$R_3 = \{(a, b) | a = b \lor a = -b\}$

$R_4 = \{(a, b) | a = b\}$

$R_5 = \{(a, b) | a = b + 1\}$

$R_6 = \{(a, b) | a + b \le 3\}$



$R_3 ,R_4, R_6$會是對稱性。

$R_3$是對稱性的，因為當$a = b$時$b = a$，或者當$a = -b$時，$b = -a$。

$R_4$是對稱性的，因為當$a = b$時$b = a$

$R_6$是對稱性的，因為當$a+b \le 3$時$b + a \le 3$。



$R_1, R_2, R_4, R_5$會是反對稱性的。

$R_1$是反對稱性的，因為當$a \le b$時，若$b \le a$，則$a = b$。

$R_2$是反對稱性的，因為不可能出現$a > b$且$b > a$。

$R_4$是反對稱性的，因為若出現$a= b$且$b = a$時，$a = b$。

$R_5$是反對稱性的，因為若出現$a=b+1$且$b=a+1$，則$a-b = b-a = 1$，由於不存在$(a, b)$來滿足等式，故$R_5$是反對稱性的。



##### Example 2

正整數集合上的「整除」關係是否為對稱性的？是否為反對稱性的？



可以知道，若$a \text{ mod }b = 0$，則$a \ge b$，正整數上的整除不符合對稱性。

但若$a \text{ mod } b = 0$且$b \text{ mod } a = 0$，則$a \ge b$且$b \ge a$，因此$a = b$，故正整數上的整除符合反對稱性。



#### Definition - 遞移性

設有一集合$A$與一關係$R$，對所有的$a, b, c \in R$，且$(a, b) \in R \land (b, c) \in R$時$(a, c) \in R$，則稱集合$A$上的關係$R$稱為遞移性的。

可以寫成$\forall a \forall b \forall c (((a, b) \in R \land (b, c) \in R) \rightarrow (a, c) \in R)$



##### Example 1

參考以下的關係，找出遞移性的關係。

$R_1 = \{(a, b) | a \le b\}$

$R_2 = \{(a, b)|a > b\}$

$R_3 = \{(a, b) | a = b \lor a = -b\}$

$R_4 = \{(a, b) | a = b\}$

$R_5 = \{(a, b) | a = b + 1\}$

$R_6 = \{(a, b) | a + b \le 3\}$



$R_1, R_2, R_3, R_4$是遞移性的。

$R_1$是遞移性的，因為當$a \le b$且$b \le c$時符合$a \le c$。

$R_2$是遞移性的，因為當$a > b$，$b > c$時符合$a > c$

$R_3$是遞移性的，因為當$a = \pm b$且$b = \pm c$時符合$a = c$。

$R_4$是遞移性的，因為當$a = b$且$b = c$時符合$a = c$。

其餘都不是遞移性的。

$R_5$不是遞移性的，因為當$a = b + 1$且$b = c + 1$時，則$a = c + 1$可能不成立，例如$(a, b) = (4, 3)$且$(b, c) = (3, 1)$。

$R_6$不是遞移性的，因為當$a + b \le 3$且$b + c \le 3$時，$a+c\le3$可能不成立，例如$(a, b) = (4, -5)$且$(b, c) = (-5, 6)$



##### Example 2

正整數集合上的「整除」關係是否為遞移性的？



若$(a, b) \in R$，也就是$a$能整除$b$，則$b \text{ mod } a = 0$，則我們可以說$b = ad$

若$(b, c) \in R$，也就是$b$能整除$c$，則$c \text{ mod } b = 0$，，則我們可以說$c = bk$

因此$c = bk = (ad)k$，利用定義知道$a$能整除$c$，可以知道正整數集合上的「整除」關係為遞移性的。



#### Introduce - 關係的組合

由$A$到$B$的關係是$A \times B$的子集合，因此兩個關係的組合可以使用所有集合間的組合來表示。



##### Example 

令$A = \{1, 2, 3\}$且$B = \text{{1, 2, 3, 4}}$。

關係$R_1 = \text{{(1, 1), (2, 2), (3, 3)}}$，$R_2 = \text{{(1, 1), (1, 2), (1, 3), (1, 4)}}$，能用以下組合。



$R_1 \cup R_2 = \text{{(1, 1), (1, 2), (1, 3), (1, 4), (2, 2), (3, 3)}}$

$R_1 \cap R_2 = \text{{(1, 1)}}$

$R_1 - R_2 = \text{{(2, 2), (3, 3)}}$

$R_2 - R_1 = \text{{(1, 2), (1, 3), (1, 4)}}$



#### Definition - 合成關係

令$R$為由集合$A$到集合$B$的關係，而$S$為由集合$B$到集合$C$的關係。

$R$與$S$的合成也是個關係，包含有序對$(a, c)$，其中$a \in A, c \in C$，而且存在一個$b \in B$，使得$(a, b) \in R$和$(b, c) \in S$。

我們將$R$和$S$的合成記為$S \circ R$。



##### Example 

令$R$為由$\{1, 2, 3\}$到$\{1, 2, 3, 4\}$的關係，$R=\text{{(1, 1), (1, 4), (2, 3), (3, 1), (3, 4)}}$。

而$S$為由$\text{{1, 2, 3, 4}}$到$\text{{0, 1, 2}}$的關係，$S = \text{{(1, 0), (2, 0), (3, 1), (3, 2), (4, 1)}}$。

$R$與$S$的合成為何？



檢驗所有的有序對，得到$S \circ R = \text{{(1, 0), (2, 1), (2, 2), (3, 0), (3, 1)}}$



#### Definition - R的冪次定義

令$R$為集合$A$上的關係。

當$n = 1, 2, 3, ...$，冪次$R^n$的遞迴定義如下：$R^1=R$且$R^{n+1} = R^n \circ R$

因此$R^2 = R \circ R$，$R^3 = R^2 \circ R = (R \circ R) \circ R$



##### Example 

令$R = \text{{(1, 1), (2, 1), (3, 2), (4, 3)}}$。求出冪次$R^n$，其中$n=1, 2, 3,...$。



因為$R^2 = R \circ R$，我們得到$R^2 = \text{{(1, 1), (2, 1), (3, 1), (4, 2)}}$。

接下來，因為$R^3 = R^2 \circ R$，$R^3= \text{{(1, 1), (2, 1), (3, 1), (4, 1)}}$

繼續計算可以發現$R^4 = R^3$，$R^5 = R^3...$，可以得到$R^n = R^3, n=4, 5, 6, 7...$



#### Theorem 1

集合$A$上的關係$R$是遞移性的，若且唯若$R^n \subseteq R$，$n = 1, 2, 3, ...$



##### Proof

假設$R^n \subseteq R$，$n = 1, 2, 3, ...$，因此$R^2 \subseteq R$。

我們能由此證明$R$是遞移性的，若$(a, b) \in R$ 和 $(b, c) \in R$，根據合成的定義，$(a, c) \in R^2$。

由於$R^2 \subseteq R$，得到$(a, c) \in R$，因此$R$是遞移性的。



利用數學歸納法來證明，可以知道$n=1$是明顯會成立的。

因此我們假設$R^n \subseteq R$，其中$n$為正整數，往證$R^{n+1}$亦為$R$的子集合。

首先假設$(a, b) \in R^{n+1} = R^n \circ R$，因而存在$x \in A$使得$(a, x) \in R$且$(x, b) \in R^n$。

根據歸納假說，$R^n \subseteq R$，我們有$(x, b) \in R$。

由於$R$是遞移性的，$(a, x) \in R$ 且 $(x, b) \in R$，可推導出$(a, b) \in R$。

因而$R^{n+1} \subseteq R$，得證。



### 9.2 n元關係及其應用

#### Definition - n元關係

令$A_1, A_2, ..., A_n$為集合，一個在這些集合上的$n$元關係是$A_1 \times A_2 \times ... \times A_n$的子集合。

集合$A_1, A_2, ..., A_n$稱為這個關係的域(domain)，而$n$稱為這個關係的階(degree)



##### Example 1

令$R$為$N \times N \times N$的關係，由有序三項$(a, b, c)$組成，其中$a, b, c$為整數，且$a < b < c$。

$(1, 2, 3) \in R$但$(2, 4, 3) \not \in R$，此關係的階數為$3$，而其域皆為自然數集合。 



##### Example 2

令$R$為$\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}$的關係，由有序三項$(a, b, c)$組成，其中$a,b,c$形成一個算術數列。

$(a, b, c) \in R$，若且唯若存在整數$k$，使得$b=a+k$且$c=a+2k$，或是$b-a=k$且$c-b=k$。

可以發現$(1, 3, 5) \in R$，因為$3=1+2$且$5=1+2\times 2$，但是$(2, 5, 9) \not \in R$，因為$5-2=3$而$9-5=4$。

此關係的階數為$3$，而其域皆為整數集合。



##### Example 3

令$R$為$\mathbb{Z} \times \mathbb{Z} \times \mathbb{Z}^+$上的關係，由有序三項$(a, b, m)$組成，其中$a$、$b$和$m$為整數、$m\ge 1$，且$a \equiv b \pmod m$。

$(8, 2, 3)$、$(-1, 9, 5)$和$(14, 0, 7)$都屬於$R$，但是$(7, 2 ,3)$、$(-2, -8, 5)$和$(11, 0, 6)$不屬於$R$。

因為$8 \equiv 2 \pmod 3$，$-1 \equiv 9 \pmod 5$和$14 \equiv 0 \pmod 7$。

然而$7 \not \equiv 2 \pmod 3$，$-2 \not \equiv -8 \pmod 5$與$11 \not \equiv 0 \pmod 6$。

此關係的階數為$3$，而其域前兩個為整數集合，第三個為正整數集合。



##### Example 4

令$R$為有序5元$(A, N, S, D, T)$所組成的關係，其中$A$為航空公司，$N$為航班數，$S$為出發地，$D$為目的地，$T$為起飛時間。

例如，中華航空的123班機在19:00由松山機場飛往澎湖機場，則(中華，123，松山，澎湖，19:00)屬於$R$。

此關係的階數為$5$，而其域為所有航空公司集合、航班集合、城市集合與時間集合。



#### Introduce - 資料庫與關係

在資料庫中進行資訊操作所需的時間與資訊儲存方式有關，以下將討論一種根據關係的概念而來的關聯式資料模型。

資料庫由紀錄組成，紀錄是由欄位形成的有序$n$項。

例如，一個學生紀錄資料庫可能包含姓名、學號、主修科系與平均分數等欄位。

關聯式資料模型將資料庫的資料以有序$n$項來表示，所以學生紀錄可以表現呈有序4元。

以下是一個簡單的資料庫，包含三筆資料：

(Jason, 590001, 資訊工程, 3.88)

(Uriah, 590002, 資訊工程, 3.66)

(Alex, 390003, 環境工程, 3.69)

因為用來表現資料庫的關係經常以表格呈現，所以這些關係也稱為表格。

表格中每一行表示資料庫的一個屬性，見以下表示方式。

| 姓名  | 學號   | 主修科系 | 平均分數 |
| ----- | ------ | -------- | -------- |
| Jason | 590001 | 資訊工程 | 3.88     |
| Uriah | 590002 | 資訊工程 | 3.66     |
| Alex  | 390003 | 環境工程 | 3.69     |

$n$元關係中稱為主鍵的域，是指有序$n$項的值可由這個域來決定，也就是說關係中沒有兩個不同的有序$n$項在主鍵的值相同。

資料庫中的紀錄經常需要增加或刪除，基於這一點，一個域是否成為主鍵的性質會隨著時間改變。

所以選用的主鍵應該是無論資料庫如何改變都能繼續使用的欄位。

在一個關係中，現有的有序$n$項聚集稱為此關係的擴展。

資料庫較固定的部分，包括資料庫的名子和屬性為其內涵。

當選擇主鍵時，目標是選一個對所有資料庫的擴展都能適用的鍵來作主鍵。

因此我們必須檢驗資料庫的擴展，來了解出現在擴展中有序$n$項集合。

在$n$元關係中，域的組合也可用來唯一地判斷出有序$n$項。

當一組域的值能判斷關係中的有序$n$項時，這些域的笛卡爾積稱為複合鍵。



##### Example 1

假設以下的表格未來不會再加入有序$n$項，則以下的表格中，哪些域是主鍵？

| 姓名       | 學號   | 主修科系 | 平均分數 |
| ---------- | ------ | -------- | -------- |
| Jason Lin  | 590001 | 資訊工程 | 3.88     |
| Uriah Xuan | 590002 | 資訊工程 | 3.69     |
| Alex Huang | 390003 | 環境工程 | 3.69     |



表中每個學生的姓名皆是唯一的有序四項，所以姓名是主鍵

學號在表中也是唯一，所以學號也是主鍵。

但主修科系、平均分數不是唯一的，所以兩者皆不是主鍵。



##### Example 2

假設以下的表格未來不會再加入有序$n$項，則以下的表格中，主修科系和平均分數的笛卡爾積是否為複合鍵？

| 姓名       | 學號   | 主修科系 | 平均分數 |
| ---------- | ------ | -------- | -------- |
| Jason Lin  | 590001 | 資訊工程 | 3.88     |
| Uriah Xuan | 590002 | 資訊工程 | 3.69     |
| Alex Huang | 390003 | 環境工程 | 3.69     |

因為在表格中沒有兩個有序四項同時有相同的主修科系和平均分數，所以主修科系跟平均分數的笛卡爾積是複合鍵。



#### Introduce - n元關係上的運算

有許多$n$元關係的運算可用來產生新的$n$元關係。

使用這些運算能回答許多資料庫上滿足某些性質的問題。

$n$元關係上最基本的運算是找出滿足某些性質的有序$n$項，見以下的定義。



#### Definition - 選擇算子

令$R$為一個$n$元關係，而$C$是$R$中元素必須滿足的條件，則選擇算子$s_c$將$n$元關係$R$對應至$n$元關係中滿足條件$C$的所有有序$n$項。

選擇算子可以用在從學生紀錄中，找到主修科系是資訊工程且平均分數大於3.7的紀錄，則可以使用選擇算子來尋找。



##### Example

| 姓名       | 學號   | 主修科系 | 平均分數 |
| ---------- | ------ | -------- | -------- |
| Jason Lin  | 590001 | 資訊工程 | 3.88     |
| Uriah Xuan | 590002 | 資訊工程 | 3.59     |
| Alex Huang | 390003 | 環境工程 | 3.79     |

從以上的表格，我們使用算子，其中$C_1$為條件「主修科系」為「資訊工程」，得到兩個有序4項。

要找到平均分數大於3.5的學生，我們用選擇算子，定義$C_2$為條件「平均分數」>「3.7」，同樣得到兩個有序4項。

最後，為了找到主修科系是資訊工程且平均分數大於3.5的紀錄，我們使用算子，其中$C_3$為條件(「主修科系」為資訊工程 $\land$ 「平均分數」> 3.7)，結果只剩下一個有序四項。



#### Definition - 投影

投影是透過刪除關係中每筆紀錄的同一欄位所產生的新$n$元關係，定義如下。

投影$P_{i_1,i_2,...,i_m}$，其中$i_1 < i_2 < ... < i_m$，將有序$n$項$(a_1, a_2, ... a_n)$對應到有序$m$項$a_{i_1}, a_{i_2}, ..., a_{i_m}$，其中$m \le n$。

也就是投影$P_{i_1,i_2,...,i_m}$刪去有序$n$項的$n-m$個分量，留下第$i_1$個分量，第$i_2$個分量、......和第$i_m$個分量。



##### Example 1

執行$P_{1, 3}$後，下列有序4項$(2, 3, 0, 4)$、$(a, b, c, d)$、$(a_1, a_2, a_3, a_4)$會變成什麼？



執行投影$P_{1, 3}$後，這些有序4項將變成$(2, 0)$、$(a, c)$、$(a_1, a_3)$。



##### Example 2

當執行投影$P_{1, 2}$後，表3的關係將會變成什麼？

| 姓名      | 主修科系   | 課程           |
| --------- | ---------- | -------------- |
| Uriah     | 資工系     | 離散數學       |
| Uriah     | 資工系     | 計算機程式設計 |
| Uriah     | 資工系     | 計算機組織     |
| Alex      | 環境工程系 | 環境工程導論   |
| Alex      | 環境工程系 | 微積分         |
| Christina | 電工系     | 電路學         |
| Christina | 電工系     | 電子學         |
| Christina | 電工系     | 微分方程       |

表3將會變成這樣。

| 姓名      | 主修科系   |
| --------- | ---------- |
| Uriah     | 資工系     |
| Alex      | 環境工程系 |
| Christina | 電工系     |



#### Definition - 連結

當表格有相同的欄位時，連結運算可以用來合併兩個表格，定義如下。

令$R$為一個$m$階關係，$S$是一個$n$階關係。

當$p \le m$且$p \le n$，連結$J_p(R, S)$是一個$m+n-p$階關係，

包含所有的有序$(m+n-p)$項$(a_1, a_2, ..., a_{m-p}, c_1, c_2, ... c_p, b_1, b_2, ... b_{n-p})$

其中有序$m$項$(a_1, a_2, ..., a_{m-p}, c_1, c_2, ..., c_p)$屬於$R$，而有序$n$項$(c_1, c_2, ..., c_p, b_1, b_2, ..., b_{n-p})$屬於$S$。



##### Example

利用連結算子將以下兩個表格連結在一起。

| 教授  | 系別       | 課程代碼 |
| ----- | ---------- | -------- |
| Uriah | 資訊工程系 | 031      |
| Uriah | 資訊工程系 | 049      |
| Alex  | 環境工程系 | 029      |
| Alex  | 環境工程系 | 011      |
| Tom   | 電子工程系 | 055      |

| 系別       | 課程代碼 | 時間  |
| ---------- | -------- | ----- |
| 資訊工程系 | 031      | 17:00 |
| 資訊工程系 | 049      | 19:00 |
| 資訊工程系 | 022      | 08:00 |
| 環境工程系 | 029      | 08:00 |
| 環境工程系 | 011      | 16:00 |
| 環境工程系 | 032      | 18:00 |
| 電子工程系 | 055      | 11:00 |

連結的結果如下

| 教授  | 系別       | 課程代碼 | 時間  |
| ----- | ---------- | -------- | ----- |
| Uriah | 資訊工程系 | 031      | 17:00 |
| Uriah | 資訊工程系 | 049      | 19:00 |
| Alex  | 環境工程系 | 029      | 08:00 |
| Alex  | 環境工程系 | 011      | 16:00 |
| Tom   | 電子工程系 | 055      | 11:00 |



### 9.3 表現關係

#### Introduce - 利用矩陣表現關係

有限集合間的關係能以01矩陣來表現。

假設$R$是由集合$A = \{a_1, a_2, ..., a_m\}$到集合$B=\{b_1, b_2, ..., b_n\}$，集合可以隨意排序，若A=B則使用相同的排列順序。

關係$R$能以矩陣$M_R = [m_{ij}]$表示，其中$m_{ij} = \left\{ \begin{array}\ 1 & \text{if } (a_i, b_j) \in R \\ 0 & \text{if } (a_i, b_j) \not\in R \end{array}\right.$



##### Example 1

假設$A=\{1, 2, 3\}$，$B=\{1, 2\}$。

令$R$為由$A$到$B$的關係，包含所有的有序對$(a, b)$，如果$a \in A$且$b \in B$，而且$a > b$。

則$R$的矩陣表示法為何？其中$a_1 = 1, a_2 = 2, a_3 = 3$，而且$b_1 = 1, b_2 = 2$。



因為$R=\{(2, 1), (3, 1), (3, 2)\}$，$R$的矩陣為$M_R = \begin{bmatrix} 0 & 0 \\ 1 & 0 \\ 1 & 1 \end{bmatrix}$

$M_R$中的$1$說明$(2, 1)$、$(3, 1)$和$(3, 2)$屬於$R$，而$0$說明沒有其他的有序對屬於$R$。



##### Example 2

令$A = \{a_1, a_2, a_3\}$，$B = \{b_1, b_2, b_3, b_4, b_5\}$。

若$R$的矩陣如下，則哪些有序對在關係$R$中？

$M_R = \begin{bmatrix} 0 & 1 & 0 & 0 & 0 \\ 1 & 0 & 1 & 1 & 0 \\ 1 & 0 & 1 & 0 & 1\end{bmatrix}$



由上面的矩陣可知，$\{(a_1, b_2), (a_2, b_1), (a_2, b_3), (a_2, b_4), (a_3, b_1), (a_3, b_3), (a_3, b_5)\} \in R$



#### Introduce - 反身性、對稱性、反對稱性與方陣

若$R$是反身性，則方陣$M_R$的主對角線皆為1。

例如：$\begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$，也就是非主對角線的矩陣元素$m_{ii} = 1$

若集合$A = \{a_1, a_2, ..., a_n\}$上的關係$R$是對稱性的，若且唯若當$(a_i, a_j) \in R$，能推導出$(a_j, a_i) \in R$。

例如：$\begin{bmatrix} 1 & 0 & 1 \\ 0 & 0 & 1 \\ 1 & 1 & 1 \end{bmatrix}$，也就是非主對角線的矩陣元素$m_{ij} \oplus m_{ji} = 0, i \neq j$，也可以寫成若且為若$M_R = (M_R)^t$

若$R$是反對稱性的，若$(a, b) \in R$且$(b, a) \in R$，則$a = b$。

例如：$\begin{bmatrix} 1 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 1 \end{bmatrix}$，也就是非主對角線的矩陣元素$m_{ij} \oplus m_{ji} = 1, i \neq j$



##### Example

假設表現關係$R$的方陣為$M_R  = \begin{bmatrix} 1 & 1 & 0 \\ 1 & 1 & 1 \\ 0 & 1 & 1 \end{bmatrix}$，判斷$R$是否為反身性的？是否為對稱性的？是否為反對稱性的？



主對角線都為1，因此是反身性的。

對於所有非主對角線的元素$m_{ij} = m_{ji}$，因此是對稱性的。

因為是對稱性的，就不會是反對稱性，所以不是反對稱性的。



#### Introduce - 聯合、交遇與矩陣

假設$R_1, R_2$為集合$A$上的關係，分別由矩陣$M_{R_1}$與$M_{R_2}$表示。

如果$M_{R_1}$或$M_{R_2}$在某個位置上的元素為1，則兩個關係之聯集的矩陣在同一位置的元素為1。

如果$M_{R_1}$且$M_{R_2}$在某個位置上的元素為1，則兩個關係之交集的矩陣在同一位置的元素為1。

可以寫成這樣的定義：$M_{R_1 \cup R_2} = M_{R_1} \lor M_{R_2}$，$M_{R_1 \cap R_2} = M_{R_1} \land M_{R_2}$。



##### Example 

假設$R_1$和$R_2$為集合$A$上的關係，其表現矩陣分別為

$M_{R_1} = \begin{bmatrix} 1 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{bmatrix}$與$M_{R_2} = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 1 \\ 1 & 0 & 0 \end{bmatrix}$，表現$R_1 \cup R_2$和$R_1 \cap R_2$的矩陣為何？



$M_{R_1 \cup R_2} = M_{R_1} \lor M_{R_2} = \begin{bmatrix} 1 & 0 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 0 \end{bmatrix}$

$M_{R_1 \cap R_2} = M_{R_1} \land M_{R_2} = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}$



#### Introduce - 合成關係與矩陣

有序對$(a_i, c_j)$屬於$S \circ R$，若且為若存在$k$使得$r_{ik} = s_{kj} = 1$。

根據布林積的定義，$M_{S \circ R} = M_R \odot M_S$



##### Example

求出表現關係$S \circ R$的矩陣，其中表現$R$與$S$的矩陣分別為

$M_R = \begin{bmatrix} 1 & 0 & 1 \\ 1 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix}$與$M_S = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 1 \end{bmatrix}$



$S \circ R$的表現矩陣為$M_{S \circ R} = M_R \odot M_S = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 1 \\ 0 & 0 & 0 \end{bmatrix}$



#### Introduce - 布林冪次與矩陣

表現兩關係合成的概念能用來找出$M_{R^n}$，可以由以下的定義找出：

$M_{R^n} = M_R^{[n]}$



##### Example 

求出表現關係$R^2$的矩陣，其中表現$R$的矩陣為

$M_R = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 0 \end{bmatrix}$



$M_{R^2} = M^{[2]}_R = \begin{bmatrix} 0 & 1 & 1 \\ 1 & 1 & 1 \\ 0 & 1 & 0 \end{bmatrix}$



#### Definition - 有向圖

一個有向圖包含一個頂點的集合$V$，以及一個$V$中元素之有序對行成的集合$E$，其元素稱為邊。

頂點$a$稱為邊$(a, b)$的初始點，而頂點$b$稱為終點。

用$(a, a)$所形成的邊用一個由頂點$a$到本身的弧來表現，稱為迴圈。



##### Example

以$a, b, c, d$為頂點，$(a, b), (a, d), (b, b), (b, d), (c, a), (c, b)$和$(d, b)$為邊所形成的有向圖如下。

![image-20210610164738806](https://i.imgur.com/X9rA6O7.png)



#### Introduce - 利用有向圖表現關係

集合$A$上的關係$R$能以有向圖來表示。

將$A$的元素當成頂點，$(a, b)$為有向圖上的邊，代表$(a, b) \in R$，能夠用這樣的方式來建立一對一關係。



##### Example 1

利用有向圖，表現在集合$\{1, 2, 3, 4\}$上的關係$R = \{(1, 1), (1, 3), (2, 1), (2, 3), (2, 4), (3, 1), (3, 2), (4, 1)\}$

![image-20210610165002061](https://i.imgur.com/x4LOkV0.png)



##### Example 2

若表現關係$R$的有向圖如下圖所示，則關係中的有序對為何？

![image-20210610165335599](https://i.imgur.com/Yy296Xn.png)



$R = \{(1, 3), (1, 4) (2, 1), (2, 3), (3, 1), (4, 1), (4, 3)\}$



#### Introduce - 關係性質與有向圖

若關係是反身性的，若且為若每個頂點必定有迴圈。

若關係是對稱性的，若且為若任意兩個頂點若有一條有向邊，則必定存在另一條反向的有向邊。

若關係是反對稱性的，若且為若任意兩個頂點僅有一條有向邊，不存在兩個頂點同時有兩條有向邊。

若關係是遞移性的，若且為若領當有一條邊指向$(x, y)$，一條邊指向$(y, z)$，則必定有一條邊指向$(x, z)$。



##### Example 1

判斷以下的有向圖所表現出的關係是否為反身性，是否為對稱性，是否為反對稱性，以及是否為遞移性的。

![image-20210610171923898](https://i.imgur.com/VQVRLUl.png)

關係是反身性的，因為每個頂點都有迴圈。

關係是不是對稱性的，也不是反對稱性的。

關係也不是遞移性的，因為有a到b與b到c的邊，但是沒有a到c的邊。



##### Example 2

判斷以下的有向圖所表現出的關係是否為反身性，是否為對稱性，是否為反對稱性，以及是否為遞移性的。

![image-20210610172544947](https://i.imgur.com/ePq6PVM.png)



有頂點沒有迴圈，所以不是反身性的。

關係是對稱性的，因為每個指向兩個頂點的有向邊都有一條反向的有向邊，也因此關係不是反對稱性的。

關係不是遞移性的，因為$(a,b)$，$(c, a)$在觀下中但是沒有指向$(c, b)$的邊。



### 9.4 關係的閉包

#### Introduce - 閉包

令$R$是集合$A$的上的關係，可能具有或不具有某種性質$P$。

如果存在包含$R$且具有性質$P$的關係$S$，並且$S$是包含$R$且具有性質$P$的每一個關係的子集，稱$S$為$R$關於$P$的閉包。



#### Introduce - 反身閉包

已知集合$A$上的關係$R$。

對所有的$a \in A$，除了已在$R$中的之外，可以透過將所有如$(a, a)$的序對都加入$R$中，就構成$R$的反身閉包。



##### Example

整數集合上的關係$R = \{(a, b) | a < b\}$，其反身閉包為何？



$R$的反身閉包$S = \{(a, b) | a < b\} \cup \{(a, a) | a \in \mathbb{Z}\} = \{(a, b) | a \le b\}$



#### Introduce - 對稱閉包

關係$R$的對稱閉包可以透過增加所有$(a, b)$在關係中而$(b, a)$不在關係中的有序對$(b, a)$來產生。

增加這些有序對產生一個對稱關係，包含了$R$，而且是任何包含$R$之對稱關係的子集。

對稱閉包可以透過原關係及其逆關係的聯集來加以建構。

也就是$R$的對稱逆包可以寫成$R \cup R^{-1}$，其中$R^{-1} = \{(b, a) | (a, b) \in R\}$



##### Example

正整數集合上的關係$R = \{(a, b) | a > b\}$，其對稱閉包為何？



$R \cup R^{-1} = \{(a, b) | a > b\} \cup \{(b, a) | a > b\} = \{(a, b) | a \neq b\}$



#### Definition - 路徑

在有向圖$G$中，從$a$到$b$的路徑(path)是指$G$中一個邊的序列$(x_0, x_1), (x_1, x_2) ... (x_{n-1}, x_n)$，其中$n$為正整數，且$x_0 = a$和$x_n = b$。

也就是說，路徑是邊的序列，其中路徑的任一個邊的終點與下一個邊的始點相同，可以記為$x_0, x_1, x_2, ..., x_{n-1}, x_n$，長度為$n$。

不包含邊的序列視為一條從$a$到$a$的路徑，也就是從$a$到$a$但長度為$0$的序列視為一條路徑。

當$n \ge 1$，在同一頂點開始和結束的路徑叫做還道(circuit)或迴圈(cycle)。



##### Example

下面哪些序列是下圖有向圖中的路徑：$a, b, e, d$、$a, e, c, d, b$、$b, a, c, b, a, a, b$、$d, c$、$c, b, a$、$e,b,a,b,a,b,e$

這些路徑的長度是多少，哪些路徑是環道？



逐一檢驗路徑。

$(a, b), (b, e), (e, d)$ 都是有向圖上的邊，因此$a, b, e, d$是個長度為3的路徑。

$(a, e),(e, c),(c, d),(d, b)$中，$(c, d)$有向邊不存在，故$a, e, c, d, b$不是路徑。

$(b, a), (a, c), (c, b), (b, a), (a, a), (a, b)$都是有向圖上的邊，因此$b,a,c,b,a,a,d$是個長度為6的路徑

且因為開始的頂點與結束的頂點相同，因此$b,a,c,b,a,a,d$是個環道。

$(d, c)$是有向圖上的邊，因此$d, c$是長度為1的路徑。

$(c, b), (b, a)$都是有向圖上的邊，因此$c, b, a$是個長度為2的路徑。

$(e, b), (b, a), (a, b), (b, a), (a, b), (b, e)$都是有向圖上的邊，因此$e,b,a,b,a,b,e$是個長度為6的路徑

且因為開始的頂點與結束的頂點相同，因此$e,b,a,b,a,b,e$是個環道。



#### Theorem - 關係與路徑

令$R$是集合$A$上的關係。從$a$到$b$存在一條長度為$n$的路徑，若且唯若$(a, b) \in R^n$



##### Proof

我們使用數學歸納法來證明

考慮$n=1$，從$a$到$b$存在一條長度為$1$的路徑，若且唯若就是$(a, b) \in R$

考慮正整數$n$時定理會為真，若從$a$到$b$存在一條長度為$n+1$的路徑，若且唯若存在元素$c \in A$，使得從$a$到$c$存在一條長度為$1$的路徑，以及一條從$c$到$b$的長度為$n$的路徑，也就是$(c, b) \in R^n$。

因此，由歸納假設，從$a$到$b$存在一條長度為$n+1$的路徑等價於存在一個元素$c$，使得$(a, c) \in R$和$(c, b) \in R^n$。

因此，$(a, b) \in R^{n+1}$，因此，從$a$到$b$存在一條長度為$n+1$的路徑等價於$(a, b) \in R^{n+1}$，得證。



#### Definition - 遞移閉包

令$R$是集合$A$的關係。

連通關係$R^*$由元素對$(a, b)$組合，使得由$a$到$b$之間存在一條長度至少為$1$的路徑於$R$中。



##### Example

令$R$是世界上所有人這個集合上的關係，如果$a$認識$b$，則$R$包含$(a, b)$。

$R^n$代表什麼意義？其中$n$是大於$2$的正整數，$R^*$又代表什麼？



如果存在某人$c$，使得$(a, c) \in R$ 和 $(c, b) \in R$，亦即存在某人$c$使得$a$認識$c$且$c$認識$b$，則關係$R^2$包含$(a, b)$。

同樣地，如果存在$x_1, x_2, ..., x_{n-1}$使得$a$認識$x_1$，$x_1$認識$x_2$，......，$x_{n-1}$認識$b$，則$R^n$包含$(a, b)$。





#### Theorem - 連通關係

關係$R$的遞移閉包等於連通關係$R^*$。



##### Proof

由定義可知$R^*$包含$R$。

為證明$R^*$是$R$的遞移閉包，必須證明$R^*$是遞移性，而且對一切包含$R$的遞移關係$S$有$R^* \subseteq S$。

首先，證明$R^*$是遞移性的，如果$(a, b) \in R^n$ 和 $(b, c) \in R^n$，則在$R$中分別存在從$a$到$b$和從$b$到$c$的路徑。

以從$a$到$b$的路徑開始，接上從$b$到$c$的路徑就得到一條從$a$到$c$的路徑，因此$(a, c) \in R^*$。

所以$R^*$是遞移性的。

現在假設$S$是包含$R$的遞移關係。因為$S$是遞移性的，$S^n$也是遞移性的，而且$S^n \subseteq S$。

此外，因為$S^* = \displaystyle \bigcup^\infty_{k=1} S^k$而且$S^k \subseteq S$，因此$S^* \subseteq S$。

從上面可以發現如果$R \subseteq S$，則$R^* \subseteq S^*$，因為任何$R$中的路徑也是$S$中的路徑，所以$R^* \subseteq S^* \subset S$。

於是，任何包含$R$的遞移關係$S$也一定包含$R^*$，因此，$R^*$是$R$的遞移閉包。



#### Lemma 1

令$A$是$n$元素的集合。$R$是$A$上的關係。

如果在$R$中存在一條從$a$到$b$的路徑，則存在一條長度不超過$n$的路徑。

此外，當$a \neq b$時，如果在$R$中存在一條從$a$到$b$的路徑，則存在一條長度不超過$n-1$的路徑。



##### Proof

假設$R$中存在從$a$到$b$的路徑，令$m$是這種路徑中最短的長度。

假設$x_0, x_1, x_2, ..., x_{m-1}, x_m$是一條從$a$到$b$的路徑，其中$x_0 = a$，$x_m = b$。



假設$a = b$且$m > n$，則在$m$個頂點中必定有重複的點（鴿洞原理）

假設$x_i = x_j$且$0 \le i < j \le m-1$，則這條路徑包含一條從$x_i$到$x_i$的迴路。

將這條迴路刪除之後，剩下的路徑必定比原先的還要短，與原先$m$是最短路徑有矛盾，所以$m$必定不可能大於$n$。

因此，此種路徑的最短長度一定小於等於$n$。



考慮到$a \neq b$，因為從$a$到$b$不存在環（若存在環，刪除環的路徑後的$m' < m$，與最短路徑$m$矛盾）

也就是每個頂點到頂點之間至多經過一次，也就是最短長度一定小於等於$n-1$。



#### Theorem - 0-1矩陣與遞移閉包

令$M_R$是$n$元素集合上關係$R$的0-1矩陣。

則遞移閉包$R^*$的0-1矩陣是$M_{R^*} = M_R \lor M_R^{[2]} \lor M_R^{[3]} \lor ...\lor M_R^{[n]}$



##### Proof

根據Lemma 1，可以看出遞移閉包是$R、R^2、R^3、......、R^n$的聯集。

因為在$R^*$的兩個頂點之間存在一條路徑，若且唯若對某個正整數$i(i \le n)$在$R^i$中，此兩點頂點之間存在一條路徑。

因此，$R^* = R \cup R^2 \cup R^3 \cup ... \cup R^n$

我們可以把關係寫成矩陣，得到$M_{R^*} = M_R \lor M_R^{[2]} \lor M_R^{[3]} \lor ...\lor M_R^{[n]}$



##### Example

求出關係$R$之遞移閉包的0-1矩陣，其中$M_R = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 0 \end{bmatrix}$



由定理$3$可知$M_{R^*} = M_R \lor M^{[2]}_R \lor M^{[3]}_R$

因此$M_R^{[2]} = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 1 \end{bmatrix}$，$M_{R}^{[3]} = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 1 \end{bmatrix}$

所以$M_{R^*} = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 0 \end{bmatrix} \lor \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 1 \end{bmatrix} \lor \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 1 & 1 \\ 0 & 1 & 0 \\ 1 & 1 & 1\end{bmatrix}$



#### Introduce - Warshall演算法

假設$R$是$n$元集合上的關係，假設$v_1, v_2, ..., v_n$是這$n$個元素的任意排列。

Warshall演算法使用路徑內點的概念，如果$a, x_1, x_2, ..., x_{m-1}, b$是一個路徑，它的內點是$x_1, x_2, ..., x_{m-1}$。

例如有向圖的一條路徑$a, c, d, f, g, h, b, j$的內點是$c, d, f,g, h, b$。



Warshall演算法的基礎是建構一系列的0-1矩陣。

這些矩陣的定義為$W_0, W_1, ..., W_n$，其中$W_0 = M_R$是這個關係的0-1矩陣，且$W_k = w_{ij}^{(k)}$。

如果存在一條從$v_i$到$v_j$的路徑，使得這條路徑的所有內點都在集合$\{v_1, v_2, ..., v_k\}$之中，則${w_{ij}^{(k)}} = 1$，否則${w_{ij}^{(k)}} = 0$。

而$W_n = M_{R^*}$，因為$M_{R^*}$的第$(i, j)$項是1，若且唯若存在一條從$v_i$到$v_j$的路徑，而且全部內點都在集合$\{v_1, v_2, ..., v_n\}$中。



##### Example

令$R$是一個關係，其有向圖如下表示，假設$a, b, c, d$是集合元素的排列。

求出矩陣$W_0, W_1, W_2, W_3, W_4$，其中矩陣$W_4$是$R$的遞移閉包。

![image-20210613212024452](https://i.imgur.com/zr8AbjX.png)



由圖上可知，假設$v_0 = a, v_1 = b, v_2 = c, v_3 = d$

則$W_0 = \begin{bmatrix} 0 & 0 & 0 & 1 \\ 1 & 0 & 1 & 0 \\ 1 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{bmatrix}$

若存在一條路徑從$v_i$到$v_j$，且內點由$a$組成，則$W_1$的$(i. j)$項為$1$，長度為1本身無內點依然可以使用

因此$W_1 = \begin{bmatrix} 0 & 0 & 0 & 1 \\ 1 & 0 & 1 & 1 \\ 1 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{bmatrix}$

若存在一條路徑從$v_i$到$v_j$，且內點由$a, b$組成，則$W_2$的$(i. j)$項為$1$，由於$b$不會是終點

所以$W_2 = W_1 = \begin{bmatrix} 0 & 0 & 0 & 1 \\ 1 & 0 & 1 & 1 \\ 1 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{bmatrix}$

若存在一條路徑從$v_i$到$v_j$，且內點由$a, b, c$組成，則$W_3$的$(i. j)$項為$1$，例如$d, c, d$或者$d, c, a$

所以$W_3 = \begin{bmatrix} 0 & 0 & 0 & 1 \\ 1 & 0 & 1 & 1 \\ 1 & 0 & 0 & 1 \\ 1& 0 & 1 & 1 \end{bmatrix}$

若存在一條路徑從$v_i$到$v_j$，且內點由$a, b, c, d$組成，也就是只要存在一條路徑使得$v_i$能到$v_j$，則$W_4$的$(i. j)$項為$1$。

因此$W_4 = \begin{bmatrix} 1 & 0 & 1 & 1 \\ 1 & 0 & 1 & 1 \\ 1 & 0 & 1 & 1 \\ 1& 0 & 1 & 1 \end{bmatrix}$

而$W_4$就是遞移閉包的矩陣。



#### Lemma 2

令$W_k = [w_{ij}^{[k]}]$是0-1矩陣，在$(i, j)$的位置上為1，若且唯若存在一條從$v_i$到$v_j$內點取自集合$\{v_1, v_2, ..., v_k\}$的路徑，則

$w_{ij}^{[k]} = w_{ij}^{[k-1]} \lor (w_{ik}^{[k-1]} \land w_{kj}^{[k-1]})$

其中$0 < i,j,k \le n$。



##### Proof

考慮算法的過程，存在一條從$v_i$到$v_j$的路徑，且只以$v_1, v_2, ... , v_k$中的頂點作為內點，若且唯若存在一條從$v_i$到$v_j$且內點是序列中的前$k-1$個頂點的路徑，或者存在從$v_i$到$v_k$和從$v_k$到$v_j$的路徑，而這些路徑的內點是表中前$k-1$個頂點。

也就是說，若$w_{ij}^{[k]} = 1$，則有兩種可能的情況：

在$v_k$做為內點之前，從$v_i$到$v_j$本身就連通，也就是$w_{ij}^{[k-1]} = 1$

以$v_k$作為內點產生一條從$v_i$到$v_k$且$v_k$到$v_j$的路徑，也就是$w_{ik}^{[k-1]} \land w_{kj}^{[k-1]} = 1$



### 9.5 等價關係

#### Definition - 等價關係

如果集合$A$上的關係是反身性、對稱性和遞移性的，則稱為等價關係。

在等價關係中，兩個有關係的元素可視為等價的，記為$a \sim b$。



##### Example 1

令$R$是實數集合上的關係，$a\ R\  b$若且唯若$a-b$是整數。$R$是否為等價關係？



1. 對所有實數$a$來說，$a-a = 0$，因此對所有實數，$a\ R\ a$，也就是$R$是反身性的。
2. 假設$a\ R\ b$，則$a-b$是整數，所以$b-a$也是整數，因此$b\ R\ a$，故$R$是對稱性的。
3. 如果$a\ R\ c$且$c\ R\ b$，則$a-b$和$b-c$是整數，所以$a-c = (a-b) + (b-c)$也是整數，因此$a\ R\ c$，故$R$是遞移性的。

以上，所以$R$是等價關係。



##### Example 2

令$m$是大於$1$的正整數。

證明關係$R = \{(a, b) | a \equiv b \pmod m\}$是整數集合上的等價關係。



1. $a \equiv b \pmod m \iff (a-b) \text{ mod } m = 0$，又因為若$a=b$，則$a-b=0$，而$0 \text{ mod } m =0$，因此$a-a=0$被$m$整除

   因此關係$R$是反身性的。

2. 若$a \equiv b \pmod m$，則$a - b = km$，則$b-a = (-k)m$，因此$b \equiv a \pmod m$

   因此關係$R$是對稱性的。

3. 若$a \equiv b \pmod m$且$b \equiv c \pmod m$，則存在$a-b=km$且$b-c=lm$

   將兩式相加得$(a-b)+(b-c)=(k+l)m$，因此$a \equiv c \pmod m$

   因此關係$R$是遞移性的。

以上，所以$R$是等價關係。



##### Example 3

令$n$為正整數，$S$為字串集合。

假設$R_n$為$S$上的關係，$s\ R_n\ t$若且唯若$s = t$，或是兩個字串$s$與$t$的前$n$個字元完全一樣，所以長度小於$n$的字串只與自身有關係。

例如，令$n=3$，$S$為所有的位元字串，則$01\ R_3\ 01$，與$00111\ R_3\ 00101$，但$01\ \not R_3 010$，$01011\ \not R_3\ 01110$。

證明對所有的字串集合和所有的正整數$n$，$R_n$都是$S$上等價關係。



1. 對於每個在字串集合$S$的字串$s$而言，$s=s$，也就是$s\ R_n\ s$，因此$R$有反身性。
2. $s\ R_n\ t$則$s=t$或是前$n$個字元一樣，也就是說$t = s$，且$t$的前$n$個字元與$s$一樣，故$t\ R_n\ s$也合理，因此$R$有對稱性
3. 若$s\ R_n\ t$且$t\ R_n u$，則$s, t$前$n$個字元一樣，$t, u$前$n$個字元一樣，也就能推出$s,u$前$n$個字元一樣，故$s\ R_n\ u$，因此$R$有遞移性

以上，所以$R$是等價關係。



##### Example 4

證明正整數集合上的「整除」關係不是等價關係。



設$R$為整除關係，若$a\ R\ b$則代表$b$可以被$a$整除。

考慮到$b=a$的情況，自己可以整除自己，因此$R$是反身性的。

考慮到$a \neq b$的情況，若$a\ R\ b$則$b\ R\ a$不一定成立，例如$a = 2, b = 4$，則$2\ R\ 4$成立但$4\ R\ 2$不成立

因此$R$不是對稱性的。

因此整除關係不是等價關係。



##### Example 5

令$R$為實數集合上的關係。

$x\ R\ y$若且唯若$x$與$y$的差小於$1$，也就是$|x-y|<1$，證明$R$不是等價關係。



考慮反身性，若$x=y$，則$|x-y|=|x-x|=0$，故$R$是反身性的。

考慮對稱性，若$x=y$且$|x-y|<1$，則$|y-x|<1$，故$R$是對稱性的。

考慮遞移性，若$x=9.1, y = 8.7, z= 7.8$，則$|x-y|=|9.1-8.7|=0.4<1$，且$|y-z|=|8.7-7.8|=0.9<1$。

但$|x-z|=|9.1-7.8|=1.3>1$，故$R$不是遞移性的。

因此關係$R$不是等價關係。



#### Definition - 等價類

令$R$是集合$A$上的等價關係。

與$A$中元素$a$有關係的所有元素之集合稱為$a$的等價類，記作$[a]_{R}$，其中$[a]_{R} = \{s | (a, s) \in R\}$

當只考慮一個關係時，可以省去下標$R$，記作$[a]$。



##### Example 1

在模$4$的同餘關係中，0和1的等價類是什麼？



0的等價類包含滿足$a \equiv 0 \pmod 4$的所有整數$a$，這個類包含所有能被4整除的整數。

因此，$[0] = \{...,-8,-4,0,4,8,...\}$

1的等價類包含滿足$a \equiv 1 \pmod 4$的所有整數$a$，這個類包含所有能被$4$除而餘數為$1$的整數。

因此，$[1] = \{...,-7,-3,1,5,9,...\}$



##### Example 2

令$n$為正整數，$S$為字串集合。

假設$R_n$為$S$上的關係，$s\ R_n\ t$若且唯若$s = t$，或是兩個字串$s$與$t$的前$n$個字元完全一樣，所以長度小於$n$的字串只與自身有關係。

例如，令$n=3$，$S$為所有的位元字串，則$01\ R_3\ 01$，與$00111\ R_3\ 00101$，但$01\ \not R_3 010$，$01011\ \not R_3\ 01110$。

考慮關係$R_3$中，字串$0111$的等價類為何？



$[0111]_3 = [011]_3  = \{011, 0110, 0111, 01100, 01101, 01110, 01111, ...\}$



#### Theorem - 等價關係與命題等價

令$R$是集合$A$上的等價關係，當$a, b \in R$，則下列命題等價。

- $a\ R\ b$
- $[a] = [b]$
- $[a] \cap [b] \neq \varnothing$



##### Proof

第一個命題等價可以推得第二個命題等價。

假設$a\ R\ b$，再假設$c \in [a]$，則$a\ R\ c$，因為$a\ R\ b$且$R$有等價關係，也就是$R$有對稱性，故$b\ R\ a$。

又因為$R$有遞移性所以可以用$b\ R\ a$與$a\ R\ c$推得$b\ R\ c$，因此有$c \in [b]$，故$[a] \subseteq [b]$。

再假設$c \in [b]$，則$b\ R\ c$，因為$b\ R\ a$且$R$有等價關係，也就是$R$有對稱性，故$a\ R\ b$。

又因為$R$有遞移性所以可以用$a\ R\ b$與$b\ R\ c$推得$a\ R\ c$，因此有$c \in [a]$，故$[b] \subseteq [a]$。

綜合以上，$[a] \subseteq [b]$且$[b] \subseteq [a]$，得到$[a] = [b]$。



第二個命題等價可以推得第三個命題等價。

假設$[a] = [b]$，則證明$[a] \cap [b] \neq \varnothing$，因為$R$具有反身性，故$a\ R\ a$成立，因此$[a]$一定是非空集合。



第三個命題等價可以推得第一個命題等價。

假設$[a] \cap [b] \neq \varnothing$，則存在元素$c$使得$c \in [a]$且$c \in [b]$，也就是$a\ R\ c$且$b\ R\ c$。

利用對稱性可以知$c\ R\ b$，利用遞移性，可以用$a\ R\ c$與$c\ R\ b$組出$a\ R\ b$。



因此，三個命題是等價的。



#### Introduce - 分割

集合$S$的分割是一組$S$的不相交非空子集合，他們的聯集正好等於$S$。

也就是唯若對於$i \in I, A_i \neq \varnothing$，且當$i \neq j$，$A_i \cap A_j = \varnothing$，則$\displaystyle \bigcup_{i \in I} A_i = S$



##### Example

假設$S = \{1, 2, 3, 4, 5, 6\}$，集合$A_1 = \{1, 2, 3\}$，且$A_2 = \{4, 5\}$，$A_3 = \{6\}$構成$S$的一個分割。

這些集合互不相交且聯集為$S$。



#### Theorem - 分割與等價關係

令$R$是集合$S$上的等價關係，則$R$的等價類構成$S$的分割。

反之，設定集合$S$的分割$\{A_i | i \in I\}$，則存在著等價關係$R$，它以集合$A_i$作為等價類，其中$i \in I$。



##### Proof

待補。



##### Example 1

列出等價關係$R$中的有序對，假設$S = \{1, 2, 3, 4, 5, 6\}$，$A_1 = \{1, 2, 3\}$，$A_2 = \{4, 5\}$和$A_3 = \{6\}$構成$S$的分割。



在分割中的子集合為$R$的等價類。

序對$(a, b) \in R$若且唯若$a \in A_i$且$b \in A_i$，其中$i \in I$。

因此，$(1, 1), (1, 2), (1, 3), (2, 1), (2, 2), (2, 3), (3, 1), (3, 2), (3, 3)$屬於$R$，因為$A_1$是一個等價類。

$(4, 4), (4, 5), (5, 4), (5, 5)$屬於$R$，因為$A_2$是一個等價類，$(6, 6)$屬於$R$，因為$A_3$是一個等價類。

除此之外，沒有其他序對屬於$R$。



##### Example 2

在模4同餘產生的整數分割中的集合是什麼？



存在4個同餘類，分別對應$[0]_4, [1]_4, [2]_4, [3]_4$，其中

$[0]_4 = \{..., -8, -4, 0, 4, 8, ...\}$

$[1]_4 = \{..., -7, -3, 1, 5, 9, ...\}$

$[2]_4 = \{..., -6, -2, 2, 6, 10, ...\}$

$[3]_4 = \{..., -5, -1, 3, 7, 11, ...\}$

