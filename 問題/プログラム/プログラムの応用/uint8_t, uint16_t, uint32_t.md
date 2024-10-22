# uint8_t, uint16_t, uint32_t

## 概要
`uint8_t`, `uint16_t`, `uint32_t`は、C言語やC++で使用される固定サイズの整数型です。これらは、特定のビット数を持つ符号なし整数を表します。

## データ型の詳細
- `uint8_t`: 8ビットの符号なし整数。範囲は0から255。
- `uint16_t`: 16ビットの符号なし整数。範囲は0から65535。
- `uint32_t`: 32ビットの符号なし整数。範囲は0から4294967295。

## 使用例
以下に、各データ型の使用例を示します。

```c
#include <stdint.h>
#include <stdio.h>

int main() {
    uint8_t a = 255;
    uint16_t b = 65535;
    uint32_t c = 4294967295;

    printf("uint8_t a: %u\n", a);
    printf("uint16_t b: %u\n", b);
    printf("uint32_t c: %u\n", c);

    return 0;
}
```

このプログラムは、各データ型の最大値を表示します。

## 注意点
- これらのデータ型は、`<stdint.h>`ヘッダファイルで定義されています。
- 符号なし整数であるため、負の値を取ることはできません。
- オーバーフローに注意が必要です。例えば、`uint8_t`型の変数に256を代入すると、0に戻ります。

## 関連情報
- `int8_t`, `int16_t`, `int32_t`: 符号付きの固定サイズ整数型。
- `size_t`: メモリサイズを表すために使用される符号なし整数型。

これらのデータ型を使用することで、プログラムの移植性と可読性を向上させることができます。

## 課題

### 課題1: 最大値の表示
以下のプログラムを完成させて、`uint8_t`, `uint16_t`, `uint32_t`の最大値を表示してください。

```c
#include <stdint.h>
#include <stdio.h>

int main() {
    uint32_t c = // ここに記述
    uint8_t a = // ここに記述
    uint16_t b = // ここに記述

    printf("uint8_t a: %u\n", a);
    printf("uint16_t b: %u\n", b);
    printf("uint32_t c: %u\n", c);

    return 0;
}
```

### 課題2: オーバーフローの確認
以下のプログラムを完成させて、`uint8_t`型の変数に256を代入した場合の挙動を確認してください。

```c
#include <stdint.h>
#include <stdio.h>

int main() {
    uint8_t a = // ここに記述

    printf("uint8_t a: %u\n", a);

    return 0;
}
```