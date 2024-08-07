

# Forecast degil Predict yaptim.
### Ne yaptim ne oldu ?

1-elimizdeki veriyi 90 10 olarak boldum.
2-targeti belirledim ve lag fonksiyonu olsusturarak rastgele adet lag olusturdum (4)
3-sonrasinda CNN modeli kurdum ve soruda bunu fonksiyon ile cagirilabilir olmasi isteniyordu,duzenledim.
4-CNN modeli kurulmus veriye daha once hic gormedigi y_test verisi kadar forecast yapmasini istedim
## kritik nokta
#### Aslinda forecast ileriyi tahminlemek demektir biz modelimize hicbir zaman y_test gostermedigimiz icin len(y_test) kadar tahmin yapinca aslinda klasik tahminlemeye donuyor.
ve biz bunu mse gibi metricslerle dogruluk oranini olcuyoruz.
# CNN VE LSTM'de verileri tensor olarak koymaliyiz 3D olmali
bu ve buna benzer onemli bilgileri detayli sekilde anlatacagim. takipte kalin...
