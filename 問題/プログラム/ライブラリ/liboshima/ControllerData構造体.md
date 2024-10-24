# ControllerData構造体

## 概要
`ControllerData`構造体は、コントローラの構造体定義を提供します。この構造体は、モーター用のボタン、その他のボタン、スティックの状態を管理します。`IM920SL`構造体で送受信することができます。

## 使用方法

### インクルード
まず、`ControllerData`構造体を使用するために必要なヘッダファイルをインクルードします。

```cpp
#include <liboshima.h>
```

### インスタンスの作成
次に、`ControllerData`構造体のインスタンスを作成します。テンプレートパラメータにモーター、ボタン、スティックの数を渡します。

```cpp
ControllerData<2, 4, 2> controllerData; // 例: 2つのモーター、4つのボタン、2つのスティック
```

### メンバーのアクセス
作成したインスタンスを使用して、各メンバーにアクセスします。

```cpp
// モーターのボタン状態にアクセス
controllerData.motorButtons[0] = ...; // MotorButtonState::FORWARD, MotorButtonState::REVERSE, MotorButtonState::STOPのいずれかを指定

// その他のボタン状態にアクセス
controllerData.otherButtons[0] = ...; // AnotherButtonState::PRESSED, AnotherButtonState::RELEASEDのいずれかを指定

// スティックの状態にアクセス
controllerData.sticks[0].x = ...; // 0から255の範囲で指定
controllerData.sticks[0].y = ...; // 0から255の範囲で指定
```

## 課題

### 課題1: モーターのボタン状態の設定
`ControllerData`構造体を使用して、2つのモーターのボタン状態を設定するプログラムを書いてください。
結果は`Serial.print()`関数を使用して、シリアルモニタに出力してください。

### 課題2: スティックの状態の設定
`ControllerData`構造体を使用して、2つのスティックの状態を設定するプログラムを書いてください。
結果は`Serial.print()`関数を使用して、シリアルモニタに出力してください。