# icaveri
## Launcher software  for iverilog4win.
---
概要：Widows上で、IcarusVerilogでRTLシミュレーションするためのランチャーソフトです。
コマンドプロンプトを使わないで、シミュレーションの実行、結果の確認、編集、のサイクルを手軽に廻すことを目的としています。

[ 必要となる外部ソフトウェア ]
- Icarus Verilog for Windows.（シミュレーションエンジン本体）
- GTKWave for windows （Icarus Verilogに同梱されている）
- VisualStudio Code または Sakura-Editor（エディタとして使用を推奨）

[ 実行環境の構築手順 ]
- IcarusVerilog+GTKWave for Windowsの入手＆インストール  
  本家ページには無いので、http://bleyer.org/icarus/ からダウンロードすることになる  
  ※64bit/32bitの２種類があるはず  
  ※インストールの際のパス名に、半角スペースが入らない様に注意すること
  （つまり、「Program Files」や「Icarus Verilog」はダメです。オススメは、C:\APP\iverilog とか）
- VisualStudio Code または Sakura-Editor の入手＆インストール  
  お好きな方を。詳細手順は検索ででてくると思うので割愛  
  ※VS Codeの拡張機能（Verilog用）は外観的に入れておくほうがいいでしょう 
- シミュレーション対象を置くフォルダ構成を考えて、作成準備  
  （例えば、C:\APP\iverilog\work\themeA とか）
- 本ランチャーソフトのファイルを配置  
  icaveri/icaveri.exe , icaveri/icaveri_cfg.txt の２ファイルを、適当なフォルダに配置する（iverilogの近傍がいいでしょうね）  
  icaveri.exe のショートカットを作るとか、スタートメニューに登録するとか．．．
- icaveri_cfg.txt をフォルダ構成に合わせて変更  
  （最低限、IV,EE だけでも、正しい設定にしてください）  
  （VS Code の人は、EEは変更不要のはず）

[ はじめての実行 ]
- icaveri.exe を起動  








