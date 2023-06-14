### How to Use ###

1. Buat icon di lokasi ini:
```
android/app/src/main/res/drawable/app_icon.png
```

Atau gunakan saja dengan perintah ini:
```
curl https://icons.iconarchive.com/icons/mattahan/ultrabuuf/128/Comics-Ironman-Red-icon.png -o android/app/src/main/res/drawable/app_icon.png
```

2. Di main.dart, tambahkan kode ini:
```
void main () async {
    WidgetsFlutterBinding.ensureInitialized();
    await NotificationService.instance.init(); // this code
    runApp(const MyApp());
}
```

3. Untuk menampilkan notifikasi, cukup panggil kode ini.
```
NotificationService.instance.showNotification(
    title: "Test Notifications",
    body: "Hello bro",
)
```