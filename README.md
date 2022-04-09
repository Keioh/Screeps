#ScreepsでC/C++を使う
C++しかできん。

#必須
*[CPPREEPS](https://github.com/screepers/cppreeps)
*[emscripten](https://emscripten.org/docs/api_reference/bind.h.html)

CPPREEPSはScreepsAPIをC++で使える様にするheaderファイルとローダー。
emscriptenはC++をWebAssemblyとJavaScriptに変換する。

#手順
1.適当な空のプロジェクトにCPPREEPSのincludeフォルダを追加する。
2.CPPREEPSのsrcフォルダをコピーして空のプロジェクトに追加する。
3.loop.cppに処理を追加、記述をする。
4.loop.cppを「CPPREEPS」のcreate.batでWebAssemblyとJavaScriptに変換する。
5.変換したファイルをゲームに追加する。
6.他の詳細は各ソフトウェアの紹介ページを確認