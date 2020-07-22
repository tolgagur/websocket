Soket Nedir? 

Soketler, prosesler arası haberleşmede (IPC) kullanılan özel dosyalardır. Aynı makina üzerindeki veya ağ bağlantısına sahip farklı makinalardaki prosesler, birer uç noktası (endpoint) olarak tanımlanan soketler üzerinden, çift yönlü olarak, haberleşebilmektedir. 

Socket Programlama Nedir? 

Çevrim içi kullanıcıların buluştuğu bir platform oluşturdunuz ve kullanıcılar arası anlık mesajlaşma özelliği getireceğinizi varsayalım, bir kullanıcından diğer bir kullanıcıya mesaj gönderildiğinde sunucu tarafında bir değişiklik olur ve sunucu bunu istemciye bildiremez. Bu değişikliği algılayabilmek için polling, long polling ya da websocket gibi yapılar kullanılır. Polling belli aralıklarla sunucuya istek yapar, sunucu her isteğe bir cevap oluşturup gönderir ve bu çok fazla trafik yaratarak, bu da anlık konseptinin dışına çıkar. Long polling ise sunucuya isteği atar fakat sunucu tarafından cevap dönmesi için yeni bir istek yapılmasını bekler. Websocketler ise HTTP protokolüne uygun olmayan eş zamanlı web uygulamarındaki karmaşık yapının basitleştirilmesini sağlar.Websocket’ler polling’e göre daha az band genişliğine ihtiyaç duyar. Websocket ile kalıcı bir bağlantıyla oluşturduğumuz port üzerinden kullanıcılar arası iletişim portunu dinleyebilir ve anlık olarak kullanıcılar arası iletişimi ucuz ve hızlı yoldan halletmiş olursunuz. 

WebSocket Nedir? 

WebSocket, tek bir TCP bağlantısı üzerinden tam çift yönlü iletişim kanalı sağlayan bir bilgisayar iletişim protokolüdür. WebSocket, web tarayıcılarında ve web sunucularında uygulanmak üzere tasarlanmıştır, fakat herhangi bir istemci veya sunucu uygulaması tarafından uygulanabilmektedir. WebSocket protokolü, TCP tabanlı bağımsız bir protokoldür. HTTP ile tek ilişkisi, HTTP sunucuları tarafından bir Upgrade isteği olarak yorumlanmasıdır. WebSocket protokolü, sunucuya ve sunucudan gerçek zamanlı veri aktarımını sağlayarak, tarayıcı ile web sunucusu arasında etkileşimi sağlamaktadır. Bu, sunucunun istemci istemeden tarayıcıya içerik gönderebileceği ve bağlantıyı açık tutarak istediği zaman mesaj alabilmesini veya gönderebilmesini sağlayan standart bir yöntem ile sağlanmaktadır. Bu şekilde, tarayıcı ile sunucu arasında iki yönlü devam eden bir iletişim gerçekleşebilmektedir. İletişim TCP 80 portu (veya TLS ile şifrelenmiş bağlantılarda 443 portu) üzerinden gerçekleşmektedir ve bu, güvenlik duvarı kullanarak Internet web trafiğini engelleyen ortamlar için bir avantaj olmaktadır. 

 

Projede Kullanılan Teknolojiler 

-Spring Boot WebSocket 

-SockJS 

-Stomp 

Protokol:TCP/IP 

 

SockJS 

SockJS, WebSocket benzeri nesne sağlayan bir tarayıcı JavaScript kütüphanesidir. SockJS, tarayıcı ve web sunucusu arasında düşük gecikme süresi, tam çift yönlü, çapraz tarayıcı Javascript API'sı sağlar. SockJS, tüm modern tarayıcılarda ve WebSocket protokolünü desteklemeyen ortamlarda (örneğin, kısıtlayıcı şirket proxy'lerinin arkasında) çalışacak şekilde tasarlanmıştır. 

 

Stomp 

Eskiden TTMP olarak bilinen Basit Metin Odaklı Mesaj Protokolü, mesaj odaklı ara yazılım ile çalışmak için tasarlanmış basit bir metin tabanlı protokoldür. STOMP istemcilerinin protokolü destekleyen herhangi bir Message Broker ile konuşmalarını sağlayan birlikte çalışabilir bir kablo biçimi sağlar. 

 

TCP/IP 

İki veya daha fazla bilgisayarın birbiriyle haberleşmesi için belirli protokollere ihtiyaç vardır. TCP/IP,  günümüzde en yaygın olarak kullanılan protokol takımıdır ve TCP/IP protokol yığınına (TCP/IP stack) gömülü, İnternette veri aktarımı için kullanılan 2 protokolü temsil eder; Transmission Control Protocol (TCP) ve Internet Protocol (IP). 

İşleyişi (https://bidb.itu.edu.tr/seyir-defteri/blog/2013/09/07/tcp-ip-protokolu) 

 

 

 

Yapısı: 
![Örnek](https://hizliresim.com/RbFmAN)

API: WebSocket mesajların gönderilmesini sağlar. 

Request channel: İsteklerimizi gönderdiğimiz websockete client olduğumuz yerdir. Request channeli bir api üzerinden dinliyoruz (http method).  

Response channel: Sunucudan gelen mesajları aldığımız yer. 

Broker: Mesajların yönetildiği yerdir. Mesajları dağıtan bileşendir. 
