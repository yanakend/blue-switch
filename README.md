# Blue Switch (fork)

> Fork of [HoshimuraYuto/blue-switch](https://github.com/HoshimuraYuto/blue-switch)  
> This is a personal fork with additional features. See changes below.

---

<details>
<summary>🇯🇵 日本語</summary>

macOS のメニューバーから Magic Keyboard / Trackpad / Mouse を複数の Mac 間でワンクリック切り替えするアプリ。

### オリジナルからの変更点

**メニュー操作の改善**
- 左クリック・右クリックどちらでもメニューを表示するよう統一
- メニューに自機（This Mac）と登録済みデバイスの一覧を表示
- デバイス名をクリックするだけで切り替え可能に（オリジナルは左クリックで1台目とトグルするのみ）

**複数台対応**
- 3台以上のMacを登録した場合、切り替え時に対象外の全デバイスへ `unregisterAll` を送信
- どのMacがキーボードを持っているかに関わらず正しく切り替わる

**アクティブ表示**
- 現在キーボードを持っているデバイスにチェックマーク（✓）を表示
- 切り替え操作と `connectAll` / `unregisterAll` の受信時に両Mac間で同期

### ビルド方法

```bash
git clone https://github.com/yanakend/blue-switch.git
cd blue-switch
open "Blue Switch.xcodeproj"
```

Xcode でスキーム `Blue Switch` を選択して Run、または Release ビルド後に `/Applications` にコピー。

### ライセンス

GPL-3.0（オリジナルと同じ）。詳細は [LICENSE](LICENSE) を参照。

</details>

---

<details open>
<summary>🇺🇸 English</summary>

A macOS menu bar app to switch Magic Keyboard / Trackpad / Mouse between multiple Macs with a single click.

### Changes from original

**Menu improvements**
- Both left and right clicks now open the menu
- Menu shows "This Mac" and all registered devices
- Click a device name to switch (original only toggled to the first device on left click)

**Multi-device support**
- When 3+ Macs are registered, sends `unregisterAll` to all non-target devices on switch
- Correctly switches regardless of which Mac currently holds the keyboard

**Active device indicator**
- Checkmark (✓) shows which device currently has the keyboard
- State is synced between Macs on `connectAll` / `unregisterAll` commands

### Build

```bash
git clone https://github.com/yanakend/blue-switch.git
cd blue-switch
open "Blue Switch.xcodeproj"
```

Select the `Blue Switch` scheme in Xcode and Run, or copy the Release build to `/Applications`.

### License

GPL-3.0 — same as the original. See [LICENSE](LICENSE).

</details>
