# Reflected-cross-site-scripting-XSS-in-the-Smart-Form
## 
## Severity: Medium
## Product: Smart Form - WordPress Plugin (https://wordpress.org/plugins/smart-forms/)
##
## POC:
Perform an edit on a form.
<img width="1385" height="546" alt="ảnh" src="https://github.com/user-attachments/assets/067b2b35-2445-45d6-bf98-560bcd5d9619" />
Then save the form and intercept the request with Burp Suite.
<img width="1480" height="811" alt="{B24AE119-90AA-4AB9-A346-31EC0CB66EC3}" src="https://github.com/user-attachments/assets/ddc5d35e-8d6f-45eb-a57a-2c1706a7140b" />
Inject the JavaScript payload <img src=x onerror=alert('XSS')> into the id parameter and send the request.
<img width="1471" height="697" alt="{40C9CD98-2B1C-4FB7-A54A-097B67713817}" src="https://github.com/user-attachments/assets/511e3c2e-df83-4836-963a-c3aa7833bf48" />
View the request in the browser and observe that the injected JavaScript is executed.
<img width="1640" height="529" alt="{CA92F728-725B-4792-9E24-6CBDE61A7928}" src="https://github.com/user-attachments/assets/d7a6c2d0-2c73-40cd-8e6a-ab922464510b" />




