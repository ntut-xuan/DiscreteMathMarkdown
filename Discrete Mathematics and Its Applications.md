# 離散數學 - 筆記

Author: NTUT 109級資工系 黃漢軒



> 2021/04/28 筆記突破60000字 :tada:



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



#### Recall - 一些有關若為且若的邏輯等價

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

關於量詞與謂語的邏輯等價，若兩邊敘述若為且若擁有相同的真值，則我們稱他為邏輯等價。

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

若為且若集合$A$的每個元素都為集合$B$的元素，則我們說$A$是$B$的子集合，且$B$為$A$的父集合。

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

函數$f$被稱做一對一函數，或者稱做單射，也就是對於所有在定義域的$a, b$，若為且若$f(a) = f(b)$，則$a = b$。

函數$f$如果是一對一函數，則這個函數是個單射函數。



#### Introduce - 滿射

若有兩集合$A, B$，若為且若所有元素$b \in B$，存在一個$a \in A$，使得$f(a) = b$，則稱做這個函數為滿射函數。



#### Introduce - 對射

若一個函數是一對一函數，且函數滿射，則我們稱作這個函數是一對一對應函數或叫做對射函數。



#### Introduce - 反函數

令$f$是一個集合$A$對集合$B$的對射函數，$f$的反函數寫作$f^{-1}$。

反函數$f^{-1}$代表集合$B$對集合$A$的函數，定義為若為且若$f^{-1}(y) = x$則$f(x) = y$。



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

- 令A與B為兩個集合，若為且若A與B對射，則集合A與集合B的勢是相同的，寫作$|A| = |B|$。

- 令A與B為兩個集合，若為且若A與B單射，則集合A的勢小於等於集合B的勢，寫作$|A| \le |B|$。

  如果集合A的勢與集合B的勢不同，則$|A| < |B|$。

- 一個集合如果是有限的，或者與正整數集合的勢相同，則我們說這個集合是可數的，否則就是不可數的。

  例如一個實數集合是個不可數的集合。

- 如果一個無限的集合是可數的，他的勢為$ℵ_0$，寫作$|S| = ℵ_0$，且唸做"aleph null"。

- 一個無限集合的勢，若為且若可以將所有的元素列成一個數列，則我們說這個無限集合的勢是可數的。

  原因是一個無限集合的勢，可以寫作一個對射函數，且函數的index是正整數，故我們可以寫成這樣的形式：

  $f(1) = a_1, f(2) = a_2, ... f(n) = a_n$

  故根據「一個集合如果是有限的，或者與正整數集合的勢相同，則我們說這個集合是可數的」，我們可以知道無限集合的勢，若為且若可以將所有的元素列成一個數列，則我們說這個集合是無限的。



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

根據勢的定義，「一個無限集合的勢，若為且若可以將所有的元素列成一個數列，則我們說這個無限集合的勢是可數的。」

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

兩個整數$a, b$能夠同餘模$m$，若為且若$a$除以$m$與$b$除以$m$的餘數相同。

如果$a$除以$m$與$b$除以$m$的餘數不同，那麼我們表示為$\displaystyle a \not\equiv b \pmod m$



#### Theorem 4

令$m$為一正整數，整數$a, b$能夠同餘於$m$，若為且若存在一個$k$使得$a = b + km$



##### Proof

若$a \equiv b \pmod m$，那麼$m | (a-b)$

因此，會存在一個$k$，使得$mk = a-b$，因此$a = mk+b$

反之，若存在一個$k$使得$a = b+km$，那麼$km = a-b$，因此可以得知$m | (a-b)$和$a \equiv b \pmod m$



#### Introduce - 兩個不同的表示法(mod m) 與 mod m

- $a \equiv b \pmod m$與$a \text{ mod } m = b$是不同的東西
  - $a \text{ mod } m = b$, 代表函數的關係。
  - $a \equiv b \pmod m$, 代表一個整數集合的關係。



#### Theorem 5

令$a, b$為整數，令$m$為正整數，則$a \equiv b \pmod m$ 若為且若 $a \text{ mod } m = b \text{ mod } m$。



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

設定整數$a, b$讓$f(p)$變成雙射函數，函數$f(p)$為雙射函數若為且若$\gcd(a, 26) = 1$

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



#### Example

假設有一個無限階梯，我們已知我們可以抵達第一階，就能抵達第二階，利用數學證明法來證明我們可以抵達每一階。



設$P(n)$為一命題，代表我們可以踏上第$n$階階梯

基礎步驟：$P(1)$為真，因為我們可以踏上第一階。

歸納步驟：我們假設$P(k)$為真，代表我們可以踏上前$k$階階梯，那麼對於所有大於等於$2$的正整數$k$，我們可以抵達$k+1$階，只要我們能夠踏上$k-1$階，根據歸納假設可知我們可以抵達$k$階，因此我們可以抵達$k+1$階。

因此，我們可以抵達所有的階梯。





