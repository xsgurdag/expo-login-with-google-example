# expo-login-with-google-example

Projeyi sağlıklı şekilde ayağa kaldırmak için aşağıdaki adımlar sırası ile izlenmelidir:
1. Oluşturulan projede "eas build -p android" komutu ile expo.dev'de projenizin build'ini oluşturun. Bu işlem aynı zamanda Expo projenizde android dosya dizininin görünür olmasını da sağlayacaktır. ( Bu işlemi "eas build -p ios" olarak da ios cihazlar için yapabilirsiniz." 

2. Build işlemi tamamlanırken consolda com.example.myapp benzeri bir Package name göreceksiniz bu Google entegrasyonu için önemli. Bu Package Name'i not almanızda fayda var.

3. Daha sonrasında "eas update --branch [branch name]" komutu ile expo.dev ortamında branch'inizi oluşturun.

4. (Not: Bu kısım Android projeleri içindir, android platformuna uygulama geliştirmeyecekseniz bu adımı atlayabilirsiniz.) Konsolda "eas credentials -p android" komutunu çalıştırın. Bu alanda 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/30cb1c93-5da7-499d-95fa-c9ac678fb050) 

gibi bir soru ile karşılaşacaksınız burada hangi profile ile devam edeceğinizi expo.dev'de projenizin sayfasına girerek oluşan build'in hangi profilde oluştuğuna bağlı olarak seçebilirsiniz. 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/d26d9247-2185-4b95-b3f1-9c4fb7be5ed3)
 
 Uygun olan profil seçiminde sonra kaşınıza böyle bir bilgilendirme gelmeli. Bu alandaki SHA1 Fingerprint bizim için önemli olan veri, not alabilirsiniz.
 ![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/f4624f27-0700-481f-800d-d6346055f533)

5. Google Cloud Console'da New Project diyerek projenizi aşağıdaki gibi oluşturun.
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/a921eb2e-eff1-4ecd-83d9-18e75590c1df)

6. Creadential bölümünden "Create Credentials", ardından "OAuth client ID" bölümüne gelin. 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/6e773011-4894-43fb-97ca-b0f82a6faec7)

7. !!! Bu kısımda Expo'nun Login with Google dokumanında belirtilmeyen bir işlemin yapılması gerekiyor. Application Type alanından "Web Application" seçeneğini seçin. Ardından Authorized JavaScript origins
alanını "https://auth.expo.io" ve Authorized redirect URIs alanını "https://auth.expo.io/@[Owner]/[Slug]" şeklinde doldurun. Owner ve Slug bilgilerinizi Expo.dev'de projenizin sayfasında aşağıdaki gibi görebilirsiniz. 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/7cd60ba7-d69d-4346-a82d-c5b5a0d796ef)

8. Daha sonrasında save'i seçip oluşan Client ID'yi kopyalayın. Burada oluşan Client ID, expoClientId alanı içindir. Örnek projede App.js dosyasında expoClientId'nin karşılığına bu bilgiyi yapıştırabilirsiniz.

9. Ardından 6. seçenekteki işlemi tekrarlayın ve Application Type alanından "Android" seçeneğini seçerek devam edin. (Burada oluşturmak istediğiniz projenin platformuna göre IOS ya da Web Application seçenekleri ile de devam edebilirsiniz.) 

10. Gelen ekranda daha önceden tespit etmiş olduğumuz SHA1 ve Package Name bilgilerini kullanarak uygun alanları doldurun ardından Save tuşu ile devam edin. 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/91de4a69-5251-4ad5-9ea4-87fda3090993)

11. Daha sonrasında oluşan Client ID'yi kopyalayıp örnek projedeki uygun alana yapıştırın (Android için androidClientId, IOS için iosClientId ve web için webClientId)

12. Bu işlemlerden sonra örnek projenizi kullanmaya başlayabilirsiniz. 






