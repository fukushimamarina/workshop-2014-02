# 論理演算子

## 関係演算子
    && -> かつ
    || -> または

- `if文`で複雑な条件を扱いたいときは, `関係演算子`を用いて複数の条件を連結しましょう
    - `&&`演算子は｢かつ｣なので, 両方の条件が真となるときのみ真となります
    - `||`演算子は｢または｣なので, 条件のどちらか1つでも真となるならば真となります

## 関係演算子
    my $hoge = 64;
    if ( $hoge > 0 && $hoge % 2 == 0 ) {
        print "&&: OK\n";
    }
    if ( $hoge > 0 || $hoge % 2 == 1 ) {
        print "||: OK\n";
    }

- 2行目は, ｢64は0より大きい(真)｣かつ｢64を2で割った余りは0(真)｣なので, 真となります
- 5行目は, ｢64は0より大きい(真)｣または｢64を2で割った余りは1(偽)｣なので, 真となります

## 練習問題
    #!/usr/bin/env perl
    use strict;
    use warnings;
    my $answer = 1; # 好きな値を入力しておく

- 簡単な数当てゲーム `question_num.pl`を作成しよう
- 端末から数字を一つ入力し, その数字が`$answer`と一致したら`OK`, `$answer`より大きければ`too big`, 小さければ`too small`と表示します
    - オプション: 入力した値が, `$answer`から-5〜+5の範囲内(例えば, `$answer`が10なら, 5〜15)の場合, `near`と表示するようにしてみましょう

