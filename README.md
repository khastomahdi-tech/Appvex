# VexClient

نسخه‌ی ۰.۳.۰: اتصال VPN با سرویس اندروید و هسته‌ی Xray.

## فعال‌سازی اتصال واقعی
1. فایل libv2ray.aar (هسته‌ی Xray برای اندروید) را در پوشه‌ی app/libs قرار بده.
2. در کد XrayCore.kt، نام کلاس‌ها و متدها را با نسخه‌ی AAR خودت تطبیق بده.
3. اجرای Build APK در GitHub Actions را بزن و APK را نصب کن.

اگر AAR نباشد، اپ کار می‌کند ولی اتصال انجام نمی‌شود و پیام روشن نمایش داده می‌شود.

## پروتکل‌ها
- VLESS (TCP، WebSocket، gRPC، HTTP، TLS، Reality)
- VMess (TCP، WebSocket، TLS)
- Trojan (TLS)
- Shadowsocks

Hysteria2 و TUIC در Xray نیستند و فعلاً پشتیبانی نمی‌شوند.

## ساخت APK با GitHub Actions
1. محتوای این پوشه را در یک مخزن GitHub آپلود کن.
2. (اختیاری) Secretهای KEYSTORE_BASE64، KEYSTORE_PASSWORD، KEY_ALIAS و KEY_PASSWORD را بساز.
3. از تب Actions، Build APK را اجرا کن و فایل را از Artifacts دانلود کن.
