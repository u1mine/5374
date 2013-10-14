
5374をカスタマイズする場合、
基本的にはdataフォルダの中を変更していただけれな、データが変更できます。

generateフォルダは
特に金沢のゴミの解析用のプログラムなので、使用しません。

unusedは将来的には使用するかもしれないプログラムなどが入っております。
具体的には、位置情報をもとに自分のエリアを自動的に設定するプログラムを作っておりましたが、諸事情により、現時点では使用されておりません。		


# data/area_days.csvの仕様

各エリアのゴミを出す曜日を記述します。
特に金沢の場合、１月にセンターが休止期間があり、
その期間１週間ずらすという仕様のため、センターの名称を記述します。

data/center.csvと対応した、名称を記述します。

特にそのような仕様がない場合は、センターの列は、空文字でも大丈夫です。
 
# data/center.csvの仕様

上記の理由で、センターの休止期間を記述します。

# data/description.csvの仕様

各ゴミのカテゴリを記述します。

## label

ゴミのカテゴリを記述します。

## sublabel

使用されておりません。

## description

使用されておりません。

## styles 

カテゴリの表示となる。イメージ画像を指定します。（デフォルトはsvgとなっております。）	

# data/target.csvの仕様

あるゴミが、どのゴミの日に捨てられるかのリストを表す。
画面表示上では、各ゴミをタップした時のアコーディオンをタップした時の	
表示されるものである。

## データの中身
'type','name' ,'notice','furigana'
の列のデータがあります。（一行目）


### type
typeの値としてはそれぞれ
「燃えるゴミ」、「燃えないゴミ」、「びんゴミ」、「資源ゴミ」のいずれかである。
	
これをもとに、紐付けを行う。

### name

ゴミの名前です。

### notice

このゴミを捨てるときの注意事項を記述します。

### furigana

リストで表示する際のラベルとしてのふりがなを指定します。
