﻿# OtherProcessDockedSample
別のアプリケーションをドッキングするサンプル  
（※マルチスレッド周りの処理はかなり怪しいです）  

## Note
### ドッキングが上手くいかないもの
- UWPアプリ(電卓とか)
- Chrome等のマルチプロセスアプリケーション

### WS_CHILDメモ
ドッキングするアプリにWS_CHILDをつけないとデバッグ強制終了(Shift+F5)時にゾンビプロセス化するのでドッキングしないようにしています  
以前試したときはWS_CHILDつけないとメニューが動かないとかあったんですが、今試したらWS_CHILDつけるとそもそもメニューが表示されないものがある様子  
notepadとか。ただ、以前もnotepadで試した気がするんですが…  
むしろnotepadはWS_CHILDつけない方が上手くいくようになっている気がします  

## References
- ウィンドウスタイル  
https://docs.microsoft.com/ja-jp/windows/win32/winmsg/window-styles  
- 電卓(UWP)がドッキングできない理由と対処方法  
https://teratail.com/questions/173588  
https://taktak.jp/2017/04/03/1970  
- Chromeがドッキングできない理由  
https://stackoverflow.com/questions/22314315/setwindowpos-not-working-for-browsers-no-mainwindowhandle?rq=1  
