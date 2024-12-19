**HAMZA CAN ALTINTOP-1220505072**<br>

**Kullanıcı Yönetim Sistemi (User Management System)** <br>
Bu proje, JavaFX kullanarak geliştirilmiş bir Kullanıcı Yönetim Sistemi'dir. Sistemde, adminler kullanıcı ekleyebilir. Kullanıcılar, sisteme giriş yapabilir ve notlarını yönetebilir. Her kullanıcı, belirli bir rol (admin, user, employee) ile sisteme erişim sağlar.

**Proje Hakkında** <br>
Bu sistem, kullanıcıların notlarını oluşturup düzenleyebileceği bir platform sunmaktadır. Ayrıca, adminler kullanıcı yönetimi işlemleri yapabilir. Sistemdeki önemli bileşenler şunlardır:<br>
**•	Admin Paneli:** Adminler kullanıcı ekleyebilir ve rolleri belirleyebilir.<br>
**•	Kullanıcı Girişi:** Kullanıcılar, e-posta ve şifre ile sisteme giriş yapar.<br>
**•	Not Yönetimi:** Kullanıcılar notlarını yönetebilir.<br>
**•	Kayıt Olma:** Yeni kullanıcılar kayıt olabilir.<br>

**Kullanım**<br>
Projede aşağıdaki ana işlevler bulunmaktadır:<br>

**1. Admin Paneli**<br>
Admin paneli, kullanıcı eklemeyi (admin, user ve employee roller seçebilmeyi) sağlar.<br>
**•	Kullanıcı Ekle:** Admin, yeni kullanıcılar ekleyebilir. Kullanıcı bilgileri (ad, e-posta, şifre, rol) belirtilerek kullanıcı eklenebilir.<br>
**•	Kullanıcı Listeleme:** Tüm kullanıcılar listelenebilir.<br>

**2. Kullanıcı Girişi**<br>
Kullanıcılar, e-posta ve şifre ile sisteme giriş yapabilir. Giriş başarılı olursa, kullanıcı rolüne bağlı olarak yetkilendirilir.<br>
**•	Admin:** Admin, herkesi yönetebilir.<br>
**•	Kullanıcı:** Kullanıcı, kendi notlarını yönetebilir.<br>
**•	Employee:** Employee, kullanıcı gibi işlem yapabilir, ancak admin yetkileri yoktur.<br>

**3. Not Yönetimi**<br>
Kullanıcılar, notlarını oluşturup düzenleyebilir. Notlar, iki durumda olabilir: aktif veya arşivlenmiş.<br>
**•	Not Ekle:** Kullanıcı, başlık, içerik, renk ve durum (aktif veya arşivlenmiş) ile not ekleyebilir.<br>
**•	Not Güncelleme:** Kullanıcılar mevcut notlarını güncelleyebilir.<br>
**•	Not Silme:** Notlar, kullanıcı rolüne bağlı olarak silinebilir.<br>

**4. Kayıt Olma**<br>
Yeni kullanıcılar, sisteme kayıt olabilirler. Kayıt olurken, e-posta ve şifre belirlerler.<br>

**Teknolojiler**<br>
Bu projede aşağıdaki teknolojiler ve araçlar kullanılmıştır:<br>
**•	JavaFX:** Kullanıcı arayüzü (UI) için.<br>
**•	FXML (isteğe bağlı):** JavaFX UI bileşenlerinin tanımlanması.<br>
**•	MVC Tasarımı:** Model-View-Controller (MVC) mimari deseni kullanılmıştır.<br>
**•	Strategy Pattern:** Not silme işlemi için kullanıcı rollerine göre farklı stratejiler uygulanmıştır.<br>

Bu proje, kullanıcı yönetimi ve not ekleme işlemleri için geliştirilmiş bir masaüstü Java uygulamasıdır. Uygulama, JavaFX kullanılarak GUI (Graphical User Interface) oluşturulmuş ve birkaç farklı tasarım deseni kullanılmıştır. Proje, Singleton, Factory, Strategy ,State tasarım desenlerini içerir ve Abstarct sınıfı ve CMV mimarisi kullanılmıştır.<br>

**İçindekiler**<br>

**1.	Proje Özeti**<br>
**2.	Tasarım Desenleri**<br>
**o	Singleton**<br>
**o	Factory**<br>
**o	Strategy**<br>
**o	Abstract**<br>
**o	State**<br>
**CMV Mimarisi ve abstract sınıflarda kullanılmıştır(NoteState ve AbstractNote).**
**3.	Veritabanı Bağlantısı**<br>
**4.	Uygulama Yapısı**<br>
**5.	Kullanıcı Arayüzü**<br>
**6.	Kullanım**<br>
**7.	Notlar**<br>

**Proje Özeti**<br>
Bu uygulama, kullanıcıların giriş yapabileceği, şifreleri ile doğrulama yapabileceği, yeni kullanıcılar ekleyebileceği, mevcut kullanıcıları listeleyebileceği ve notlar oluşturup yönetebileceği bir sistem sunar. Her kullanıcıya belirli bir rol atanır (admin, user, employee) ve her rolün farklı yetkileri vardır. Admin, kullanıcı ekleyebilir ve yönetebilir, user kendi notlarını ekleyip düzenleyebilir, employee ise yalnızca belirli işlemleri yapabilir.<br>


**Tasarım Desenleri**<br>
Bu projede kullanılan başlıca tasarım desenleri aşağıda açıklanmıştır:<br>
**Singleton Tasarım Deseni**<br>
**•	DatabaseConnection sınıfı**, veritabanı bağlantısını yönetir ve tek bir bağlantı örneği oluşturulmasını sağlar. Bu sayede her veritabanı işlemi için aynı bağlantı kullanılır, bu da kaynakların daha verimli yönetilmesine olanak tanır ve diğer yerlerden yapıcı metotla ulaşılır sadece.<br>
**Factory Tasarım Deseni**<br>
•	**AbstractNoteFactory deseni,** notların oluşturulmasını soyutlar ve farklı not türlerinin eklenmesini kolaylaştırır.<br>
•	**ConcreteNoteFactory,** belirli bir not türünü oluştururken, AbstractNoteFactory ise genel bir şablon sunar.<br>
**Strategy Tasarım Deseni**<br>
**•	DeleteStrategy sınıfı,** kullanıcının notları silme yetkisini belirler. Kullanıcı rolüne bağlı olarak farklı silme stratejileri uygulanır. Örneğin, user rolündeki bir kullanıcı tüm notları silebilirken, employee rolündeki kullanıcı silme yetkisine sahip değildir.<br>
**•	AdminDeleteStrategy, UserDeleteStrategy ve EmployeeDeleteStrategy sınıfları,** her bir kullanıcının silme işlemi üzerinde farklı haklara sahip olmasını sağlar.<br>

**State Tasarım Deseni**<br>
**•	NoteState sınıfı,** durum için temel bir yapı oluşturur,  notifyState() fonksiyonunun abstract  halini içerir.<br>
**•	ActiveNoteState sınıfı, notifyState()** fonksiyonuyla durum için temel bir yapı oluşturur.(aktif not)<br>
**•	InActiveNoteState sınıfı, notifyState()** fonksiyonuyla durum için temel bir yapı oluşturur.(arşivlenmiş not)<br>


**Veritabanı Bağlantısı**<br>
Projede **Singleton tasarım deseni** kullanılarak veritabanı bağlantısı yönetilmektedir. DatabaseConnection sınıfı, sadece tek bir bağlantı örneği oluşturulmasını sağlar ve bu örnek tüm uygulama boyunca kullanılır.<br>

**Uygulama Yapısı**<br>
Uygulama üç ana paketten **(CMV)** oluşmaktadır:<br>
**1.	Controller:** İş mantığı ve veritabanı işlemleri burada yönetilir.<br>
**2.	Model:** Notlar ve kullanıcıları temsil eden sınıflar burada yer alır.<br>
**3.	View:** Uygulamanın GUI kısmını oluşturan sınıflar burada bulunur.<br>

**Controller**<br>
**•	UserController sınıfı,** kullanıcı ekleme, listeleme, doğrulama ve kayıt işlemlerini yönetir.<br>
**•	NoteController sınıfı** ise notları ekler, günceller, listeler ve siler.<br>

**Model**<br>
**•	User sınıfı,** kullanıcıya ait bilgileri saklar.<br>
**•	ConcreteNote sınıfı,** bir notun özelliklerini temsil eder.<br>
**•	Note sınıfı,** soyut bir not şablonu sunar.<br>

**View**<br>
**•	LoginFrame:** Kullanıcıların sisteme giriş yapabilmesini sağlar.<br>
**•	RegisterFrame:** Yeni kullanıcı kaydı oluşturulabilir.<br>
**•	AdminView:** Admin paneli üzerinden kullanıcı ekleme yapılabilir.<br>
**•	NoteView:** Kullanıcıların notlarını görüntüleyebileceği ve yönetebileceği ekrandır.<br>

**Kullanıcı Arayüzü**<br>
Uygulamanın kullanıcı arayüzü **JavaFX** kullanılarak oluşturulmuştur. Temel ekranlar ve işlevler şunlardır:<br>
**1.	LoginFrame:** Kullanıcıların sisteme giriş yapmasını sağlar. Admin kullanıcıları ekleyebilir.<br>
**2.	RegisterFrame:** Yeni kullanıcıların sisteme kayıt olmasını sağlar.<br>
**3.	AdminView:** Admin paneli üzerinden kullanıcı yönetimi yapılabilir.<br>
**4.	NoteView:** Kullanıcıların notlarını ekleyebileceği, düzenleyebileceği ve silebileceği ekran.<br>

**Kullanım**<br>
**1.	Giriş Yap:** Sisteme kullanıcı adı ve şifre ile giriş yapabilirsiniz.<br>
**2.	Admin Ekle:** Giriş yaptıktan sonra admin olarak sisteme yeni admin kullanıcıları ekleyebilirsiniz.<br>
**3.	Not Ekle:** Sistemdeki kullanıcılar kendi notlarını ekleyebilir ve yönetebilir.<br>
**4.	Kullanıcı Yönetimi:** Admin, sisteme yeni kullanıcılar ekleyebilir ve mevcut kullanıcıları listeleyebilir.<br>

**Notlar**<br>
•	Veritabanı bağlantı bilgileri ve kullanıcı yönetim bilgileri, **UserController** ve **DatabaseConnection** sınıflarında saklanmaktadır.<br>
•	**Proje**, **Strategy**, **Factory**, **Singleton** ve **State** tasarım desenlerini kullanarak esnek ve sürdürülebilir bir yapıya sahiptir.<br>

Diğer Takım Arkadaşım:(https://github.com/HaticeFAKS)

