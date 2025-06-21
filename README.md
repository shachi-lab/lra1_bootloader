# LRA1 Bootloader

このリポジトリでは、LRA1 デバイス専用のブートローダーを提供しています。  
このブートローダーは、LRA1 のアップデートツールを使用してファームウェアを安全に書き込むために作成されています。  
ブートローダーに不具合が発生した場合の修復用として公開しています。

## ファイル名
- **lra1_bootloader_v100.bin**  
  LRA1専用のブートローダーのバイナリファイルです。

## 書き込み方法
- **J-LINK**、**ICD**、**PICkit**、**MPLAB Snap**、**Atme-ICE**、**OpenOCD** 等のツールを使用し、SWD経由でプログラムをフラッシュしてください。
- **MPU** :  Microchip ATSAMR35J17B
- **書き込み開始アドレス**: `0x000000`
- SWDインターフェースを使用して書き込みを行います。  
  具体的には、以下のピンに接続してください:
  - **SWCLK** : Pin 30 (PA30)
  - **SWDIO** : Pin 29 (PA31)
  - **nSRST** : Pin 33 (RESET) - 必要に応じて接続してください  
  
  ツールによっては、**SWCLK**, **SWDIO**, **nSRST** 信号に対してプルアップ抵抗が必要な場合があります。  
  また、書き込み時にはこれらの信号線に他のデバイス等が接続されないようにしてください。  

- 書き込みには、各ツール専用のアプリ等が必要となります。  
  操作方法については、それぞれの説明に従ってください。  

## 電源要件
- 電源電圧は **3.3V** を使用してください。  
  (SWDインターフェースの **VTref** への接続も必要です。）

## 注意事項
- このブートローダーは、ユーザーの利便性向上のために公開されています。  
  **使用は自己責任で行ってください。**

- このリポジトリに含まれるファイルおよび情報は、LRA1デバイスのファームウェアアップデートおよびブートローダー復旧に必要な情報を提供することを目的としています。  

- 適切な書き込みツールと回路構成で、安全かつ確実に書き込みを行ってください。

## 免責事項
- このブートローダーの書き込みよって生じたあらゆる不具合やデバイスの破損に関しては、著作権者ならびに製作者は一切の保証を行いませんので、あらかじめご了承ください。

## 著作権
 - Copyright (c) 2023-2025 Shachi-lab  
All rights reserved.

このソフトウェアはLRA1モジュール用に開発され、使用許諾契約に基づきi2-electronicsに提供されました。  
This software was originally developed for the LRA1 module, and provided to i2-electronics under a usage agreement.

## ライセンス
- このブートローダーは、**バイナリのみの提供**となります。  
- 再配布および使用は自由ですが、**改変や派生物の作成は固く禁止**されています。  
- ソースコードは公開されておらず、バイナリそのものの提供のみとなります。

---

## 📡 このプロジェクトについて

このリポジトリは、個人プロジェクト「[しゃちらぼ｜Shachi-lab](https://shachi-lab.com)」で進めている  
LoRaモジュール「LRA1」に関する開発・実験の一部です。

ブログでは、LRA1の使い方やTipsに加えて、  
AIアシスタント「ろらたん」が技術と遊び心を交えながら解説してくれます。

🎀「正式には“しゃちらぼ”だけど、“シャチラボ”でもいいよ〜♪」

## 📡 About this project (English)

This repository is part of a personal project from [Shachi-lab](https://shachi-lab.com),  
which focuses on the development and experimentation of the Japanese LoRa module “LRA1”.

The blog introduces how to use LRA1, practical tips, and fun insights —  
with the help of an AI assistant named *Roratan* who adds a friendly and playful touch.

🎀 “It's officially called ‘Shachi-lab’, but feel free to call it ‘Shachilab’ too!”

## 🔗 関連リンク

- 📘 [しゃちらぼ｜Shachi-lab 技術ブログ](https://blog.shachi-lab.com)
- 🛠 LRA1関連の記事一覧：https://blog.shachi-lab.com/tag/lra1
- 🐦 X（旧Twitter）： [@shachi_lab](https://x.com/shachi_lab)
- 🐙 GitHub：[@shachi-lab](https://github.com/shachi-lab)
- 📗 Qiita： [@shachi-lab](https://qiita.com/shachi-lab)
