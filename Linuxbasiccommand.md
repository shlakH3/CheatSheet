## 連番生成
~~~
seq 1 10 >> "Filename"
~~~
![image](https://github.com/user-attachments/assets/1696c6bd-13bb-4db7-9340-374e582b5417)

## 必ずCommand2を実行
~~~
"Command1";"Command2"
~~~
![image](https://github.com/user-attachments/assets/999ed1bb-59c6-4c22-a33c-a4c1d0fdf086)

## Command1をFilenameに書き込み、標準出力
~~~
"Command1" | tee "Filename"
~~~
![image](https://github.com/user-attachments/assets/bdc7b27e-3b85-4498-9fd6-717f21bdf050)

## 先頭から〇行数分表示
~~~
head -n "num" "Filename"
~~~
![image](https://github.com/user-attachments/assets/9e1b7c30-0d41-4fce-9ee3-6d50dec6fab1)

## 末尾から〇行数分表示
~~~
tail -n "num" "Filename"
~~~
![image](https://github.com/user-attachments/assets/f78d6a91-8f71-4ae5-b93e-e45f4786a775)

リアルタイムで最終行を更新
~~~
tail -f "Filename"
~~~
## 先頭から〇文字目を表示
~~~
cut -c "num" "Filename"
~~~
![image](https://github.com/user-attachments/assets/842d4543-d4a5-4850-aa25-9ada4a229ceb)

![image](https://github.com/user-attachments/assets/8f9b220c-1934-4154-9988-9ec566198711)

## 指定したフィールド数の情報を表示
~~~
cut -d"delimiter" -f "field num" "Filename"
~~~
![image](https://github.com/user-attachments/assets/46c47a46-af9e-48a4-a168-a55323732005)

![image](https://github.com/user-attachments/assets/e382409b-b827-447a-b6fb-2ca1cfea46a3)
~~~
cut -d"delimiter" -f "field num" "Filename" | head or tail -n "num"
~~~

![image](https://github.com/user-attachments/assets/08c01602-0285-4916-9278-d0404b7ffba2)

## 文字列の連結
~~~
paste -d"demiliter" "Filename1" "Filename2" > "Newfilename"
~~~
![image](https://github.com/user-attachments/assets/2e04661d-e3af-4c0b-98d8-c0f2df0e63e4)

## 文字の変換や削除
~~~
tr -d "string" < "Filename"
~~~
![image](https://github.com/user-attachments/assets/859684d4-4f00-40cc-8770-f773f654b0dd)

![image](https://github.com/user-attachments/assets/ab74c1bb-bcc4-4bb2-aa26-31aed1eb7118)

## クラスを使った文字列削除
~~~
"Filename" | tr -d [:digit:] or [:alpha:]
~~~
![image](https://github.com/user-attachments/assets/d720c3e7-2daf-4ea8-91c3-03a561794c2f)
![image](https://github.com/user-attachments/assets/040fc4bd-30bc-46e4-bd43-7fd72c8bdf32)

## 文字置換
~~~
"Filename" | tr 'a-z' 'A-Z'
~~~
![image](https://github.com/user-attachments/assets/34a97c4c-3764-437c-88d9-e536264d92a5)

## 指定した行数でファイル分割
※拡張子にaa,ab,acとつくので、ファイル名の拡張子は「.」まで記載
~~~
split -"num" "Splitedfilename" "Newfilename"
~~~
![image](https://github.com/user-attachments/assets/460214d0-23f7-4377-b5de-d2c26c4e0414)

## 並び替え
~~~
sort "Filename"
~~~
![image](https://github.com/user-attachments/assets/2f1e250b-4563-4b1a-8081-e8bc9d5fd688)

![image](https://github.com/user-attachments/assets/88553144-c605-47c6-9886-d90831aef594)

※文字列として認識するので、数値として認識させる場合は、-nオプション
~~~
sort -n "Filename"
~~~
![image](https://github.com/user-attachments/assets/6e71765f-bc7f-4054-aae1-c338ad5c2c2c)

## 降順
~~~
sort -r "Filename"
~~~
![image](https://github.com/user-attachments/assets/d93c7735-c6d7-4df5-8ad4-7d3894380cac)

## 重複表示または非表示
※catやnlでは使えず、sortと組み合わせる
~~~
sort "Filenamme" | uniq -d
~~~
![image](https://github.com/user-attachments/assets/90ad8621-f268-428c-8ed0-aa54a45b28c0)

![image](https://github.com/user-attachments/assets/5d797083-e91e-4873-aa72-ccbab907aaef)
# 正規表現
![image](https://github.com/user-attachments/assets/166e4ca9-e129-4e65-a5d9-73d431c37660)

## 行頭指定
![image](https://github.com/user-attachments/assets/b03da9eb-78ba-4fbb-a13c-a2ba3f311449)

## 行末指定
![image](https://github.com/user-attachments/assets/a6abbef4-3175-4a39-bea5-c614e010c191)

