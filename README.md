
## **🔑 Required Authentication - How to Get Cookies**

To use `instagram`, you need Instagram session cookies. Choose the method that suits you best. I generally go with the first.

### **📌 Method 1: Using `document.cookie` in the Console**

1. Open **Instagram** ([https://www.instagram.com](https://www.instagram.com)) and log in.
2. Open **Developer Tools**:
   - **Chrome**: Press `F12` or `Ctrl + Shift + I` (`Cmd + Opt + I` on Mac).
   - **Firefox**: Press `F12` or `Ctrl + Shift + I`.
3. Click on the **Console** tab.
4. Copy and paste this command, then press **Enter**:

   ```js
   console.log(document.cookie);
   ```

5. The output will show all your cookies:

   ```sh
   datr=abc123; ig_did=xyz456; csrftoken=token123; sessionid=987654321%3Aabcdef%3A12%3Aabcxyz;
   ```

### **📌 Method 2: Open Instagram on Your Browser**

1. Log in to [Instagram](https://www.instagram.com/).
2. Open **Developer Tools**:
   - Chrome: Press `F12` or `Ctrl + Shift + I` (`Cmd + Opt + I` on Mac).
   - Firefox: Press `F12` or `Ctrl + Shift + I`.
3. Go to the **Network** tab and refresh the page.
4. Look for a request to `www.instagram.com/api/v1/...`
5. Copy the **Cookies** header. It should contain values like:

   ```sh
   datr=...; ig_did=...; csrftoken=...; sessionid=...
   ```

6. Use this string as your `--cookies` value.

---


## **📜 License**

This project is licensed under the **MIT License**.

---

## **🙌 Contributing**

Pull requests are welcome! If you find a bug or want to add features, feel free to contribute.

🚀 **Enjoy using `f12-cookie`!** Let me know if you need any modifications! 🚀

---

σΔγ
