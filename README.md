# estat_dl
codezine記事「ディープラーニングを用いた時系列データの予測モデル」にて使用したデータ、ソースコードです
## ソースコード
### chapter01.ipynb
第1稿「ディープラーニングを用いた時系列データの予測モデル」で使用したソースコードです
- 目的変数:mig_in(年次)
- 説明変数:*_lag1(前年の全データ,年次)
- ロジック:ディープラーニング(CNN)
## データ
### data
出典:政府統計の総合窓口(e-Stat) (https://www.e-stat.go.jp/)
各データファイル(CSV)は、「住民基本台帳人口移動報告」,「住民基本台帳に基づく人口、人口動態及び世帯数調査」,「賃金構造基本統計調査」,「工業統計調査」,「商用統計調査」を加工して作成
免責:利用者がコンテンツを用いて行う一切の行為(コンテンツを編集・加工等した情報を利用することを含む)について何ら責任を負うものではありません。
コンテンツは予告なく変更、移転、削除等が行われることがあります。
### 00000000_pre_id.csv
- prefecture:都道府県
- prefecture_id:都道府県ID
### 00200523_migration.csv
- datetime:日時
- prefecture:都道府県
- mig_in:県外からの転入者数
- mig_out:県外への転出者数
- mig_internal:県内移動者数
### 00200241_population.csv
- datetime:日時
- prefecture:都道府県
- pop_male:男性人口数
- pop_female:女性人口数
- pop_sum:合計人口数
- pop_households:世帯数
#### 00450091_wage.csv
- datetime:日時
- prefecture:都道府県
- wag_age:労働者の平均年齢
- wag_salary:労働者の平均月給
- wag_bonus:労働者の平均賞与
- wag_workers:労働者の人数
### 00550010_industrial.csv
- datetime:日時
- prefecture:都道府県
- idt_offices:工業事業所数
- idt_employees:工業従業員数
- idt_salaries:工業給与総額
- idt_costs:工業原材料総額
- idt_sales:工業出荷総額
### 00550020_retail.xlsx
- datetime:日時
- prefecture:都道府県
- ret_offices:卸小売事業所数
- ret_employees:卸小売従業員数
- ret_sales:卸小売商品販売額
## 動作確認環境
### OS
- macOS Mojave 10.14.6
### Python
- Python 3.7.2(anaconda3-5.3.1)
### Python Packages
- jupyter 1.0.0
- numpy 1.15.1
- pandas 0.23.4
- scikit-learn 0.19.2
- tensorflow 1.14.0
- Keras 2.2.4
- matplotlib 2.2.3

