# **04_ランダムな数を出力**

## **あらかじめ作られたプログラムを使う**

あらかじめ作られたクラス（処理の設計図）を自分で作るプログラムに組み込むことができます。

ここでは、アプリ開発でよく使うrandom関数を紹介します。

<br>

## **メソッドとは**

変数やリストに対して、操作方法を指示することができます。  
WriteLine メソッドや Nextメソッドのように、便利なメソッドが多数用意されています。  

<br>

### **メソッドの例：**  

- Console.WriteLine(data) ：指定したデータを出力する（改行あり）
- Console.Write(data) ：指定したデータを出力する（改行なし）
- random.Next() ：0以上のランダムな数値を作成する

## **randomクラス**  

「乱数」を生成する関数

「乱数」とは・・・ランダムな数のことでプログラムを実行するたびに結果が変わる値のことです。ランダムとは規則性がなく予測が不可能な状態のことです。  

random関数を使うと指定した範囲内の数をランダムに生成して返してくれます。  
実際に動かして確認してみよう。何度か実行して結果が違うことを確認してみよう。

<br>

0~10の数値をランダムに出力します

```c#

  var random = new Random();      // クラスを実体化
  var number = random.Next(10);  // 最大値は未満なので注意（目的の数値 + 1）
  Console.WriteLine(number);

```

<br>

1~6の数値をランダムに出力します

```c#

  var random = new Random();      // クラスを実体化
  var number = random.Next(1,7);  // 最大値は未満なので注意（目的の数値 + 1）
  Console.WriteLine(number);

```

<br>

# **確認問題**

## **問題①**

下のプログラムを修正して  
50 ～ 99のランダムな数字を出力するプログラムを書こう。

```c#

  var random = new Random(); 
  var number = random.Next();
  Console.WriteLine(number);

```

## **問題②**

宝くじの当選金額を求めるプログラムを考えます。  
1等は1000000円（100万円）です。  
当選者の数はランダムに決まります。(1~50人)

出力結果になるようにプログラムを完成させよう。

```c#

  var price = 1000000;
  var random = new Random(); 
  var winner = random.Next();
  
```

```
 >>当選人数は⚪︎⚪︎です。
 >>当選金額は⚪︎⚪︎円です。
```

# **解答例**

## **問題①**

下のプログラムを修正して  
50 ～ 99のランダムな数字を出力するプログラムを書こう。

```c#

  var random = new Random(); 
  var number = random.Next(50,100);
  Console.WriteLine(number);

```

## **問題②**

宝くじの当選金額を求めるプログラムを考えます。  
1等は1000000円（100万円）です。  
当選者の数はランダムに決まります。(1~50人)
1人当たりの当選金額を求めましょう。

```c#

  var price = 1000000;
  var random = new Random(); 
  var winner = random.Next(50);
  Console.WriteLine($"当選人数は{winner}です");
  Console.WriteLine($"当選金額は{price / winner}円です");

```

```
 >>当選人数は⚪︎⚪︎です。
 >>当選金額は⚪︎⚪︎円です。
```