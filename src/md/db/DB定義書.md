# DB定義書
## ER図
[ER図はこちら]() 

# DBテーブルカラム詳細一覧

### 購入テーブル (d_purchase)
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|オーダーID|order_id|bigint(20)|○|○||
|顧客コード|customer_code|varchar(50)||○||
|購入日|purchase_date|date||○||
|総額|total_price|int(11)||○||

### 購入詳細テーブル (d_purchase_detail)
|和名|属性名(カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:----:|
|オーダー詳細ID|detail_id|bigint(20)|○|○||
|オーダーID|order_id|bigint(20)|○|○|○|
|商品コード|item_code|int(11)||○||
|価格|price|int(11)||○||
|数量|num|int(11)||○||

### 顧客マスタ (m_customers)
|和名|属性名(カラム)|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:---:|
|顧客コード|customer_code|varchar(50)|○|○||
|パスワード|pass|varchar(50)||○|○|
|氏名|name|varchar(20)||○||
|住所|address|varchar(100)||○||
|電話番号|tel|varchar(20)||○||
|メールアドレス|mail|varchar(100)||○||
|削除フラグ|del_flag|int(11)||||
|登録日|reg=date|date||○||

### カテゴリマスタ　(m_category)
|和名|属性名|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:---:|
|カテゴリID|category(20)||○||
|登録日|reg_date|date||○||

### 商品マスタ (m_items)
|和名|属性名 (カラム名)|型|PK|NN|FK|
|:---|:---|:---|:---|:---:|:---:|
|商品コード|item_code|int(11)|○|○||
|商品名|item_name|varchar(50)||○||
|価格|price|int(11)||○||
|カテゴリID|category_id|int(11)||○|○|
|画像ファイル名|image|vachar(200)||○||
|商品詳細説明|detail|varchar(500)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||○||
