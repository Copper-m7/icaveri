# icaveri
## Launcher software  for iverilog4win.
---
概要：Widows上で、IcarusVerilogでRTLシミュレーションするためのランチャーソフトです。
コマンドプロンプトを使わないで、シミュレーションの実行、結果の確認、編集、のサイクルを手軽に廻すことを目的としています。（PATH編集、ubuntuやCygwinなどは不要）

[ 動作に必要となる外部ソフトウェア ]
- Icarus Verilog for Windows.（シミュレーションエンジン本体）
- GTKWave for windows （Icarus Verilogに同梱されている）
- VisualStudio Code または Sakura-Editor（エディタとして使用を推奨）

[ 実行環境の構築手順 ]
- IcarusVerilog+GTKWave for Windowsの入手＆インストール  
  本家ページには無いので、http://bleyer.org/icarus/ からダウンロードすることになる  
  ※64bit/32bit(x86)の２種類があるはず  
  ※インストールの際のパス名に、半角スペースが入らない様に注意すること
  （つまり、「Program Files」や「Icarus Verilog」はダメです。オススメは、C:\APP\iverilog とか）
- VisualStudio Code または Sakura-Editor の入手＆インストール  
  お好きな方を。詳細手順は検索ででてくると思うので割愛  
  ※VS Codeの拡張機能（VerilogHDLなど）は外観や編集補助として推奨  
  ※Sakuraも強調文字ライブラリを設定した方がいいでしょう
- シミュレーション対象を置くフォルダ構成を考えて、作成準備  
  （例えば、C:\APP\iverilog\work\themeA とかが良い）
- 本ランチャーソフトのファイルを配置（コンパイル無しの場合）  
  icaveri_bin/icaveri.exe , icaveri_bin/icaveri_cfg.txt の２ファイルを、適当なフォルダに配置する（iverilogの近傍がいいでしょうね）  
  icaveri.exe のショートカットを作るとかは、適宜．．．
- icaveri_cfg.txt をフォルダ構成に合わせて変更  
  （最低限、IV,EE 行だけでも、正しい設定にしてください）  
  （VS Code の人は、EEは変更不要。のはず）

[ はじめての icaveri.exe 起動 ]  
- 設定に問題なければ、iverilog付属のサンプルlfsr16が選択でき、そのままシミュレーションが実行でき、simの後、波形ビューワが起動できるはずです。

[ 各種操作 ]
- ファイル名のボタンを押すと、エディタが起動します
- シミュレーションエラー行のダブルクリックに対応
- シミュレーションのプロセス中断ができます
- GTKWave中で、gtkwを保存更新（Ctrl+S）することで、表示波形設定を保存して、次回起動時に利用できます
- Verilogファイルのポート記述から、呼び出し記述の表示機能
- Verilogファイル内の、簡易grep機能（module限定機能）

[ source ]
- VisualStudio 2017 Express C# です  

[ License ]
- とりあえず、MITにしとこう
