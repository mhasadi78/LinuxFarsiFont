# LinuxFarsiFont

A fontconfig XML configuration to improve Persian (Farsi) and Arabic font
rendering on Linux desktops by aliasing the **Sahel** font as the default
for sans-serif, system-ui, Persian, and Arabic text.

## How it works

Fontconfig lets users override system fonts by placing XML rules in
`~/.config/fontconfig/conf.d/`. This file (`10-sahel.conf`) does four things:

1. Prefers Sahel for `sans-serif`, `sans`, and `system-ui` families.
2. Forces Sahel whenever the text language is Persian (`fa`) or Arabic
   (`ar`) — strong binding, so it overrides most application settings.
3. Appends Sahel as a universal fallback for every font request.
4. Enables `hintslight` hinting and antialiasing for better on-screen
   rendering.

## Prerequisites

Install the **Sahel** font on your system. It is available in most distro
package repositories and also from [Designer's Website](https://rastikerdar.github.io/sahel-font/).

If you prefer a different font, edit every `<string>Sahel</string>` line
in `10-sahel.conf` before installing.

## Installation

```sh
cp 10-sahel.conf "$HOME/.config/fontconfig/conf.d/10-sahel.conf"
fc-cache --force
```

For the changes to take full effect, **log out and log back in** (or
restart your desktop environment).

## License

GNU General Public License v3.0 — see [LICENSE](LICENSE).

---

## راهنمای فارسی

### معرفی

یک تنظیمات fontconfig برای بهبود نمایش فونت‌های فارسی و عربی در محیط
دسکتاپ لینوکس. این تنظیمات فونت **ساحل (Sahel)** را به‌عنوان قلم پیش‌فرض
برای متن‌های sans-serif، system-ui، فارسی و عربی انتخاب می‌کند.

### کارایی

فایل `10-sahel.conf` این کارها را انجام می‌دهد:

1. اولویت دادن به فونت ساحل برای خانواده‌های `sans-serif`، `sans` و
   `system-ui`.
2. اجبار فونت ساحل برای متن‌هایی با زبان فارسی (`fa`) یا عربی (`ar`) —
   این تنظیم قوی (strong binding) است و در بیشتر نرم‌افزارها اعمال می‌شود.
3. اضافه کردن فونت ساحل به‌عنوان پشتیبان (fallback) برای تمام درخواست‌های
   فونت.
4. فعال‌سازی `hintslight` و `antialias` برای نمایش بهتر روی صفحه.

### پیش‌نیازها

فونت **ساحل** باید روی سیستم شما نصب باشد. می‌توانید آن را از مخزن
پکیج‌های توزیع لینوکس خود یا از
[وبسایت سازنده](https://rastikerdar.github.io/sahel-font/) دریافت کنید.

اگر می‌خواهید از فونت دیگری استفاده کنید، قبل از نصب، تمام خطوط
`<string>Sahel</string>` در فایل `10-sahel.conf` را به نام فونت دلخواه
خود تغییر دهید.

### نصب

```sh
cp 10-sahel.conf "$HOME/.config/fontconfig/conf.d/10-sahel.conf"
fc-cache --force
```

برای اعمال کامل تغییرات، از سیستم **خارج شده و دوباره وارد شوید** (یا
محیط دسکتاپ خود را restart کنید).

### مجوز

جی‌ن‌یو جی‌پی‌ال نسخه ۳ — فایل [LICENSE](LICENSE) را ببینید.
