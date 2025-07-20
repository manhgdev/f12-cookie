````markdown path=/Users/manhg/DEV/API/REAME/f12-cookie/README.md mode=EDIT
## **🔑 Required Authentication - How to Get Cookies**

To use social media platforms like `Instagram`, `Zalo`, and others, you need session cookies. Choose the method that suits you best. I generally go with the first.

### **📌 Method 1: Using `document.cookie` in the Console**

1. Open your target platform and log in:
   - **Instagram**: [https://www.instagram.com](https://www.instagram.com)
   - **Zalo**: [https://zalo.me/pc](https://zalo.me/pc) or [https://id.zalo.me/account/login?continue=https%3A%2F%2Fzalo.me%2Fpc](https://id.zalo.me/account/login?continue=https%3A%2F%2Fzalo.me%2Fpc)
2. Open **Developer Tools**:
   - **Chrome**: Press `F12` or `Ctrl + Shift + I` (`Cmd + Opt + I` on Mac).
   - **Firefox**: Press `F12` or `Ctrl + Shift + I`.
3. Click on the **Console** tab.
4. Copy and paste this command, then press **Enter**:

   ```js
   console.log(document.cookie);
   ```

5. The output will show all your cookies:

   **Instagram example:**
   ```sh
   datr=abc123; ig_did=xyz456; csrftoken=token123; sessionid=987654321%3Aabcdef%3A12%3Aabcxyz;
   ```

   **Zalo example:**
   ```sh
   _zlang=vn; app.event.zalo.me=value123; zpsid=session456; zpw_sek=token789;
   ```

### **📌 Method 2: Using Network Tab**

1. Log in to your target platform:
   - [Instagram](https://www.instagram.com/)
   - [Zalo](https://zalo.me/pc)
2. Open **Developer Tools**:
   - Chrome: Press `F12` or `Ctrl + Shift + I` (`Cmd + Opt + I` on Mac).
   - Firefox: Press `F12` or `Ctrl + Shift + I`.
3. Go to the **Network** tab and refresh the page.
4. Look for API requests:
   - **Instagram**: `www.instagram.com/api/v1/...`
   - **Zalo**: `zalo.me/api/...` or `id.zalo.me/...`
5. Copy the **Cookies** header. It should contain values like:

   **Instagram:**
   ```sh
   datr=...; ig_did=...; csrftoken=...; sessionid=...
   ```

   **Zalo:**
   ```sh
   _zlang=...; zpsid=...; zpw_sek=...
   ```

6. Use this string as your `--cookies` value.
````
