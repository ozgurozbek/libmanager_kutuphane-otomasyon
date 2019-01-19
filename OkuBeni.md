 # libmanager_kutuphane-otomasyon
 
## Açıklama
C# programlama dili kullanılarak Katmanlı mimari ile yapılmıştır. Access veri tabanı 	  kullanılmıştır. Aşağıdaki istekler çerveçesinde yapılmıştır. Programın içindeki yorum satırları türkçedir.

## İstekler
 - 1)Katmanlı Mimari kullanılcak.
 - 2)Öğrenci ve Kitap ekle, sil, güncelle olucak.
 - 3)Kitap ver ve kitap geri al olucak.
 - 4)Öğrencinin şimdiye kadar aldığı verdiği ve şuan elinde olan kitap görüntülenebilcek.
 - 5)Öğrencinin geciktirdiği kitaplar listesinde kırmızı olarak işaretlencek.
 - 6)Kitabın teslim süresine iki gün kaldıysa eğer uyarı amaçlı sarı işaretlencek.
 - 7)Teslim edilmiş kitaplar yeşil renkte işaretlenecek.
 - 8)Teslim edilmesine 2 gün kalana kadar turkuazla işaretlenecek.
 - 9)Kitap alma ve iade işlemleri tarihsel düzeyde gerçekleşecek.
 - 10)Kitap odu ve adına göre kitap bilgilerine ulaşılabilcek.
 - 11)Kitabın geciktirildiği her gün için 1 tl lik ceza yazılacak.
 - 12)Kütüphanedeki tüm kitaplar, öğrenciye verilmiş olan kitaplar ve verilmye hazır olan kitaplar **Zedgrapgh** ile grafik ile gösterilcek.

## Katmanlar
### Entity Layer (Varlık Katmanı)
Access tablolarımızı kodda tek tek oluşturup içindeki sutunları oluşturduğumuz yerdir. Kodda bu sutunlara gelecek değişkenleri oluşturup kapsüllemelerini yaptık. Diğer katamnalrdan erişimizi sağlama için classlarımızı public yaptık.
### Facade Layer (Cephe Katmanı)
SQL işlemlerinin yapıldığı katman. Bu katmanda entity katmanı ile beraber iş yapmaktayız bunu yapa bilmek için başvurulardan (referances) entity layeri ekleyip kullandığımız yerlerin tamamında çağırmamız gerekiyor. 
### Business Logic Layer (İş Mantık Katmanı)
Sunum katmanından aldığımız değerleri kontrol edip facade katmanına yolladığımız yerdir. Yine classlar public yapılır ve burayada  entity ve facede katmanı referanslanır ve çağırılır.
### Presentations Layer (Sunum Katmanı)
Kullanıcının gördüğü katmandır. Burdan aldığımız değerleri Business Logic Layera yollarız. Diğer katmanları tekrardan burada referanslamamız ve çağırmamız gerekli.