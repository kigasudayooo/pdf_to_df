# 春闘における一時金の支給状況PDFの加工
連合は春季に賃金交渉の結果を[公表](https://www.jtuc-rengo.or.jp/activity/roudou/shuntou/)している。
しかし公表形式はPDFとなっており、時系列での評価をするためには手間がかかる。
このため、今回は特に一時金の支給状況に限定して、pdfの表をpythonを用いて加工する。

流れとしてはwindowsであればwsl、その他であればコマンドプロンプト上で以下を動かせば環境構築できる。
```
git clone https://github.com/kigasudayooo/pdf_to_df.git
cd pdf_to_df
code .

```

