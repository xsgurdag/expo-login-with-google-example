# expo-login-with-google-example

Projeyi sağlıklı şekilde ayağa kaldırmak için aşağıdaki adımlar sırası ile izlenmelidir:
1. Oluşturulan projede "eas build -p android" komutu ile expo.dev'de projenizin build'ini oluşturun. Bu işlem aynı zamanda Expo projenizde android dosya dizininin görünür olmasını da sağlayacaktır. ( Bu işlemi "eas build -p ios" olarak da ios cihazlar için yapabilirsiniz." 
2. Build işlemi tamamlanırken consolda com.example.myapp benzeri bir Package name göreceksiniz bu Google entegrasyonu için önemli. Bu Package Name'i not almanızda fayda var.
3. Daha sonrasında "eas update --branch [branch name]" komutu ile expo.dev ortamında branch'inizi oluşturun.
4. Konsolda "eas credentials -p android" komutunu çalıştırın. Bu alanda 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/30cb1c93-5da7-499d-95fa-c9ac678fb050) 

gibi bir soru ile karşılaşacaksınız burada hangi profile ile devam edeceğinizi expo.dev'de projenizin sayfasına girerek oluşan build'in hangi profilde oluştuğuna bağlı olarak seçebilirsiniz. 
![image](https://github.com/xsgurdag/expo-login-with-google-example/assets/117263107/d26d9247-2185-4b95-b3f1-9c4fb7be5ed3)


