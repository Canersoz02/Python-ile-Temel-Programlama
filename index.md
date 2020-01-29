# Python ile Temel Programlama

## Print Komutu
Print komutunu, ekrana herhangi bir şey yazdırmak için kullanabiliriz. Bunu yapmak için print ve ardından parantez ve çift tırnak içinde istediğimiz ifadeyi yazarız. Ardından, sol üst köşedeki **Run> Run Program** butonuna basarak (F5'e de basabilirsiniz) programınızı çalıştırın. Raspberry Pi, sizi programınızı kaydetmeye yönlendirecektir. Programınızı herhangi bir isimle kaydettikte sonra sonuçlarını yeni bir pencerede göreceksiniz.
```python
print(“Hello World”) → Output: Hello World 
```
Bir variable (değişken), koşullara veya programa iletilen bilgiye bağlı olarak değişebilen bir değerdir. Bir variable'a istediğiniz kadar değer atayabilirsiniz. Her bir varible'ın adını kullandığınızda, Python aslında otomatik olarak yerine değerini koymaktadır. Bir örnek yapalım:
```python
isim = “Yasemin”
print(isim) → Output: Yasemin
```
Yukarıdaki örnekte, isim variable'ına "Yasemin" değerini atadık. Yani, biz bu variable'ı print ettirince, ekrana atadığımız değer yazdırılır. Bu değeri, kodun içinde daha sonra değiştirebiliriz. Bir başka örnek yapalım:
```python
isim = “Yasemin”
isim = “Tabag”
print(isim) → Output: Tabag
```

## Data Tipleri
Python' daki değişkenler birçok farklı formatta tutulabilir. BU tutulan formatlara "data tipi" denir. Bir değişkene atanan her data tipi, programda farklı bir yer kaplar. Bu basit data tiplerinin birkaç örneğini yapalım...
### Integer(int)
Bir tamsayıyı belirtir, yani negatif veya pozitif, virgülsüz herhangi bir sayı olduğunu gösterir. Python'da **int** olarak gösterilir. Örneğin: 0,5,-250,500
### Float(float)
Pozitif veya negatif, virgülle gösterimi olan ondalıklı bir sayıyı ifade eder. Python'da ondalıklı sayıları göstermek için virgül yerine nokta kullanılır (Amerikan sistemi). Python'da **float** olarak gösterilir. Örneğin: 0.01, 1.5, -2.5
### Boolean(bool)
Bir boolean, sadece True veya False değerlerini alabilir. Durumları veya koşulları göstermek için kullanılır. Python'da **bool** olarak gösterilir. Örneğin: True, False
### String(str)
Çift tırnak içerisinde bulunan karakter dizileridir. Python'da **str** olarak gösterilir. String'ler hem harfler hem de sayılardan oluşabilirler. Örneğin: "Yasemin", "sif123re"

Önemli: String içine yazılan bir sayı karakter olarak algılanır bu yüzden string'ler integer veya float değerleri ile karşılaştırılamazlar. Python'da 5 ve "5" farklı değerlerdir. İlki, 5 tam sayısına eşittir ve bununla işlemler vs. yapılabilir. İkincisi ise sadece 5 karakteridir, bir sayı değeri yoktur.
### List(list)
Adı üzerinde bir listedir. String veya sayı değerleri gibi farklı data tiplerini depolayabilir. Python'da list olarak gösterilir. Örneğin: [0,1,2,3,4,5,6,7]
### Type Metodu
Python'da bir değerin data tipini öğrenmek için **type** metodunu kullanırız. Örneğin: type(6)→int
### Data Tiplerinin Birbirine Çevrilmesi
Yukarıda anlatılan data tipleri birbirine çevrilebilir, buna **type casting** denir. Örneğin bir string'i integer ile karşılaştırmak için string'i integer'a çevirebiliriz. Bunu yapmak data tiplerinin Python'da kısa gösterimini (int,str vs.) kullanırız. Örneğin: int("2")→ 2 

"2" string'inin bir sayı değeri olmasa da bu string'i bir integer'a yani tamsayıya cast ettiğimizde artık bir sayı değeri vardır.

### Kod Örneği
```python
yas = 14
print(yas) → Output: 14
print(type(yas)) → Output: <class 'int'>


ortalama = 89.7
print(89.7) → Output: 89.7
print(type(ortalama)) → Output: <class 'float'>

yagmurYagiyor = False
print(yagmurYagiyor) → Output: False
print(type(yagmurYagiyor)) → Output: <class 'bool'>

isim = “Yasemin”
print(isim) → Output: Yasemin
print(type(isim)) → Output: <class 'str'>

yonler = [“Kuzey”, “Guney”, “Dogu”, “Bati”] 
print(yonler) → Output: [“Kuzey”, “Guney”, “Dogu”, “Bati”]
print(type(yonler)) → Output: <class 'list'>

dogumYili = “2001”
print(type(dogumYili)) → Output: <class 'str'>
dogumYili = int(dogumYili) 
#dogumYili artik “2001” degil, 2001 degerinde
print(type(dogumYili)) → Output: <class 'int'>
 
```

## Input
Input, kullanıcının yazılan programla iletişime geçebilmesi için kullanılır. Oyun oynarken girdiğimiz ok tuşları veya bilgisayara giriş yaparken girdiğimiz şifre input’a örnektir.

Python 3’de kullanıcı girişi almak için input() fonksiyonu kullanılır. Eğer input() komutunda alınması gereken belirli bir data tipi önceden verilmezse input() hep sonuç olarak string verir. Input’un içine eğer bir string değeri girersek bize yazılan stringi print eder ve sonra input almaya başlar.

```python
isim = input(“Adin nedir? ”) → Output: Adin nedir? Yasemin
print(isim) → Output: Yasemin
print(type(isim)) → Output: <class 'str'>
```

## Aritmetik
Python’u bir hesap makinesi olarak kullanabiliriz. Değişkenlerimizi tanımladıktan sonra, aynı matematikte olduğu gibi, bunları yazarak işlem yapabiliriz. 
### Toplama
\+ işareti ile print komutunu kullanarak istediğimiz bir işlem yazalım:
```python
x = 3
y = 5
print(x + y) → Output: 8
```
### Çıkarma
Çıkarma için - işaretini kullanırız.
```python
x = 3
y = 5
print(y - x) → Output: 2
```
### Çarpma
Çarpma işlemi için * işaretini kullanırız.
```python
x = 3
y = 5
print(y * x) → Output: 15
```

### Bölme
Bölme işlemi için / işaretini kullanırız.
```python
x = 3
y = 5
print(y / x) → Output: 1.6666666666666667
```

Python’da bölmek bize normalde kesin bir sonuç verir (yani float halinde kesirli bir sayı verir). Eğer sonucun sadece tam sayı kısmını almak istiyorsak // işaretini kullanırız.
```python
print(y // x) → Output: 1
```

### Üs Alma
Üs almak için ** işaretini kullanırız. (x üzeri y = x ** y)
```python
x = 3
y = 5
print(y ** x) → Output: 125
```

### Modülo
Modülo, bir bölmenin kalanını verir. Modülo için % işaretini kullanırız.
```python
x = 3
y = 5
print(y % x) → Output: 2
```
UNUTMAYIN: İşlem önceliği Python’da da geçerlidir!


## Egzersiz: Ortalama Hesaplama
Bir kullanıcıya input() fonksiyonuyla 3 farklı dersinin notunu soran ve bunların ortalamasını hesaplayıp print eden bir program yazın. (input()’un sonucunu int’e çevirmeyi unutmayın!)

```python 
not1 = int(input(“Birinci notu girin: ”))
not2 = int(input(“Ikinci notu girin: ”))
not3 = int(input(“Ucuncu notu girin: ”))
ortalama = (not1 + not2 + not3) / 3
print(“Ortalama: ” + ortalama)
```

## If/Else If/Else
### If Komutu
If komutu, sonucu True veya False olan ifadeleri değerlendirir. Eğer if’in yanında yazan ifade True (yani doğru) oluyorsa if’in altında yazan kod bloğu çalışır. Aksi takdirde alttaki kod bloğu çalışmaz. If komutunu yazarken sonunda : koymayı ve alt satırda içe geçmeyi unutmayın!
Örnek: Eğer yağmur yağıyorsa, şemsiye götür.  
```python
if yagmurYagiyor == True:
    print(“Semsiye gotur!”)
```

### Else If (Elif) Komutu
Eğer if’in yanında yazan ifade False (yani yanlış) oluyorsa Python bir elif (else if) kod bloğu arar. İlk ifade yanlışsa ancak altındaki elif ifadesi doğruysa elif’in altındaki kod bloğu çalışır.

Örnek: Eğer yağmur yağıyorsa, şemsiye götür. Eğer yağmur yağmıyorsa ama kar yağıyorsa, eldiven giy.
```python 
if yagmurYagiyor:
    print(“Semsiye gotur!”)
elif karYagiyor:
    print(“Eldiven giy!”)
```

### Else Komutu
Eğer if veya elif’lerde yazılan bütün ifadeler False (yani yanlış) oluyorsa else’in altındaki kod bloğu çalışır. Else’in yanına bir koşul koymaya gerek yoktur çünkü else son çaredir, sadece başka hiçbir şey doğru değilse çalışır.

Örnek: Eğer yağmur yağıyorsa, şemsiye götür. Eğer yağmur yağmıyorsa ama kar yağıyorsa, eldiven giy. Eğer yağmur da kar da yağmıyorsa, güneş gözlüğü tak.
```python 
if yagmurYagiyor:
    print(“Semsiye gotur!”)
elif karYagiyor:
    print(“Eldiven giy!”)
else:
    print(“Gunes gozlugu tak!”)
```

### Karşılaştırma Operatörleri
Python’da karşılaştırma yaparken alışık olduğumuz karşılaştırma operatörlerini kullanırız:
* \> ​Büyüktür 
* \< ​Küçüktür 
* \>= ​Büyüktür eşittir 
* \<=​ Küçüktür eşittir 
* ==​ Eşit midir? 
	* DİKKAT: = işareti, variable’lara değer vermek için kullanılır. == ise iki değerin eşit olup olmadığını kontrol eder.
* != ​Eşit değil midir? (İki değerin farklı olup olmadığını kontrol eder)

### Mantıksal Operatörler
Mantıksal operatörler, birden fazla koşulu kontrol etmek için kullanılırlar. 

#### and
and kullanılırken ifadenin True olması için iki ifade de doğru olmalıdır.
```python
True and True #True
True and False #False
False and True #False
False and False #False
```


#### or
or kullanılırken ifadenin True olması için en az bir ifade doğru olmalıdır.
```python
True or True #True
True or False #True
False or True #True
False or False #False
```

#### not
not kullanılınca ifadenin tersi alınır.
```python
not True #False
not False #True
```
## Egzersiz: Takdir/Teşekkür Belgesi
Önceki ortalama yazma programınızı devam ettirerek eğer ortalama 85’in üstündeyse “Takdir” print ettirin. Eğer ortalama 70 ve 85 arasındaysa “Tesekkur” print ettirin. Eğer ortalama 70’in altındaysa “Maalesef belge alamadin :(“ print ettirin.

```python
if ortalama > 85:
	print(“Takdir”)
elif ortalama > 70:
	print(“Tesekkur”)
else:
	print(“Maalesef belge alamadin :(”)
```

DİKKAT!
```python
if ortalama > 85:
	print(“Takdir”)
if ortalama > 70:
	print(“Tesekkur”)
if ortalama < 70:
	print(“Maalesef belge alamadin :(”)
```

If yerine neden elif kullanıyoruz? Yukarıdaki örneğe bakarsak, eğer ortalama 85’ten büyükse hem Takdir, hem de Tesekkur print eder. Bu nedenle üst üste if kullanmak yerine elif kullanmayı tercih ederiz.


## For Döngüsü
For döngüsü, “for” ifadesindeki koşul artık geçerli olmayana kadar, bir kod bloğunu tekrar tekrar yürütür. For döngüsü, herhangi bir kod bloğunu belli bir sayıda tekrar ettirmek için kullanılır.

Örnek:
```python
hayvanlarim = [“kediler”, “kopekler”, “tavsanlar”, “kuslar”]

for hayvan in hayvanlarim:
    print(hayvan)

→ Output:
kediler
kopekler
tavsanlar
kuslar
```

Yukarıda, önce *hayvanlarim* listesini yazıyoruz. *for hayvan in hayvanlarim:* ifadesi, yazdığımız hayvan değişkenine, bir döngü oluşturup, sırayla listedeki hayvanları atıyor. Program, listenin sonuna ulaşana kadar liste boyunca döngüye geçmeye devam eder. Böylece, hayvan isimli değişken, “kediler”, “kopekler”, “tavsanlar”, '“kuslar”ı ifade eder. Daha sonra bunu print ettiğimizde de karşımıza bu listedeki hayvanlar çıkıyor. 
### Range
Range fonksiyonu, for loop yazarken en sık kullanılan fonksiyonlardan bir tanesidir. range(x), sıfırdan başlayarak x kadar sayı demektir. Örneğin, range(3) = 0, 1, 2. Biz range’i for looplarda range’in içindeki sayı kadar loopu tekrar etmek için kullanırız.


Örnek:
```python
for i in range(5):
    print(i)

→ Output:
0
1
2
3
4
```


## While Döngüsü
While döngüsü, belirli bir koşul geçerli kaldığı sürece, bir kod bloğunu tekrar tekrar yürütür. While döngüsünü, bir kod bloğunu tekrar ettirmek istediğimiz ama kaç kez tekrar edeceğini bilmediğimizde kullanırız. 

Örnek:
Diyelim ki bir bilgisayara Super Mario oynatıyoruz ve önüne bir Mario’nun engel çıkana kadar yürümeye devam etmesini istiyoruz, ancak doğal olarak bu engelin ne zaman çıkacağını bilmiyoruz.

```python
engel = False
while not engel:
	print(“Mario 1 kare ileri gitti.”)
      # engelKontrolu() adli hayali fonksiyon, Mario’nun onunde engel olup
      # olmadigini kontrol eder ve eger engel varsa engel
      # degiskenini True hale getirir.
	engelKontrolu() 
print(“Mario’nun onunde bir engel var.”)

→ Output:
Mario 1 kare ileri gitti.
Mario 1 kare ileri gitti.
Mario 1 kare ileri gitti.
Mario 1 kare ileri gitti.
…
Mario 1 kare ileri gitti.
Mario’nun onunde bir engel var.
```

### Sonsuz While Döngüleri
Eğer while döngüne özel bir koşul verilmezse, veya verilen koşul değişmez ise while döngüsü sonsuza dek çalışır. Bazen biz bir kod bloğunu sonsuza dek çalıştırmak isteriz. Bunun içinde 
while True: cümlesini kullanırız.

Örnek:
```python
while True:
    print(“Yasemin”)

→ Output:
Yasemin
Yasemin
Yasemin
Yasemin
ׅׅׅׅׅׅׅ…
```

### Limitli While
Bir while döngüsünü aynı zamanda bir for döngüsü gibi de kullanabiliriz. Yani spesifik bir sayıda işlem yapmasını sağlayabiliriz.

Örnek:
```python
sayac = 3
while sayac >= 0:
	print(“Sayac = ” + sayac)
	sayac = sayac - 1
print(“Sayac bitti!”)

→ Output:
Sayac = 3
Sayac = 2
Sayac = 1
Sayac = 0
Sayac bitti!
```

## List
Liste, Python’da sık kullanılan bir veri türüdür. Herhangi bir listenin içinde data toplayabilir, “liste metodları” dediğimiz fonksiyonlarla da bu listeleri değiştirebiliriz. Bir örnek yapalım:

```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar) → Output: [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar[0]) → Output: kedi
```

Yukarıdaki örnekte, listedeki her elemana sıfırdan başlayarak devam eden bir sayı verilmiştir. Bu verilen sayılara index sayıları denir. Yazdığımız kodda, “0” indexindeki eleman, yani kedi elemanı print edilmiştir. Başka bir örnek yapalım:

```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar[1]) → Output: kopek
print(hayvanlar[4]) → Output: bu komut, “IndexError: list index out of range” error’ü verir, çünkü hayvanlar’ın 4. index’i yoktur
```

### Liste Metotlar
#### append() metotu
Listenin sonuna yeni bir eleman eklemek için kullanılır. Örnek:
```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
hayvanlar.append(“panda”)
print(hayvanlar) → Output: [“kedi”, “kopek”, “tavsan”, “kus”, “panda”]
```

#### pop() metotu
Listenin sonundaki elemanı çıkarmak için kullanılır. Örnek:
```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
hayvanlar.pop()
print(hayvanlar) → Output: [“kedi”, “kopek”, “tavsan”]
```
#### List Slicing
Eğer listenin içindeki elemanların bir kısmını almak istiyorsak, slicing metodunu kullanırız. List slicing’de, print etmek istediğimiz elemanların ilkinin ve sonuncusunun indexini yazarız. Indexlerdeki elemanlar dahil olarak bunlar print edilir. Bir örnek yapalım:

```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar[0:2]) → Output: [“kedi”, “kopek”]
```

Slicing metodunda eğer ilk indexten başlayacaksak o sayıyı yazmamıza gerek yoktur. Aynı şekilde, eğer slice edeceğimiz kısım en son indexte bitecekse o kısmı da boş bırakabiliriz. İki noktadan önceki kısımda görünmeyen bir sıfır vardır. Örnek:

```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar[:3]) → Output: [“kedi”, “kopek”, “tavsan”]
```

İki noktadan sonraki kısımda görünmeyen bir sonuncu index vardır. Listedeki eleman sayısına göre bu index değişir. Örnek:

```python
hayvanlar = [“kedi”, “kopek”, “tavsan”, “kus”]
print(hayvanlar[:3]) → Output: [“kus”]
```
## Fonksiyonlar
Fonksiyonlar, bir kere tanımlandıktan sonra sürekli yeniden kullanılabilen, her çağrıldığında aynı şeyi yapan kod parçalarıdır. Python’da önceden yazılmış olan birçok fonksiyon olduğu gibi, kendimiz de fonksiyon tanımlayabiliriz. Python’a yüklü olan fonksiyonlara modül denir. En basit modül örneği olarak print() komutunu verebiliriz. Bir fonksiyon örneği yapalım:

```python
def fonksiyonOrnegi():
	print(“Pi Wars 2020’ye hosgeldiniz!”)
```

Yukarıda yazdığımız fonksiyon, tahmin edilebildiği gibi, print()’in içinde yazan ifadeyi print edecek. fonksiyonOrnegi() diyerek, bu fonksiyonu programın içinde herhangi bir yerde çağırabiliriz:

```python
def fonksiyonOrnegi():
	print(“Pi Wars 2020’ye hosgeldiniz!”)
fonksiyonOrnegi() → Output: Pi Wars 2020’ye hosgeldiniz!
```

### Parametreler
Bir fonksiyona “parametreler” ekleyebiliriz. Matematikteki fonksiyonlara nasıl bir sayı değeri veriyorsak ve o değere  göre fonksiyonu hesaplıyorsak, Python’daki fonksiyonlarda da bunu yapıyoruz. Yani, parametre olarak yazdığımız değer bize fonksiyonun içine yerleştirilmiş bir biçimde geri dönüyor. Örneğin, Python’da bulunan print() modülünün içinde yazdığımız mesaj, o fonksiyonunun bir parametresidir. 

```python
print(“Pi Wars 2020’ye hosgeldiniz!”)
 ↓                   ↓
Fonksiyon		Parametre
```

Python’da bir fonksiyonun parametreleri sayı olmak zorunda değildir, string veya boolean da olabilir. Virgülle ayrıldığı sürece, bir fonksiyona birden fazla parametre eklenebilir.

Örnek1:
```python
def kacYasindasin(yas):
	print(“Ben, ” + yas + “yasindayim.” )
kacYasindasin(“14 ”) → Output: Ben, 14 yasindayim.
```

Örnek2:
```python
def carpiBes(x):
	print(x * 5)
carpiBes(5) → Output: 25
```

## Egzersiz: Faktoryel Hesaplama
Verdiğimiz sayının faktoryelini hesaplayan bir fonksiyon yazalım.
```python
def faktoryel(n):
	carpim = 1
	for x in range(2, n+1):
		carpim = carpim * x
	print(str(n) + “! = ” + str(carpim))
faktoryel(5) → Output: 5! = 120
faktoryel(10) → Output: 10! = 3628800
```
