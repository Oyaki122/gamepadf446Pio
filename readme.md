# F303_HAL_Template
## About
STM32F446REをPlatformIOかつHALで開発するときのテンプレート．

## 環境構築
[stm32pio](https://github.com/ussserrr/stm32pio)と[STM32CubeMX](https://www.st.com/ja/development-tools/stm32cubemx.html)を使う．  
stm32pioは
```shell
pip install stm32pio
```
でインストールできる．  
[VsCode Action Buttons](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons)があると便利になる．

## 使い方
1. Use This Template を押して新しいリポジトリを作る
1. clone してくる
1. VSCode で開く
1. 普通の PlatformIO プロジェクトとして使う

### 設定の変更と反映
フォルダ内の`pinmap.ioc`をCubeMXで開き，設定を変更する．  
ターミナルで`stm32pio generate`を実行して，変更を反映したコードを生成する．

## Action Buttons
[VsCode Action Buttons](https://marketplace.visualstudio.com/items?itemName=seunlanlege.action-buttons)をインストールすると，ステータスバーにCubeMXボタンとGenerateボタンが表示されるようになる．
![image](https://user-images.githubusercontent.com/58695125/217482481-0474e798-93a2-4ee7-9be5-960f80dc6d0a.png)  
CubeMXを押すとCubeMXが起動し，各種設定を変更できる．Generateを押すと変更を反映したコードが生成される．

### WindowsでCubeMXが開かない
`$PROJECT_DIR/.vscode/settings.json`の`"open pinmap.ioc"`を`"Invoke-Item pinmap.ioc"`に書き換えてください．
