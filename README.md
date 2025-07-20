````markdown path=README.md mode=EDIT
# 🍪 F12 Cookie Extractor

A comprehensive guide to extracting session cookies from social media platforms for authentication purposes.

---

## 🎯 Overview

This tool helps you extract session cookies from various social media platforms including **Instagram**, **Zalo**, and others. These cookies are essential for API authentication and automated interactions.

---

## 🔑 Authentication Requirements

To interact with social media platforms, you need valid session cookies. Below are two reliable methods to obtain them.

---

## 📋 Supported Platforms

| Platform | Login URL | Notes |
|----------|-----------|-------|
| **Instagram** | [instagram.com](https://www.instagram.com) | Most common use case |
| **Zalo** | [zalo.me/pc](https://zalo.me/pc) | Vietnamese social platform |

---

## 🛠️ Method 1: Console Cookie Extraction

### Step-by-Step Instructions

1. **Navigate to Platform**
   - **Instagram**: Go to [instagram.com](https://www.instagram.com)
   - **Zalo**: Go to [zalo.me/pc](https://zalo.me/pc) or [id.zalo.me login](https://id.zalo.me/account/login?continue=https%3A%2F%2Fzalo.me%2Fpc)

2. **Login to Your Account**
   - Complete the login process normally

3. **Open Developer Tools**
   ```
   Chrome/Edge: F12 or Ctrl+Shift+I (Cmd+Opt+I on Mac)
   Firefox:     F12 or Ctrl+Shift+I
   Safari:      Cmd+Opt+I
   ```

4. **Access Console Tab**
   - Click on the **Console** tab in Developer Tools

5. **Extract Cookies**
   ```javascript
   console.log(document.cookie);
   ```
   - Copy and paste the command above
   - Press **Enter** to execute

### Expected Output Examples

**Instagram Cookies:**
```
datr=abc123def456; ig_did=xyz789; csrftoken=token123; sessionid=987654321%3Aabcdef%3A12%3Aabcxyz; rur=NAO
```

**Zalo Cookies:**
```
_zlang=vn; app.event.zalo.me=value123; zpsid=session456; zpw_sek=token789; _ga=GA1.2.123456789
```

---

## 🌐 Method 2: Network Tab Extraction

### Step-by-Step Instructions

1. **Login to Platform**
   - **Instagram**: [instagram.com](https://www.instagram.com)
   - **Zalo**: [zalo.me/pc](https://zalo.me/pc)

2. **Open Developer Tools**
   - Use the same shortcuts as Method 1

3. **Navigate to Network Tab**
   - Click on **Network** tab
   - Refresh the page (`F5` or `Ctrl+R`)

4. **Find API Requests**
   - **Instagram**: Look for `www.instagram.com/api/v1/...`
   - **Zalo**: Look for `zalo.me/api/...` or `id.zalo.me/...`

5. **Extract Cookie Header**
   - Click on any API request
   - Find **Request Headers** section
   - Copy the entire **Cookie** header value

### Expected Cookie Headers

**Instagram Format:**
```
Cookie: datr=...; ig_did=...; csrftoken=...; sessionid=...; rur=...
```

**Zalo Format:**
```
Cookie: _zlang=...; zpsid=...; zpw_sek=...; _ga=...
```

---

## ⚠️ Important Notes

- 🔒 **Keep cookies secure** - Never share them publicly
- ⏰ **Cookies expire** - You may need to refresh them periodically
- 🌍 **Platform-specific** - Each platform has different cookie formats
- 🔄 **Session validity** - Logging out will invalidate cookies

---

## 🚀 Usage

Once you have extracted the cookies, use them as your `--cookies` parameter in your applications:

```bash
your-app --cookies "datr=...; sessionid=...; csrftoken=..."
```

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🤝 Contributing

Pull requests are welcome! If you find bugs or want to add features:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

---

## 💡 Support

If you encounter issues or need help:
- Check the troubleshooting section
- Open an issue on GitHub
- Contribute improvements

---

**🎉 Happy cookie extracting!** 

*Built with ❤️ for developers*

---

*σΔγ*
````
