# dict-mn

Энэхүү монгол хэлний толь нь [Hunspell](http://hunspell.github.io) үгийн алдаа шалгагчид тулгуурлан ажиллах бөгөөд 45 мянга орчим үндэс, тэдгээрийн 450 сая гаруй хувилал бүхий үгийн санг агуулсан.

Толийн онцлогийг дурдвал:

-   Академич Ц. Дамдинсүрэн нарын "Монгол үсгийн дүрмийн толь" бүтээлийг баримтлан бүтээсэн
-   Нөхцөлийн угсруулан холбох зарчимд тулгуурласан (Hunspell v1.3.3-аас хойших хувилбарт ажиллана)
-   Алдаатай үгийн зөв хувилбарыг оновчтой тодорхойлно
-   Morphological analysis
-   Stemming

# Hunspell ашиглах

Хэрэв таны ашиглаж буй программ Hunspell дэмждэггүй эсвэл та их хэмжээний өгөгдлийн бүх алдаатай үгсийг давхцалгүйгээр жагсаалт болгон харахыг хүсвэл Hunspell программыг дараах байдлаар ашиглахыг зөвлөж байна.

Юун түрүүнд [Hunspell](https://github.com/hunspell/hunspell) алдаа шалгагчаа суулгасан байх хэрэгтэй. Хэрхэн суулгах мэдээллийг [https://github.com/hunspell/hunspell](https://github.com/hunspell/hunspell) хаягаас мөн авах боломжтой.

## Hunspell суулгах

Linux үйлдлийн систем дээр суулгах бол

```
sudo apt install hunspell
```

Mac үйлдлийн систем дээр суулгах бол

```
brew install hunspell
```

Windows үйлдлийн систем дээр суулгах бол [Chocolatey](https://chocolatey.org) ашиглаж болно

```
choco install hunspell.portable
```

Ийнхүү суулгасан бол толь (`mn_MN.aff`, `mn_MN.dic`) байрлаж буй замыг дараах байдлаар оруулж өгнө

```
hunspell -d <your-location>/mn_MN,en_US -l input.txt | sort | uniq > output.txt
```

Дээрх жишээнд монгол, англи толиудыг зэрэг ашигласан байна. Ихэнх программуудад олон толийг нэгэн зэрэг ашиглах боломжгүй байдаг бөгөөд энэ тохиолдолд толиудаа нэгтгэх хэрэгтэй болдог. Үүний тулд [hunspell-merge](https://github.com/arty-name/hunspell-merge) ашиглахыг зөвлөж байна.
