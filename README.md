# 1 – Why we need to use OOP ? Some major OOP languages ?

    Hiç şüphe yok ki yazılım dünyasında en çok karşılaşılan kavramlardan bir tanesi nesne tabanlı programlama kavramıdır. Nesne tabanlı programlama aslında bir düşünme şekli, bir felsefe olarak kabul edilebilir. Bu felsefede her şey nesnedir. Gerçekleştirilen işlemler nesneler ve nesneler arasındaki ilişkiler yardımı ile gerçekleştirilir.

    Object Oriented Programming (kısaca OOP) için gerçek hayatın yazılım dünyasına aktarılmasıdır demek yanlış olmaz. Çünkü çevremizde gördüğümüz her şey de aslında birer nesnedir. Örneğin siz bir nesnesiniz ve sizi siz yapan bazı özellikler bulunmaktadır. İsminiz, doğum yılınız, göz renginiz ve boyunuz gibi pek çok özelliğe sahipsiniz. Ayrıca gerçekleştirdiğiniz bazı davranışlar da bulunmaktadır. Örneğin yemek yemek, uyumak, yazı yazmak gibi bazı davranışları da gerçekleştiriyorsunuz. Nesne yönelimli programlamada da olay aynen bu şekildedir. Bir nesnenin özellikleri ve davranışları bulunmaktadır. Bu özellik ve davranışlar sınıf içerisinde oluşturulur. Sınıf, nesnelerin üretim merkezidir. Bir nesnenin özellikleri ve davranışları sınıf içerisinde belirtilir ve buna göre üretim yapılır. Nesnelerin özellikleri değişkenler ile oluşturulurken; davranışları metotlar/fonksiyonlar ile belirlenir. Nesnelerin oluşturulması için ise "new" anahtar sözcüğü kullanılır ve "new" anahtarının kullanılması ile bellekte o nesneye özel bir yer ayrılır. Böylece nesne artık var olmuş, hayata geçmiştir.

## OOP ÖNEMİ

    Geliştirilen hemen hemen her yazılım projesi OOP mantığı ile geliştirilmektedir. Dolayısıyla OOP, her yazılımcının bilmesi gereken bir kavramdır. Ayrıca OOP mantığını iyi kavramak, diğer yazılım kavramlarının daha rahat anlaşılmasını sağlar. Örneğin, Tasarım Desenleri konularına hakim olmak istiyorsanız OOP bilmeniz şarttır ve OOP mantığını iyi kavradıysanız Tasarım Desenleri öğrenmeniz de daha rahat olacaktır. Bunlarla beraber, güzel ve kaliteli projeler gerçekleştirmek için kullanılan yazılım diline hakim olmak gerekmektedir ve günümüzde kullanılan yazılım dillerinin çoğu nesne tabanlıdır. Dolayısıyla OOP mantığına hakim olmak, kullanılan yazılım dilinden daha fazla yararlanabilmek ve daha kaliteli projeler gerçekleştirebilmek anlamına gelir. Sıklıkla kullandığımız Java, C#, C++ ve Python gibi diller nesne tabanlı programlama dillerine örnek verilebilir.

## Sıklıkla kullanılan OOP DİLLERİ

- JAVA
- C#
- C++
- Python

# 2 – Interface vs Abstract class ?

    Soyutlama yapabilmek için nesneye yönelik programlamada iki yöntem mevcuttur; interface ve abstract. Soyutlama kavram olarak sınıfın içindeki işleyişini dışarıya kapamaktır. Örneğin, atmde işlem yaparken kullanıcıların atmnin işleyişinden bilgisi olmaz. Kullanıcılar, metodları veya akışı arayüz sayesinde çağırarak kullanır. Kartın doğrulanması, hesap bilgilerinin kontrolü, yapılacak işleme göre yeterli bakiye bulunup bulunmadığının hesaplanması gibi metotların işleyişinden kullanıcı haberdar olmaz. Bu işleyişe müdahale edilemez. Nesneye yönelik programlamada da sınıflar oluşturulurken bazı metotların işleyişinin sadece bulunduğu sınıf tarafından bilinmesi gerektiği durumlar olabilir.

## Abstraction

    Abstraction implementasyon ayrıntılarını kullanıcıdan gizler. Abstract (soyut) kavramı yalnızca sınıflar ve metotlar ile kullanılır, değişkenler için kullanılmaz. Herhangi bir metodu abstract olarak tanımlarsak, o metodun görevinin/uygulamasının (implementation) ilgili sınıfın alt sınıfında olması gerekir, çünkü abstract metotlar hiçbir zaman implementasyondan bahsetmez.

## Interface

    Interface, sınıflara ait metotların sadece imzalarının bulunduğu, implementasyonlarının bulunmadığı bir yapıdır. Interface içerisinde sadece soyut metotlar tanımlanabilir. Eğer bir sınıf interface'den miras alırsa, interface'de tanımlanmış olan her bir soyut özelliği de (metotları da) miras alması gerekir. Miras alan sınıf, interface'de bulunan bir veya daha fazla metoda ihtiyaç duymuyorsa yazılımın tasarımsal açıdan bir sorunu var demektir. Bu sorun, interface'lerin alt interface'lere bölünmesiyle yani **Interface Segregation** ile çözülebilir.

![Resim Açıklaması](file://C:\Users\Asuss\Desktop\patikahw1\hw-1-iremkvkpnr\images\resim1.png?msec=1742582807161)

# 3 – Why wee need equals and hashcode ? When to override ?

## Neden equals() ve hashCode() Kullanmalıyız?

    Java'da equals() ve hashCode() metotları, nesneleri karşılaştırmak ve koleksiyonlarda doğru şekilde çalışmasını sağlamak için çok önemlidir.

### 1. Nesne Karşılaştırması (equals())

    Varsayılan olarak == operatörü, nesne referanslarını karşılaştırır, içeriği değil. Ancak çoğu zaman nesnelerin içerik olarak eşit olup olmadığını kontrol etmek isteriz. İşte bu noktada equals() devreye girer.

### 2. Koleksiyonlarla Çalışma (hashCode())

    Hash tabanlı koleksiyonlar (HashMap, HashSet, Hashtable) nesneleri saklarken hashCode() metodunu kullanır. Eğer hashCode() doğru bir şekilde override edilmezse, equals() ile eşit kabul edilen nesneler koleksiyonlarda hatalı çalışabilir.

## equals() ve hashCode() Ne Zaman Override Edilmelidir?

Bu metotları şu durumlarda override etmelisiniz:

- Özel nesne karşılaştırması yapmak istiyorsanız (Örneğin, Person nesnelerini id alanına göre karşılaştırmak).
- Nesneniz HashSet, HashMap gibi hash tabanlı koleksiyonlarda kullanılacaksa.
- İki nesnenin aynı olarak algılanmasını istiyorsanız.

## equals() ve hashCode() Nasıl Override Edilir?

    Aşağıda, Person sınıfında equals() ve hashCode() metotlarının doğru şekilde override edilmesine bir örnek verilmiştir:

```java
import java.util.Objects;  

class Person {  
    private int id;  
    private String name;  

    public Person(int id, String name) {  
        [this.id](http://this.id/) = id;  
        [this.name](http://this.name/) = name;  
    }  

    @Override  
    public boolean equals(Object obj) {  
        if (this == obj) return true;  
        if (obj == null || getClass() != obj.getClass()) return false;  
        Person person = (Person) obj;  
        return id == [person.id](http://person.id/);  
    }  

    @Override  
    public int hashCode() {  
        return Objects.hash(id);  
    }  
}  
```

## Önemli Noktalar:

- equals() metodu, nesneleri id alanına göre karşılaştırır.
- hashCode() metodu, id değerine dayalı bir hash üretir ve equals() ile tutarlı olmasını sağlar.
- equals() metodunu override ettiğinizde, her zaman hashCode() metodunu da override etmelisiniz.

# 4 – Diamond problem in Java ? How to fix it?

    Java'daki elmas problemi, bir sınıfın aynı temel sınıftan miras alan iki sınıftan miras aldığı çoklu miras bağlamında ortaya çıkan belirsizliğe atıfta bulunur. Bu, elmas biçimli bir miras yapısı oluşturur ve yöntem çözümünde belirsizliğe yol açar.

![Resim Açıklaması](file://C:\Users\Asuss\Desktop\patikahw1\hw-1-iremkvkpnr\images\resim2.png?msec=1742582952853)

## Önemli Noktalar

- **Sınıfların Çoklu Kalıtımı**: Java, doğrudan elmas sorununu önlemek için sınıflar için çoklu kalıtımı desteklemez.
- **Arayüzlerde Varsayılan Yöntemler**: Java 8 arayüzlerde varsayılan yöntemleri tanıttı; bu, birden fazla arayüz uygulandığında elmas sorununa yol açabilir.
- **Açık Çözüm**: Elmas problemi, uygulayıcı sınıftaki çakışan metodu açıkça geçersiz kılarak ve hangi üst arayüzün metodunun kullanılacağını belirterek çözülür.

Bu mekanizma, yöntem çözümünde herhangi bir belirsizlik olmamasını sağlar ve net, belirsizliğe yer vermeyen bir miras yapısına olanak tanır.

# 5 – Why we need Garbagge Collector ? How does it run ?

    Java ve bazı Nesneye Yönelik Programlama dillerinde GC bulunmaktadır. Ancak bazı orta seviyeli programlama dillerinde işi biten nesneyi bellekten silmek, programcının görevidir. Örn : C++'da bir nesneyi Destructor (yıkıcı veya yok edici) metodu ile yok ederiz.

    Java dilinde bir sınıftan oluşturulan nesnenin işi bittiğinde bellekte ona ayrılan yer boşaltılır. Belleği boşaltma işlevi Garbage Collector'dır.

```java
public class Main {
    public static void main(String[] args) {
        Integer a = 5;
        Integer b = 7;
        Integer toplam = 0;
        toplam = a + b;
        .
        .
        .
    }
}
```

    Yukarıdaki örnekte Integer tipinde 3 değişken oluşturulmuştur. a ve b değişkenleri toplam değişkeninde
işlem gördükten sonra bir daha kullanılmamıştır. Dolayısıyla programın akışı
boyunca bellekte sürekli olarak gereksiz yer işgal edecektir. Garbage Collector
ise bu süreçte programı yukarıdan aşağıya akışını takip eder ve belleği işgal
eden alanları boşaltır.

    Bir süreç (process) başladığı anda bellekte bu process için boş bir yer ayırılır. Bu ayrılan boşluğa daha önce **Bilgisayar ve Bellek** konusunda bahsettiğimiz heap bölgesi denir. Referanslar aracılığıyla heap bellekten nesnelerin yerleri tutulur. RunTime'da oluşturulan nesneler, uygulama tarafından ihtiyaç duyulmadığı zamanlarda ya da programda oluşturulan nesnenin işi bittiğinde, heap bellekten temizlenir. Bu işlem için "Garbage Collector" mekanizması kullanılır.

## Garbage Collector Çalışma Mantığı

```java
public class Main {
    public static void main(String[] args) {
        Integer a = new Integer(5);
    }
}
```

### Senaryo

    Program "new" operatörünü çalıştırdığı zaman "heap" belleğe gider ve bellekte yeterli bir yer alan olup olmadığına kontrol eder. Yeterli alan varsa referans, bellekteki bu yeri gösterir, nesnenin yapılandırıcı metodu çalışır.

# 6 – Java 'static' keyword usage ?

    Java'da static anahtar kelimesi, bir sınıfa ait olan üyeleri (değişkenler, metotlar, bloklar ve iç sınıflar) belirtmek için kullanılır. static olarak tanımlanan öğeler, sınıfın bir örneği oluşturulmadan doğrudan sınıf adıyla erişilebilir. İşte static anahtar kelimesinin kullanım alanları:

## Static Değişkenler (Class Variables)

Bir sınıfa ait olup, tüm örnekler tarafından paylaşılan değişkenlerdir.

```java
class Example {  
    static int count = 0;  
}  
```

Example.count olarak doğrudan erişilebilir.

## Static Metotlar (Class Methods)

Sınıfın nesnesi olmadan çağrılabilen metotlardır.

```java
class Example {  
    static void show() {  
        System.out.println("Static method called");  
    }  
}  
Example.show(); // Çıktı: Static method called  
```

## Static Bloklar (Static Initializer Blocks)

Sınıf belleğe yüklendiğinde bir kez çalıştırılan kod bloklarıdır.

```java
class Example {  
    static {  
        System.out.println("Static block executed");  
    }  
}  
```

## Static İç Sınıflar (Static Nested Classes)

Bir sınıf içinde static olarak tanımlanmış iç sınıflardır.

```java
class Outer {  
    static class Inner {  
        void display() {  
            System.out.println("Static nested class");  
        }  
    }  
}  
Outer.Inner obj = new Outer.Inner();  
obj.display();  
```

## Static Import

Bir başka sınıfın static üyelerine doğrudan erişmek için kullanılır.

```java
import static java.lang.Math.PI;  
System.out.println(PI); // Math.PI yerine doğrudan PI kullanılabilir  
```

## Önemli Notlar:

- static metotlar, nesneye özgü olmayan işlemler için uygundur.
- static metot içinde this veya super anahtar kelimeleri kullanılamaz.
- static değişkenler tüm nesneler arasında paylaşılan tek bir bellek alanına sahiptir.

# 7 – Immutability means ? Where, How and Why to use it ?

    Değişmezlik (immutability), bir nesnenin oluşturulduktan sonra durumunun değiştirilememesi anlamına gelir. Java'da String, Integer, Double gibi bazı sınıflar değişmezdir.

## Neden Değişmezlik Kullanılır?

- **Thread-Safe (İş Parçacığı Güvenliği)**: Değişmez nesneler birden fazla iş parçacığı (thread) tarafından güvenle paylaşılabilir.
- **Cache ve Performans Avantajı**: Değişmez nesneler cache mekanizmalarında ve hash tabanlı koleksiyonlarda daha verimli kullanılır.
- **Öngörülebilirlik**: Bir nesnenin değişmediğini bilmek, hataları önlemeye yardımcı olur.

## Değişmez Bir Sınıf Nasıl Oluşturulur?

- Sınıfı final olarak tanımla (alt sınıflar oluşturulamaz).
- Tüm alanları private final yap (doğrudan değiştirilemez).
- Setter metodu sağlamama (değerler değiştirilemez).
- Değiştirilebilir alanlar için derin kopyalama yap (koleksiyonlar, nesne referansları).

```java
final class ImmutablePerson {  
    private final String name;  
    private final int age;  

    public ImmutablePerson(String name, int age) {  
        [this.name](http://this.name/) = name;  
        this.age = age;  
    }  

    public String getName() {  
        return name;  
    }  

    public int getAge() {  
        return age;  
    }  
}  
```

Bu sınıfta name ve age değiştirilemez, çünkü setter metodu yoktur ve alanlar final olarak tanımlanmıştır.

## Nerede Kullanılır?

- Çok iş parçacıklı uygulamalar (Thread safety için).
- Hash tabanlı koleksiyonlar (HashMap, HashSet).
- Güvenlik gerektiren sistemler (Hassas verileri değiştirilmez kılmak için).

# 8 – Composition and Aggregation means and differences ?

    Nesne Yönelimli Programlama (OOP), yazılım geliştirmenin temel prensiplerinden biridir ve bu prensipler arasında nesneler arasındaki ilişkileri açıkça ifade etmek önemli bir rol oynar. Bu ilişkileri belirleyen ve düzenleyen üç önemli terim, **association**, **aggregation** ve **composition** olarak adlandırılır. Bu terimler, yazılım geliştiricilere nesneler arasındaki bağlantıları daha iyi anlamalarına ve tasarımlarını daha etkili bir şekilde oluşturmalarına yardımcı olur.

## 1) Composition

    Composition ilişkisi, bir sınıfın birden fazla bağlı olduğu sınıflar arasında özel bir ilişki türünü ifade eder. Bu ilişkide, ana sınıf, bağlı olduğu diğer sınıflar olmadan var olabilir; ancak bağlı olduğu sınıflar, ana sınıf olmadan var olamazlar. Bu durum, güçlü bir bağlantıyı temsil eder, couple sıfatlandırması yapılabilir. İlk aşamada, bu sınıfların aynı alan içinde modellemesi beklenir, çünkü aralarındaki ilişki kuvvetlidir (sıkıdır). Ancak, uygulama büyüdükçe, başlangıçta aynı domain* içinde bulunan bu sınıflar farklı alanlara bölünebilir ve hala birbirlerine bağlı olarak var olabilirler.

Biz bu ilişkiye **has-a (sahiplik)** ilişkisi de diyebiliriz.

## 2) Aggregation

    Sahip olunan nesnenin, sahip olan nesneden bağımsız bir şekilde var olabilmesi durumu diyebiliriz. Örnek vererek açıklamak gerekirse:

```javascript
// Kitap sınıfı  
class Kitap {  
  constructor(isbn, baslik) {  
    this.isbn = isbn;  
    this.baslik = baslik;  
  }  

  bilgileriGoster() {  
    console.log(`ISBN: ${this.isbn}, Başlık: ${this.baslik}`);  
  }  
}  

// Kütüphane sınıfı, Aggregation ilişkisiyle Kitap sınıfını içerir  
class Kutuphane {  
  constructor(kutuphaneAdi) {  
    this.kutuphaneAdi = kutuphaneAdi;  
    this.kitaplar = []; // Kitapları tutan bir dizi  
  }  

  kitapEkle(kitap) {  
    // Aggregation: Kutuphane sınıfı, Kitap sınıfına sahiptir, ancak Kitaplar bağımsızdır  
    this.kitaplar.push(kitap);  
  }  

  kutuphaneyiGoster() {  
    console.log(`Kütüphane Adı: ${this.kutuphaneAdi}`);  
    console.log("Kitaplar:");  
    this.kitaplar.forEach(kitap => kitap.bilgileriGoster());  
  }  
}  

// Kitap nesneleri oluştur  
const kitap1 = new Kitap("978-0-13-449416-6", "Clean Code: A Handbook of Agile Software Craftsmanship");  
const kitap2 = new Kitap("978-0596007126", "JavaScript: The Good Parts");  

// Kütüphane nesnesi oluştur  
const bilgisayarKutuphanesi = new Kutuphane("Bilgisayar Kütüphanesi");  

// Kitapları kütüphaneye ekle  
bilgisayarKutuphanesi.kitapEkle(kitap1);  
bilgisayarKutuphanesi.kitapEkle(kitap2);  

// Kütüphaneyi göster  
bilgisayarKutuphanesi.kutuphaneyiGoster();  
```

    Burada mantık şu; kütüphane, kitaba sahip fakat kitap, kütüphanesizde tek başına var olabilir. İşte biz burada Kütüphane-Kitap arasındaki ilişkiye Aggregation ilişki türü diyebiliriz. Composition gibi burada da **has-a** ilişkisinden bahsedilebilir. Aralarındaki fark, **sahip olunan nesnenin, sahip olan nesneden bağımsız bir şekilde var olup olamaması durumudur**.

    Composition ilişkisi, sınıflar arasında güçlü bir bağlantıyı temsil ederken, Aggregation ilişkisi sahip olunan nesnenin bağımsız bir şekilde var olabilmesini ifade eder.

# 9 – Cohesion and Coupling means and differences ?

    Uyum (Cohesion), bir sınıf veya modülün tek bir amaca hizmet etme derecesidir. Yüksek uyum, bir bileşenin yalnızca belirli bir işlevi yerine getirmesi anlamına gelir. Bu, kodun daha okunaklı, bakımının kolay ve test edilebilir olmasını sağlar.

    Bağlılık (Coupling) ise bir bileşenin diğer bileşenlere ne kadar bağımlı olduğunu ifade eder. Düşük bağlılık, bileşenlerin birbirinden bağımsız çalışabilmesini sağlarken, yüksek bağlılık bir bileşende yapılan değişikliklerin diğer bileşenleri de etkilemesine yol açar.

# 10 – Stack vs Heap Memory in Java

Java'da bellek yönetimi Heap ve Stack adı verilen iki ana bölge üzerinden yapılır.

## Stack Bellek

- Küçük ve hızlı bir bellek bölgesidir.
- Metot çağrıları, yerel değişkenler ve referans değişkenler burada saklanır.
- LIFO (Last In, First Out) prensibiyle çalışır.
- Bellek otomatik olarak yönetilir ve metot çağrısı tamamlandığında değişkenler otomatik olarak temizlenir.

## Heap Bellek

- Büyük ve daha yavaş bir bellek alanıdır.
- Nesneler ve sınıf örnekleri burada saklanır.
- Çöp toplayıcı (Garbage Collector) tarafından yönetilir.
- Global erişime açıktır, yani farklı metodlar ve thread'ler buradaki verilere erişebilir.

## Stack ve Heap Arasındaki Farklar

| Özellik | Stack | Heap |
| --- | --- | --- |
| **Kullanım Alanı** | Yerel değişkenler ve metot çağrıları | Nesneler ve sınıf örnekleri |
| **Hız** | Daha hızlı | Daha yavaş |
| **Yönetim** | Otomatik olarak temizlenir | Garbage Collector tarafından yönetilir |
| **Erişim** | Sınırlı ve geçicidir | Daha uzun süre saklanabilir |

Stack, hızlı ve geçici veriler için kullanılırken, Heap uzun süreli veri saklama için idealdir.  
Performans açısından dengeli bir bellek yönetimi sağlamak için ikisi birlikte kullanılır.

# 11 – Exception means ? Type of Exceptions ?

    Exception (İstisna), bir programın çalışma zamanında beklenmedik bir durumla karşılaşması sonucu oluşan hatadır. Java'da istisnalar, hataların kontrol altına alınmasını ve programın çökmeden çalışmasını sağlar.

## Java'da Exception Türleri

Java'daki istisnalar iki ana kategoriye ayrılır:

### Checked Exceptions (Denetlenen İstisnalar)

- Derleme (compile-time) sırasında kontrol edilir.
- Programcı tarafından ele alınması zorunludur, aksi halde derleme hatası oluşur.
- Genellikle dosya okuma/yazma, veritabanı işlemleri gibi dış kaynaklarla çalışırken ortaya çıkar.
- Örnekler: IOException, SQLException, FileNotFoundException

### Unchecked Exceptions (Denetlenmeyen İstisnalar)

- Çalışma zamanında (runtime) oluşan istisnalardır.
- Derleme sırasında kontrol edilmez, ancak programın çalışması sırasında hataya neden olabilir.
- Genellikle programcı hatalarından kaynaklanır.
- Örnekler: NullPointerException, ArrayIndexOutOfBoundsException, ArithmeticException

### Error (Hata)

- Sistem seviyesindeki ciddi hatalardır.
- Programcı tarafından yakalanamaz ve düzeltilmesi genellikle mümkün değildir.
- Örnekler: OutOfMemoryError, StackOverflowError, VirtualMachineError

Java'da try-catch blokları kullanılarak istisnalar yakalanabilir ve programın düzgün çalışmaya devam etmesi sağlanabilir.

# 12 – How to summarize 'clean code' as short as possible ?

    Kod, kolayca anlaşılabiliyorsa temizdir - ekipteki herkes tarafından. Temiz kod, orijinal yazarından başka bir geliştirici tarafından okunabilir ve geliştirilebilir. Anlaşılabilirlikle birlikte okunabilirlik, değiştirilebilirlik, genişletilebilirlik ve sürdürülebilirlik gelir.

# 13 - What is the method of hiding in Java ?

    Eğer alt sınıf, üst sınıftan devralacağı bir üyeyi kendisi tekrar tanımlarsa, bu durumda üst sınıftaki üye devralınmaz ve alt sınıfta erişimde doğrudan kendi sınıfının üyesine ulaşılır. Buna **gizleme (hiding)** denir. Kısaca alt sınıftaki üye, üst sınıftaki üyeyi gizler.

    Bu durumda üst sınıfın üyelerine ulaşmak için `super` kullanılır.

    Tekrar tanımlamada alt sınıf üst sınıftaki üyeyi; değişken ise aynı isimle, metot ise **arayüzle** tekrar tanımlar.

## Gizleme Türleri

Gizleme dört üyede olabilir:

- Sınıf değişkeni ve metodu
- Nesne değişkeni ve metodu

### Değişken Gizleme:

- Üst sınıftaki değişkenler, alt sınıfta aynı isimde tekrar tanımlandığında alt sınıftan gizlenirler.
- Bu durumda doğrudan isimle sınıftaki değişkene `super` ile beraber isimle, üst sınıftaki değişkene ulaşılır.
- Gizleyen ve gizlenen değişkenlerin tipleri farklı olabilir.
- Değişken gizlemenin **anlamlı bir kullanımı yoktur**, bu nedenle pek kullanılmaz.

### Metot Gizleme:

- Üst sınıftaki metotlar da alt sınıfta **arayüzleri** aynı bırakılarak yeni bir **gerçekleştirmeyle (implementation)** tekrar tanımlanabilirler.
- Tekrar tanımlanırken metodun arayüzünde hiç bir şey değiştirilmemelidir.
- Metodun sadece gerçekleştirmesi değiştirilebilir.

### Metot Gizleme ve Ezme (Overriding):

- Aslen metotlarda gizlenme sadece statik metotlar için geçerlidir.
- Yani üst sınıfın statik metodu, alt sınıfta aynı arayüzle statik olarak tekrar tanımlanırsa bu metot gizleme olur.
- Üst sınıfın nesne metotlarını alt sınıfta tekrar tanımlamaya gizleme denmez, buna **ezme** ya da **overriding** denir.
- Alt sınıftaki bir sınıf metodu, üst sınıftaki bir sınıf metodunu gizleyebilir.
- Alt sınıftaki bir sınıf metodu, üst sınıftaki bir nesne metodunu gizleyemez. Bu bir hatadır.
- Alt sınıftaki bir nesne metodu, üst sınıftaki bir sınıf metodunu gizleyemez, aslen bu bir ezme girişimidir ancak hatadır.

# 14 - What is the difference between abstraction and polymorphism in Java ?

    Java'da soyutlama (abstraction) ve çok biçimlilik (polymorphism), nesne yönelimli programlamada önemli kavramlardır, ancak farklı amaçlara hizmet ederler.

## Soyutlama (Abstraction):

- **Tanım**: Soyutlama, bir nesnenin implementasyon detaylarını gizleyip, yalnızca önemli özelliklerini gösterme kavramıdır. Bu, nesnenin ne yaptığını, nasıl yaptığına odaklanmayı sağlar.
- **Nasıl çalışır**: Soyutlama, soyut sınıflar veya arayüzler (interfaces) kullanılarak yapılır. Soyut sınıflar, gövdesiz (abstract) yöntemlere sahip olabilir ve bu yöntemler, alt sınıflar tarafından implement edilmelidir.

```java
abstract class Hayvan {  
    abstract void ses();  // soyut metod  
}  

class Kopek extends Hayvan {  
    void ses() {  
        System.out.println("Hav hav");  
    }  
}  
```

## Çok Biçimlilik (Polymorphism):

- **Tanım**: Polymorphism, "birçok şekil" anlamına gelir. Bu, nesnelerin, üst sınıflarının bir örneği olarak işlenebilmesini ve alt sınıflarda yeniden tanımlanmış metotların çağrılabilmesini sağlar.
- **Türleri**: Java'da polymorphism iki türde olabilir:  
    - Derleme Zamanı (Metod Aşırı Yükleme - Method Overloading): Aynı isimle birden fazla metodun farklı parametrelerle tanımlanması.  
    - Çalışma Zamanı (Metod Geçersiz Kılma - Method Overriding): Alt sınıfların, üst sınıflarındaki metodları kendi ihtiyacına göre değiştirmesi.

```java
class Hayvan {  
    void ses() {  
        System.out.println("Ses çıkarmıyor.");  
    }  
}  

class Kopek extends Hayvan {  
    @Override  
    void ses() {  
        System.out.println("Hav hav");  
    }  
}  

public class Test {  
    public static void main(String[] args) {  
        Hayvan h = new Kopek();  
        h.ses();  // Çıktı: Hav hav  
    }  
}  
```

Burada Kopek sınıfı, Hayvan sınıfındaki ses() metodunu geçersiz kılarak,
farklı bir davranış sergiler.
