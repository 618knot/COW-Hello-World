# COW-Hello-World
[COW](https://esolangs.org/wiki/COW)で"Hello,World!"したときのコード置き場

[実行環境](https://frank-buss.de/cow.html)

## 圧縮版
```
MoOMoOMoOMoOMoOMoOMoOMoOMMMmoOMMMmoOMoOMoOMOOmOoMOOMOomOoMoOmoOmoomOoMMMmoOMMMmoOMOomoomOoMMMmoOmoOMMMMoOMMMmoOmoOmoOmoOmoOmoOMMMMoOMoOMoOMoOMoOMoOMoOMoOMoOMoOMoOmOomOomOomOomOomOomOomOoMOOMOomOoMoOmoOmoomoOmoOMMMmOomOoMMMMOOMOomOoMoOmoOmoomOoMoOMoOMoOMMMmoOmoOmoOmoOMMMMMMmoOMMMMoOMoOMoOMoOMoOMoOMoOMoOMMMmoOMMMMMMMoOMoOMoOMoOMoOMoOmoOMMMMoOMoOMoOMMMmoOmoOmoOMMMMMMmoOMMMMOoMOoMOoMMMmoOMMMMMMmoOMMMMOoMOoMOoMOoMOoMOoMOomOomOomOomOomOomOomOoMMMmOomOomOomOomOoMMMmoOmoOMMMmOomOomOoMMMMOOMOomoOMOomOomoomoOMoOMoOMoOMoOMoOMoOMMMmoOmoOmoOmoOmoOmoOmoOMMMMMMmoOmoOmoOmoOmoOmoOMMMMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOoMOOMoomOomoo
```

## 改行・スペースあり版
```
MoO MoO MoO MoO MoO MoO MoO MoO MMM

moO MMM

moO MoO MoO

MOO mOo

MOO MOo mOo MoO moO moo

mOo MMM moO MMM

moO MOo

moo

mOo MMM moO moO MMM MoO MMM

moO moO moO moO moO moO MMM MoO MoO MoO MoO MoO MoO MoO MoO MoO MoO MoO

mOo mOo mOo mOo mOo mOo mOo mOo

MOO MOo mOo MoO moO moo

moO moO MMM mOo mOo MMM

MOO MOo mOo MoO moO moo

mOo MoO MoO MoO MMM

moO moO moO moO MMM MMM

moO MMM MoO MoO MoO MoO MoO MoO MoO MoO MMM

moO MMM MMM MoO MoO MoO MoO MoO MoO

moO MMM MoO MoO MoO MMM

moO moO moO MMM MMM

moO MMM MOo MOo MOo MMM

moO MMM MMM

moO MMM MOo MOo MOo MOo MOo MOo MOo

mOo mOo mOo mOo mOo mOo mOo MMM

mOo mOo mOo mOo mOo MMM

moO moO MMM

mOo mOo mOo MMM

MOO MOo moO MOo mOo moo

moO MoO MoO MoO MoO MoO MoO MMM

moO moO moO moO moO moO moO MMM MMM

moO moO moO moO moO moO MMM MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo

MOO Moo mOo moo
```

## コメントあり版
```
; 0番メモリに8数えてレジスタに保存
MoO MoO MoO MoO MoO MoO MoO MoO MMM

; 1番メモリに移動してレジスタの8をコピーし、レジスタをクリア
moO MMM

; 2番メモリに移動して2数える
moO MoO MoO

; 0 0 2

; ループA開始 2番メモリが0になると終了
MOO mOo

; ループB 1番メモリが0になるまで0番メモリの値をインクリメント
MOO MOo mOo MoO moO moo

; 0番メモリの値を1番メモリにコピー
mOo MMM moO MMM

; 3番メモリに移動して値をデクリメント
moO MOo

; ループA終端 3番メモリが0でなければループA開始地点に戻る 0ならループAおわり
moo

; 32 32 0

; 1番目メモリの値を3番メモリにコピーしその値を1増やすしてレジスタに保存
mOo MMM moO moO MMM MoO MMM

; 32 32 0 33(!)

; 33を9番メモリにコピーして11足す
moO moO moO moO moO moO MMM MoO MoO MoO MoO MoO MoO MoO MoO MoO MoO MoO

; 1番メモリに移動
mOo mOo mOo mOo mOo mOo mOo mOo

; ループC 1番メモリが0になるまで0番メモリの値をインクリメント = 32 + 32
MOO MOo mOo MoO moO moo

; 3番メモリを1番メモリにコピー
moO moO MMM mOo mOo MMM

; 64 33 0 33(!) 0 0 0 0 0 44(,)

; ループD 1番メモリが0になるまで0番メモリの値をインクリメント = 64 + 33
MOO MOo mOo MoO moO moo

; 0番メモリの値を3増やして値をレジスタに保存
mOo MoO MoO MoO MMM


; レジスタの値を4番メモリにコピー
moO moO moO moO MMM MMM

; 100 0 0 33(!) 100(d) 0 0 0 0 44(,)

; 5番メモリに100をコピーして8足してレジスタに保存
moO MMM MoO MoO MoO MoO MoO MoO MoO MoO MMM

; 100 0 0 33(!) 100(d) 108(l) 0 0 0 44(,)

; 6番メモリに108をコピーしてレジスタに保存しなおして、6番メモリに6足す
moO MMM MMM MoO MoO MoO MoO MoO MoO

; 100 0 0 33(!) 100(d) 108(l) 114(r) 0 0 44(,)
 
; 7番メモリに108をコピーして3足してレジスタに保存
moO MMM MoO MoO MoO MMM

; 100 0 0 33(!) 100(d) 108(l) 114(r) 111(o) 0 44(,)

; 10番メモリに111をコピーしてレジスタに保存しなおす
moO moO moO MMM MMM

; 100 0 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o)

; 11番メモリに111をコピーして3引いてレジスタに保存
moO MMM MOo MOo MOo MMM

; 100 0 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l)

; 12番メモリに108をコピーしてレジスタに保存しなおす
moO MMM MMM

; 100 0 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l) 108(l)

; 13番メモリに108をコピーして7引く
moO MMM MOo MOo MOo MOo MOo MOo MOo

; 100 0 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l) 108(l) 101(e)

; 6番メモリの値をレジスタに保存
mOo mOo mOo mOo mOo mOo mOo MMM

; 114を1番メモリにコピー
mOo mOo mOo mOo mOo MMM

; 100 114 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l) 108(l) 101(e)

; 3番メモリの値をレジスタに保存
moO moO MMM

; 33を0番メモリにコピー
mOo mOo mOo MMM

; ループE 0番メモリが0になるまで1番メモリの値をデクリメント = 114 - 33
MOO MOo moO MOo mOo moo

; 0 81 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l) 108(l) 101(e)

; 1番メモリの値に6足してレジスタに保存
moO MoO MoO MoO MoO MoO MoO MMM

; 0 87 0 33(!) 100(d) 108(l) 114(r) 111(o) 44(,) 0 111(o) 108(l) 108(l) 101(e)

; 87を8番メモリにコピーしてレジスタに保存しなおす
moO moO moO moO moO moO moO MMM MMM

; 0 87 0 33(!) 100(d) 108(l) 114(r) 111(o) 87(W) 44(,) 111(o) 108(l) 108(l) 101(e)

; 87を14番メモリにコピーして15引く
moO moO moO moO moO moO MMM MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo MOo

; 0 87 0 33(!) 100(d) 108(l) 114(r) 111(o) 87(W) 44(,) 111(o) 108(l) 108(l) 101(e) 72(H)

; ループF 14番メモリからASCII文字を表示してメモリ番号を1ずつデクリメント。メモリの値が0になったら(2番メモリまで行ったら)ループ終わり
MOO Moo mOo moo
```
