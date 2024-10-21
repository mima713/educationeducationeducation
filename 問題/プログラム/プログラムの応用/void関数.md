# void関数

## void関数とは
`void`関数は、戻り値を持たない関数です。つまり、関数が処理を終えた後に何も返さない場合に使用されます。`void`関数は、主に副作用を持つ操作（例えば、画面への出力や変数の値の変更）を行うために使用されます。

### 例の説明
以下に、`void`関数の例を示します。

1. **ヘッダファイルのインクルード**:
    ```cpp
    #include <stdio.h>
    ```
    `stdio.h` は標準入出力ライブラリで、`printf` 関数を使用するために必要です。

2. **void関数 `printMessage` の定義**:
    ```cpp
    void printMessage() {
        printf("Hello, World!\n");
    }
    ```
    - `void printMessage()` は、引数を取らず、何も返さない関数です。
    - `printf("Hello, World!\n");` は、"Hello, World!" というメッセージを画面に出力します。

3. **`main` 関数**:
    ```cpp
    int main() {
        printMessage();
        return 0;
    }
    ```
    - `printMessage();` は、`printMessage` 関数を呼び出します。
    - `return 0;` は、プログラムの正常終了を示します。

この例では、`printMessage` 関数を使用して "Hello, World!" というメッセージを画面に出力しています。`void`関数を使うことで、特定のタスクを実行するコードを整理し、再利用することができます。

## 課題

### 課題1: メッセージを出力する
新しい`void`関数 `printCustomMessage` を作成し、引数として文字列を受け取り、その文字列を画面に出力するようにしてください。`main` 関数で `printCustomMessage` 関数を呼び出し、任意のメッセージを出力するプログラムを書いてください。

### 課題2: 数値を出力する
新しい`void`関数 `printNumber` を作成し、引数として整数を受け取り、その整数を画面に出力するようにしてください。`main` 関数で `printNumber` 関数を呼び出し、任意の整数を出力するプログラムを書いてください。