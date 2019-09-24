# icaveri
## Launcher software  for 'icarus verilog for windows'.
---
概要：Windows上で、IcarusVerilogでRTLシミュレーションするためのランチャーソフトです。
コマンドプロンプトを使わないで、シミュレーションの実行、結果の確認、編集、のサイクルを手軽に廻すことを目的としています。（面倒なコマンド起動、PATH編集、ubuntuやCygwin環境などは不要、逆にLinux環境で本ソフトは使えません）  
![app_image](https://github.com/Copper-m7/www/blob/master/image/icaveri.png)  
[ 動作に必要となる外部ソフトウェア ]
- Icarus Verilog for Windows.（シミュレーションエンジン本体）
- GTKWave for windows （Icarus Verilogに同梱されている）
- VisualStudio Code または Sakura-Editor（エディタとして使用を推奨）

[ 実行環境の構築手順 ]
- IcarusVerilog+GTKWave for Windows の入手＆インストール  
  Win用は、本家ページには無いので、http://bleyer.org/icarus/ からダウンロードすることになる  
  ※64bit/32bit(x86)の２種類があるので、使用Winに合った方を。  
  2019年8月時点は、iverilog-v11-20190809-x64_setup.exe [17.0MB] が最新の様です。  
  ※インストールの際のパス名に、半角スペースが入らない様に注意すること
  （つまり、「Program Files」はダメ。オススメは、C:\APP\iverilog とか）
- VisualStudio Code または Sakura-Editor の入手＆インストール  
  お好きな方を。詳細手順は検索ででてくると思うので割愛  
  ※VisualStudio Codeの拡張機能（VerilogHDLなど）は外観や編集補助として推奨します。コンソールは利用しないんだけど。  
  ※Sakuraも強調文字ライブラリをVerilogで設定した方が、いいでしょう
- シミュレーション対象を置くフォルダ構成を決めて、フォルダなどを準備する
　（例えば、C:\APP\iverilog\work\themeA とかが良い。各自の準備したsim対象のRTL＆テストベンチとか．．．）
- 本ランチャーソフトのファイルを配置（コンパイル無しの場合）  
  githubから、icaveri_bin/icaveri.exe , icaveri_bin/icaveri_cfg.txt
  の２ファイルを、適当なフォルダに配置する（iverilogの近傍がいいでしょうね） 
  icaveri.exe のショートカットを作るとかは、適宜．．．
- icaveri_cfg.txt を各自のフォルダ構成に合わせて変更  
  （テキスト内のコメントを参照のこと。最低限、IV,EE 行だけでも、正しい設定にしてください。VisualStudio Code であれば、EEの記述は変更不要のはず。）

[ はじめての icaveri.exe 起動 ]  
- 既にテストベンチ付きのRTLを持っている場合は、icaveri_cfg.txt に追記してください。
- 設定に問題なければ、iverilog付属のサンプルlfsr16が選択できる。
　そのままiverilogボタン１つでシミュレーションが実行できる。
　simが動けば、波形ビューワが起動できるはずです。

[ 各種操作 ]
- ファイル名のボタンを押すと、エディタが起動します
- シミュレーションエラー行のダブルクリックに対応（エディタ起動）
- シミュレーションのプロセス中断ができます
- GTKWave起動には、gtkwファイルを使います。波形観測時に、gtkwを保存更新（Ctrl+S）することで、表示波形設定を保存して、次回起動時に利用できます
- GTKWaveはCtrl+Shift+Rのキー操作で、再sim後の波形データを読み直すことができるので、GTKWaveは終了せずに再Simできます
- Verilogファイルのポート記述から、呼び出し記述の表示機能
- 簡易grep機能（module限定機能、ダブルクリック対応）  

[ 開発環境 ]
- VisualStudio 2017 Express C# です。  

[ License ]
- とりあえず、MITにしとこう  
