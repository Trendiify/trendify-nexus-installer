<div align="center">

# 🚀 Trendify Nexus Installer

### One-click Cloudflare deployment for Trendify Nexus

<p>
  <a href="#-english">
    <img src="https://img.shields.io/badge/🇬🇧%20English-1f2937?style=for-the-badge" alt="English">
  </a>
  <a href="#-فارسی">
    <img src="https://img.shields.io/badge/🇮🇷%20فارسی-1f2937?style=for-the-badge" alt="فارسی">
  </a>
</p>

<br>

<a href="https://Trendiify.github.io/trendify-nexus-installer/" target="_blank">
  <img src="https://img.shields.io/badge/🚀%20Open%20Trendify%20Nexus%20Installer-0f172a?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Open Installer">
</a>

<br><br>

**Automated Cloudflare deployment — no VPS required.**

</div>

---

<a id="-english"></a>

# 🇬🇧 English

## 📝 About

**Trendify Nexus Installer** is a lightweight web-based installer designed to deploy **Trendify Nexus** automatically on Cloudflare.

The goal of Version 1 is simple:

> Enter your Cloudflare API Token → Start Installation → Get your Trendify Nexus Dashboard.

No VPS, dedicated server, or manual database configuration is required for the initial deployment.

---

## ✨ Features

* 🚀 One-click Trendify Nexus installation
* ☁️ Cloudflare Workers deployment
* 🗄️ Automatic Cloudflare D1 database creation
* 🔗 Automatic D1 binding
* 🌐 Automatic `workers.dev` deployment
* 🔐 Automatic administrator initialization
* 🧩 Automatic Dashboard deployment
* ⚡ No VPS required
* 🛠️ No manual SQL setup
* 🔑 Cloudflare API Token used during installation

---

## 🚀 Open Installer

Click the button below to open the Installer in a new browser tab:

<div align="center">

<a href="https://YOUR-GITHUB-USERNAME.github.io/trendify-nexus-installer/" target="_blank">
  <img src="https://img.shields.io/badge/🚀%20OPEN%20INSTALLER-111827?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Open Installer">
</a>

</div>

---

## 🏗️ Architecture

```text
                    ┌──────────────────────┐
                    │  Trendify Installer  │
                    │       Web UI         │
                    └──────────┬───────────┘
                               │
                               │ Cloudflare API Token
                               ▼
                    ┌──────────────────────┐
                    │    Installer API     │
                    │   Cloudflare Worker  │
                    └──────────┬───────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
              ▼                ▼                ▼
        Cloudflare D1    Cloudflare Worker   workers.dev
              │                │                │
              └────────────────┴────────────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Trendify Nexus    │
                    │      Dashboard       │
                    └──────────────────────┘
```

After installation, the Dashboard can create and manage its own Gateway Workers.

The Installer does **not** create Gateway Workers.

---

## ⚙️ Installation Process

The Installer automatically performs the following steps:

```text
1. Verify Cloudflare Token
             ↓
2. Detect Cloudflare Account
             ↓
3. Create D1 Database
             ↓
4. Initialize Database Schema
             ↓
5. Create Administrator
             ↓
6. Deploy Trendify Nexus
             ↓
7. Bind D1 Database
             ↓
8. Enable workers.dev
             ↓
9. Return Dashboard URL
```

---

## 🔑 Cloudflare API Token

Create a Cloudflare API Token with:

```text
Account Settings → Read
D1 → Edit
Workers Scripts → Edit
```

For Version 1, no custom domain is required.

The Dashboard is deployed using Cloudflare `workers.dev`.

---

## 🔐 Default Login

A fresh installation automatically creates:

```text
Username: admin
Password: admin
```

⚠️ **Change the default password immediately after your first login.**

---

## 🌐 Gateway Architecture

Gateways are created from inside the Trendify Nexus Dashboard.

```text
Trendify Nexus
      │
      ▼
   Gateways
      │
      ▼
Create Gateway
      │
      ▼
Gateway Worker
      │
      ▼
 Cloudflare
```

The Installer is responsible only for the initial Trendify Nexus deployment.

---

## 🗄️ Database

The Installer automatically creates and initializes a Cloudflare D1 database.

The Dashboard uses:

```text
D1 Binding: DB
```

No manual SQL commands are required during a fresh installation.

---

## 🔒 Security

Never commit sensitive information to this repository.

Do not publish:

* Cloudflare API Tokens
* API Keys
* Worker Secrets
* Database credentials
* Session tokens
* Private credentials

Each user should create and manage their own Cloudflare API Token.

---

## 📦 Version 1

### Current Release

**Trendify Nexus Installer — V1**

Version 1 focuses on a simple and reliable automated installation process.

### V1 includes

* Cloudflare account detection
* Automatic D1 creation
* Automatic database initialization
* Automatic admin creation
* Dashboard deployment
* D1 binding
* `workers.dev` support
* No VPS requirement
* No manual SQL configuration

---

## 🛣️ Roadmap

Future releases may include:

* 🌐 Custom domain deployment
* ⚙️ Advanced installation settings
* 🔄 Upgrade and migration system
* 📊 Deployment diagnostics
* 📦 Version management
* ☁️ Additional Cloudflare configuration

---

## 🤝 Contributing

Bug reports, suggestions, improvements, and Pull Requests are welcome.

Before submitting changes:

1. Never commit secrets.
2. Test the Installer on a fresh Cloudflare account.
3. Verify D1 creation.
4. Verify Dashboard deployment.
5. Verify administrator login.
6. Document architectural changes.

---

<a id="-فارسی"></a>

# 🇮🇷 فارسی

## 📝 معرفی

**Trendify Nexus Installer** یک Installer تحت وب برای نصب و راه‌اندازی خودکار **Trendify Nexus** روی Cloudflare است.

هدف نسخه اول این پروژه این است که کاربر فقط با وارد کردن **Cloudflare API Token** بتواند کل سیستم را به صورت خودکار راه‌اندازی کند.

یعنی:

```text
Cloudflare Token
       ↓
Start Installation
       ↓
ساخت Database
       ↓
ساخت Admin
       ↓
Deploy پنل
       ↓
دریافت آدرس پنل
```

بدون نیاز به VPS، سرور اختصاصی یا تنظیم دستی Database.

---

## 🚀 باز کردن Installer

برای اجرای Installer روی دکمه زیر کلیک کنید:

<div align="center">

<a href="https://YOUR-GITHUB-USERNAME.github.io/trendify-nexus-installer/" target="_blank">
  <img src="https://img.shields.io/badge/🚀%20باز%20کردن%20Trendify%20Nexus%20Installer-111827?style=for-the-badge&logo=cloudflare&logoColor=white" alt="باز کردن Installer">
</a>

</div>

این دکمه Installer را در یک **تب جدید مرورگر** باز می‌کند.

---

## ⚙️ روند نصب

Installer به صورت خودکار این مراحل را انجام می‌دهد:

```text
بررسی Cloudflare Token
        ↓
تشخیص Account
        ↓
ساخت D1 Database
        ↓
ساخت جداول Database
        ↓
ساخت Admin
        ↓
Deploy پنل Trendify Nexus
        ↓
اتصال D1
        ↓
فعال‌سازی workers.dev
        ↓
نمایش آدرس پنل
```

---

## ✨ امکانات

* 🚀 نصب خودکار Trendify Nexus
* ☁️ اجرای کامل روی Cloudflare
* 🗄️ ساخت خودکار D1
* 🔗 اتصال خودکار D1 به Worker
* 🌐 استفاده از `workers.dev`
* 🔐 ساخت خودکار Administrator
* 🧩 Deploy خودکار Dashboard
* ⚡ بدون نیاز به VPS
* 🛠️ بدون نیاز به اجرای دستی SQL
* 🔑 استفاده از Cloudflare API Token در زمان نصب

---

## 🔑 دسترسی Cloudflare

API Token باید حداقل این دسترسی‌ها را داشته باشد:

```text
Account Settings → Read
D1 → Edit
Workers Scripts → Edit
```

در نسخه اول نیازی به Custom Domain نیست.

---

## 🔐 ورود اولیه

بعد از نصب، حساب Administrator به صورت خودکار ساخته می‌شود:

```text
نام کاربری: admin
رمز عبور: admin
```

⚠️ **بعد از اولین ورود حتماً رمز عبور را تغییر دهید.**

---

## 🌐 Gateway

Gateway از طریق خود Dashboard ساخته می‌شود.

```text
Trendify Nexus
      ↓
Gateways
      ↓
Create Gateway
      ↓
Gateway Worker
```

Installer مسئول ساخت Gateway نیست و فقط نصب اولیه Dashboard و Database را انجام می‌دهد.

---

## 🗄️ دیتابیس

Installer به صورت خودکار Cloudflare D1 را ایجاد کرده و جداول مورد نیاز را آماده می‌کند.

Binding اصلی Dashboard:

```text
DB
```

بنابراین برای نصب جدید نیازی به اجرای دستی SQL نیست.

---

## 🔒 امنیت

هرگز اطلاعات حساس را داخل GitHub قرار ندهید.

موارد زیر نباید داخل Repository قرار بگیرند:

```text
Cloudflare API Token
API Keys
Worker Secrets
Database Credentials
Session Tokens
Private Credentials
```

هر کاربر باید API Token مربوط به Cloudflare خودش را بسازد.

---

## 📦 نسخه اول

**Trendify Nexus Installer — Version 1**

تمرکز V1 روی یک فرآیند نصب ساده و قابل اعتماد است.

```text
Token
 ↓
Cloudflare
 ↓
D1
 ↓
Admin
 ↓
Dashboard
 ↓
workers.dev
```

---

## 🛣️ نسخه‌های آینده

امکانات احتمالی نسخه‌های آینده:

* 🌐 Custom Domain
* ⚙️ تنظیمات پیشرفته Installer
* 🔄 Upgrade و Migration
* 📊 گزارش خطا و وضعیت نصب
* 📦 مدیریت Version
* ☁️ امکانات بیشتر Cloudflare

---

## ❤️ Trendify Nexus

**نصب خودکار، سریع و بدون نیاز به VPS.**

<div align="center">

**Made for Trendify Nexus**

</div>
