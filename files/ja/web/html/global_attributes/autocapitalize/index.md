---
title: autocapitalize
slug: Web/HTML/Global_attributes/autocapitalize
tags:
  - Autocapitalize
  - HTML
  - Reference
  - ウェブ
  - グローバル属性
translation_of: Web/HTML/Global_attributes/autocapitalize
---
{{HTMLSidebar("Global_attributes")}}

**`autocapitalize`** [グローバル属性](/ja/docs/Web/HTML/Global_attributes)は列挙型の属性で、ユーザーによって入力／編集されたとき、入力文字列の先頭大文字化が自動的に行われるかどうか、どのように行われるかを制御します。以下の値を指定することができます。

- `off` または `none`: 自動的な大文字化は適用されません (すべての文字は既定で小文字です)。
- `on` または `sentences`: 各文の最初の文字を既定で大文字にします。それ以外の文字は既定で小文字です。
- `words`: 各語の最初の文字を既定で大文字にします。それ以外の文字は既定で小文字です。
- `characters`: すべての文字は既定で大文字になります。

`autocapitalize` 属性は、物理キーボードからの入力時の挙動には影響しません。モバイル端末の仮想キーボードや音声入力など、他の入力方式の挙動に影響します。その様な方式では、文の最初の文字を自動的に大文字化することでユーザーを補助することがよくあります。 `autocapitalize` 属性は要素単位の挙動を上書きすることができます。

`autocapitalize` 属性では、 {{HTMLElement("input")}} 要素の {{htmlattrxref("type", "input")}} の値が `url`, `email`, `password` の場合は自動大文字化が有効になりません。

## 仕様書

| 仕様書                                                                                                           | 状態                             | 備考 |
| ---------------------------------------------------------------------------------------------------------------- | -------------------------------- | ---- |
| {{SpecName('HTML WHATWG', "interaction.html#autocapitalization", "autocapitalize")}} | {{Spec2('HTML WHATWG')}} |      |

## ブラウザーの対応

{{Compat("html.global_attributes.autocapitalize")}}