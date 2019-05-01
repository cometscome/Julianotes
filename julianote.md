# 物理で使う数値計算入門：Julia言語による簡単数値計算
<div style="text-align: right;">
永井佑紀
</div>

## 1. はじめに：このノートの目的
初めて数値計算をする人がJuliaを使って簡単にコードを書いて計算できるように、という意図で書いています。特に、物理で使うことの多い計算を中心にまとめています。

## 2. Juliaのインストール
Juliaを使うには、二つの方法があります。
1. 対話的実行環境　REPL(read-eval-print loop)
2. 通常の実行方法

1は、普通のアプリケーションのようにJuliaを起動して、その中でコードを書いたり計算をしたりプロットしたりするものです。簡単な計算を気軽に試すことができます。

2は、通常の実行方法で、ファイルにプログラムコードを```test.jl```みたいな形で保存してから、

```
julia test.jl
```
で実行する方法です。

このノートでは、最初は簡単なので1.のREPLを使います。少し複雑になってきた場合には、ファイルにコードを保存して、2.で実行することにします。




### 2.1. バージョン
このノートでのJuliaのバージョンは、1.1.0とします。

### 2.2. Macの場合

https://julialang.org/downloads/
から```macOS 10.8+ Package (.dmg)```をダウンロードして、他のアプリケーションと同様にインストールします。インストールしたあとは、アプリケーションにJulia 1.1がありますので、それをダブルクリックするとターミナルが起動して使えるようになります。

### 2.3. Linuxの場合
Linuxの場合には、

```
wget https://julialang-s3.julialang.org/bin/linux/x64/1.1/julia-1.1.0-linux-x86_64.tar.gz
tar -xvf julia-1.1.0-linux-x86_64.tar.gz
echo 'export PATH="$PATH:$HOME/julia-1.1.0/bin"' >> ~/.bashrc
source ~/.bashrc
```
でインストールができますので、あとは

```
julia
```
で起動することができます。

### 2.4 Windowsの場合
Windows版のJuliaをインストールすれば使用できます。、あるいは、Windows Subsystem for Linuxを使ってUbuntuを入れることで上のLinuxと同じようにインストールすることもできます。




## 3. 基本的演算編


```julia
    function test(a::Int64)
        a = 3
        return a
    end

    test()
```