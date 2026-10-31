ICON APK (anti putih-putih / anti kepotong)

KENAPA ICON KEPOTONG/ADA FRAME PUTIH?
File icon di zip ini sudah full (tanpa transparan, tanpa putih). Frame putih muncul kalau APK-nya
TIDAK punya adaptive icon -> Android membungkus icon lama (legacy) dalam kotak putih dan mengecilkannya.
Jadi yang harus dibenerin ada di project/builder APK, bukan di website.

CARA PAKAI (project Android Studio / WebView)
1. Copy isi folder android-res/ ke app/src/main/res/ (timpa file lama).
   Wajib ada: mipmap-anydpi-v26/ic_launcher.xml + ic_launcher_round.xml  <- ini adaptive icon-nya.
2. AndroidManifest: android:icon="@mipmap/ic_launcher" android:roundIcon="@mipmap/ic_launcher_round"
3. Hapus ic_launcher lama di mipmap-* / drawable lain kalau ada (supaya tidak bentrok).
4. Uninstall APK lama di HP, install ulang (launcher nyimpan icon lama).

KALAU PAKAI BUILDER ONLINE (website2apk, dsb)
- Upload apk-icon-1024.png sebagai icon.
- Kalau ada opsi "Adaptive icon": foreground = apk-adaptive-foreground-432.png,
  background = apk-adaptive-background-432.png (atau warna solid #081438).
- Kalau builder cuma menerima 1 gambar, ukuran/frame-nya dibuat builder -> frame putih bisa tetap ada.

Foreground sudah diperkecil ke zona aman (logo ga kepotong mask bulat/squircle) dan latarnya navy #081438.
