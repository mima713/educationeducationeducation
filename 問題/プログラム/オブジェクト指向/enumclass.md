# 列挙型クラス（Enum Class）

## 概要
列挙型クラス（Enum Class）は、C++11で導入された機能で、従来の列挙型（enum）に比べて型安全性が向上しています。列挙型クラスを使用することで、名前空間の汚染を防ぎ、型の安全性を確保することができます。

## 列挙型クラスの定義方法
列挙型クラスは、`enum class` キーワードを使用して定義します。以下に基本的な構文を示します。

```cpp
enum class EnumName {
    Enumerator1,
    Enumerator2,
    Enumerator3
};
```

## 例

### 基本的な列挙型クラス
以下は、基本的な列挙型クラスの例です。

```cpp
#include <stdio.h>

enum class Color {
    Red,
    Green,
    Blue
};

int main() {
    Color myColor = Color::Green;

    if (myColor == Color::Green) {
        printf("The color is Green.\n");
    } else {
        printf("The color is not Green.\n");
    }

    return 0;
}
```

### 列挙型クラスのスコープ
列挙型クラスの列挙子は、列挙型クラスのスコープ内に限定されます。これにより、名前の衝突を防ぐことができます。

```cpp
#include <stdio.h>

enum class TrafficLight {
    Red,
    Yellow,
    Green
};

enum class Color {
    Red,
    Green,
    Blue
};

int main() {
    TrafficLight light = TrafficLight::Red;
    Color color = Color::Red;

    if (light == TrafficLight::Red) {
        printf("The traffic light is Red.\n");
    }

    if (color == Color::Red) {
        printf("The color is Red.\n");
    }

    return 0;
}
```

### 列挙型クラスの整数値への変換
列挙型クラスの列挙子を整数値に変換するには、`static_cast` を使用します。

```cpp
#include <stdio.h>

enum class Color {
    Red,
    Green,
    Blue
};

int main() {
    Color myColor = Color::Blue;
    int colorValue = static_cast<int>(myColor);

    printf("The integer value of Color::Blue is %d.\n", colorValue);

    return 0;
}
```

## 課題

### 問題1: 列挙型クラスの定義
以下の要件を満たす列挙型クラス `Season` を定義してください。
- 列挙子: `Spring`, `Summer`, `Autumn`, `Winter`

### 問題2: 列挙型クラスの使用
以下の要件を満たすプログラムを作成してください。
- 列挙型クラス `Season` を使用
- 変数 `currentSeason` を `Season::Summer` に設定
- `currentSeason` が `Season::Summer` であるかどうかをチェックし、結果を `printf` で出力

### 問題3: 列挙型クラスの整数値への変換
以下の要件を満たすプログラムを作成してください。
- 列挙型クラス `Season` を使用
- 変数 `currentSeason` を `Season::Winter` に設定
- `currentSeason` を整数値に変換し、その値を `printf` で出力

## まとめ
列挙型クラスを使用することで、型安全性が向上し、名前空間の汚染を防ぐことができます。列挙型クラスの列挙子はスコープ内に限定されるため、名前の衝突を防ぐことができます。また、`static_cast` を使用して列挙型クラスの列挙子を整数値に変換することも可能です。