# mecab-it-security-dictionary
IT security dictionary for MeCab

## Overview
情報セキュリティ用語を収録したMeCab用の辞書です。

## Getting started
システム辞書があるディレクトリを渡す必要があるのでそれを調べます。

```bash
$ mecab -D
filename:	/var/lib/mecab/dic/debian/sys.dic
version:	102
charset:	UTF-8
type:	0
size:	392126
left size:	1316
right size:	1316
```

ここでは「/var/lib/mecab/dic/debian/」ですね。

> $ /usr/lib/mecab/mecab-dict-index -d /var/lib/mecab/dic/debian -u mecab-it-security-dic.dic -f utf8 -t utf8 mecab-it-security-dic.csv 

これで、カレントディレクトリに「mecab-it-security-dic.dic」というファイルができます。/etc/mecabrcに以下を追加。

> userdic = /root/share/mecab-it-security-dic.dic
