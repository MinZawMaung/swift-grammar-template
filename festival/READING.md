# 読解ノート：自分のアプリのコード3箇所

> **氏名：** （ミンズォーマウン）
> **AI利用レベル：** 1（質問のみ。説明は自分の言葉で書く）
> **最終更新：** 2026-10-17

生成AIに書いてもらったコードでも、自分で書いたコードでもかまいません。自分のアプリの中から3箇所を選んで、次の3つの問いに答えてください。分からないところは、生成AIに「この行は何をしていますか」「この行を消すとどうなりますか」と聞いてかまいません。ただし、書くのは自分の言葉です。

> 💡 担任の先生の指示で、項目が増えることがあります。

---

## 箇所1：（例：品名を追加するボタンの処理）

override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
    let touch = touches.first!
    let location = touch.location(in: self)
    if location.x < self.frame.midX {
        if let car = self.playerCar {
            if car.position.x > 30 {
                car.position.x -= 50
            }
        }
    } else {
        if let car = self.playerCar {
            if car.position.x < self.frame.size.width - 30 {
                car.position.x += 50
            }
        }
    }
}

**何をしているか：**
箇所1：touchesBegan(_:with:)

コード

override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
    let touch = touches.first!
    let location = touch.location(in: self)
    if location.x < self.frame.midX {
        if let car = self.playerCar {
            if car.position.x > 30 {
                car.position.x -= 50
            }
        }
    } else {
        if let car = self.playerCar {
            if car.position.x < self.frame.size.width - 30 {
                car.position.x += 50
            }
        }
    }
}

何をしているか

画面をタップした場所によって、車を左または右に移動させます。



**なぜこう書くのか：**

画面の中央を基準にして、左側をタップしたか、右側をタップしたかを判断するためです。

**もしこう書かなかったら：**

タップした場所によって左右の動きを分けられなくなります。また、車の位置を確認しないと、画面の端を越えてしまう可能性があります。
---

## 箇所2：（見出し）

```swift
// コードを貼る
```

**何をしているか：**

**なぜこう書くのか：**

**もしこう書かなかったら：**

---

## 箇所3：（見出し）

```swift
// コードを貼る
```

**何をしているか：**

**なぜこう書くのか：**

**もしこう書かなかったら：**

---

## 自分ではまだ説明できない箇所（正直に）

（アプリの中で「動いているけれど何をしているか分からない」ところを書く。ここに書いたものは、後期の文法の授業で分かるようになります。）
