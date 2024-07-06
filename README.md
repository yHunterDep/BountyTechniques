# Mass XSS OneLiners
- Dalfox XSS<br>
`subfinder -d vulnweb.com | httpx | katana -ps | gf xss | qsreplace | anew | dalfox pipe --skip-bav`
