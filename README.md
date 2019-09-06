# vue-handson-stopwatch

Kamakura MokMok Hack #56 「Vue を使ってストップウォッチをつくるハンズオン」用のリポジトリです。

## 環境のセットアップ

- ⚠️ セットアップは基本 MacOS 向けです。
- ⚠️ すでに導入してるよって方はスキップしてください。

### HomeBrew のインストール

Terminal で `brew --version` を叩いて何もでてこなければ以下を叩いて [HomeBrew](https://brew.sh/index_ja) 入れましょう。

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### NodeBrew で Node を入れる

今回は NodeBrew を使って Node.js のバージョン管理（Node.js 自体のバージョン指定）を行います。
`nodebrew` と叩いて何もでなければ入れていきましょう。
※他のバージョン管理を使っても良いです。

```
brew install nodebrew
```

### Node.js のバージョンを合わせる

トラブルを避けるために今回は以下のバージョンを使います。

```
nodebrew install v10.15.3
```

入れたらバージョンを指定します。

```
nodebrew use v10.15.3
```

### Vue/React のセットアップ

#### yarn

`yarn -v` と入れて何もでなければ入れましょう。
これらは開発環境を作る上で必要です。

```
npm i -g yarn
```

#### Vue

`yarn -v&&vue --version` と入れて何もでなければ入れましょう。
これらは開発環境を作る上で必要です。

```
npm i -g @vue/cli
```

#### React

React は特に準備は不要です。

## プロジェクトの説明

リポジトリの構成については次の通りです。

```
react-vue-handson/
    ├ vue-stopwatch/ … Vueのプロジェクト
        ├ src/ … ソースコード
            ├ components … コンポーネント群
            ├ vuex … 状態管理関連
    ├ react-stopwatch/ … Reactのプロジェクト
        ├ src/ … ソースコード
            ├ components … コンポーネント群
            ├ redux … 状態管理関連
```

### プロジェクトを作る

今回はすでにプロジェクトの基本セットは入れています。コンポーネントや状態管理の実装のハンズオンを行いたいので、プロジェクトを作成する方法を知りたい方は以下をお試しください。

## おまけ

#### Vue + TypeScript

Vue（TypeScript + Class Component）のプロジェクトを作る時は以下を叩くと順を追ってできます。

```
vue create vue-ts-example {プロジェクト名}
```

TypeScript + Class Component での記述をオンにする場合は以下の流れで行うと良いです（今回はテストを書くところまではできないのでテスト周りは外しています）。
選択肢にチェックを入れたい時は `space` キーを押しましょう。

TypeScript を使いたくないという方は `Check the features needed for project` の時に TypeScript にチェックをいれない様にします。

#### React + TypeScript

React は TypeScript と相性良いので使っていきましょう。ていうか個人的に使ってくれーーという気持ちです 😇

```
npx create-react-app react-stopwatch --typescript
```
