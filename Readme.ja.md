IntelliJ uroboroSQL Formatter
=============================

uroboroSQL Formatterは、エンタープライズシステムで用いられることの多い、  
非常に長いSQL(1K step以上)でも見やすく保守性の高いスタイルへフォーマットするための  
IntelliJ IDEAのプラグインです。

特に日本など、英語を母国語としない国では、SELECT句などにコメントを入れることがあります。  
その場合、AS句とコメントの縦位置を揃えて、もはや芸術的とも言える見やすさを追求しますが、  
これ自動的に実現するために開発したものです。

#### 一般的なフォーマッタの場合

```sql
SELECT MI.MAKER_CD AS ITEM_MAKER_CD -- メーカーコード
,
       MI.BRAND_CD AS ITEM_BRAND_CD -- ブランドコード
,
       MI.ITEM_CD AS ITEM_CD -- 商品コード
,
       MI.CATEGORY AS ITEM_CATEGORY -- 商品カテゴリ
FROM M_ITEM MI -- 商品マスタ

WHERE 1 = 1
  AND MI.ARRIVAL_DATE = '2016-12-01' -- 入荷日
```

#### uroboroSQL Formatterの場合

```sql
SELECT
    MI.MAKER_CD AS  ITEM_MAKER_CD   -- メーカーコード
,   MI.BRAND_CD AS  ITEM_BRAND_CD   -- ブランドコード
,   MI.ITEM_CD  AS  ITEM_CD         -- 商品コード
,   MI.CATEGORY AS  ITEM_CATEGORY   -- 商品カテゴリ
FROM
    M_ITEM  MI  -- 商品マスタ
WHERE
    1               =   1
AND MI.ARRIVAL_DATE =   '2016-12-01'    -- 入荷日

```

Features
--------

-	SELECT句、WHERE句内でASや演算子の縦位置を揃えてフォーマット
-	各行の末尾にコメントがあっても正しくフォーマット

How to Use
----------

-	Codeメニューから「Format SQL」を選択
-	Alt + Shift + L on Windows, Cmd + Ctrl + L on OS X

License
-------

[python-sqlparse library](https://github.com/andialbrecht/sqlparse) and this code are both on [2-clauses BSD](http://www.opensource.org/licenses/bsd-license.php)

---

Copyright 2017 by Future Architect.
