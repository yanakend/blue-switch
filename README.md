# Blue Switch (fork)

> Fork of [HoshimuraYuto/blue-switch](https://github.com/HoshimuraYuto/blue-switch)

macOS のメニューバーから Magic Keyboard / Trackpad / Mouse を複数の Mac 間でワンクリック切り替えするアプリ。

## オリジナルからの変更点

### メニュー操作の改善
- 左クリック・右クリックどちらでもメニューを表示するよう統一
- メニューに自機（This Mac）と登録済みデバイスの一覧を表示
- デバイス名をクリックするだけでキーボード等を切り替え可能に（オリジナルは左クリックで1台目とトグルするのみ）

### 複数台対応
- 3台以上のMacを登録した場合、切り替え時に対象外の全デバイスへ `unregisterAll` を送信
- どのMacがキーボードを持っているかに関わらず正しく切り替わる

### アクティブ表示
- 現在キーボードを持っているデバイスにチェックマーク（✓）を表示
- 切り替え操作と `connectAll` / `unregisterAll` の受信時に両Mac間で同期

## ビルド方法

```bash
git clone https://github.com/yanakend/blue-switch.git
cd blue-switch
open "Blue Switch.xcodeproj"
```

Xcode でスキーム `Blue Switch` を選択して Run、または Release ビルド後に `/Applications` にコピー。

## ライセンス

GPL-3.0（オリジナルと同じ）。詳細は [LICENSE](LICENSE) を参照。
