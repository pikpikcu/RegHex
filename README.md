# RegHex

RegHex is a collection of regexes for every use.

Usage (personal preference): `grep -Proh "$REGEX" . | sort -u > result_file`

# Table of Contents

- [AWS Client ID](https://github.com/0x41CoreDump/RegHex#AWS-Client-ID)
- [AWS MWS Key](https://github.com/0x41CoreDump/RegHex#AWS-MWS-Key)
- [AWS Secret Key](https://github.com/0x41CoreDump/RegHex#AWS-Secret-Key)
- [Base32](https://github.com/0x41CoreDump/RegHex#Base32)
- [Base64](https://github.com/0x41CoreDump/RegHex#Base64)
- [Facebook Access Token](https://github.com/0x41CoreDump/RegHex#Facebook-Access-Token)
- [Facebook Client ID](https://github.com/0x41CoreDump/RegHex#Facebook-Client-ID)
- [Facebook Secret Key](https://github.com/0x41CoreDump/RegHex#Facebook-Secret-Key)
- [Github](https://github.com/0x41CoreDump/RegHex#Github)
- [Google API Key](https://github.com/0x41CoreDump/RegHex#Google-API-Key)
- [Google Cloud Platform API Key](https://github.com/0x41CoreDump/RegHex#Google-Cloud-Platfrom-API-Key)
- [Google Oauth](https://github.com/0x41CoreDump/RegHex#Google-Oauth)
- [IPv4](https://github.com/0x41CoreDump/RegHex#IPv4)
- [IPv6](https://github.com/0x41CoreDump/RegHex#IPv6)
- [Javascript Variables](https://github.com/0x41CoreDump/RegHex#Javascript-Variables)
- [LinkedIn Client ID](https://github.com/0x41CoreDump/RegHex#LinkedIn-Client-ID)
- [LinkedIn Secret Key](https://github.com/0x41CoreDump/RegHex#LinkedIn-Secret-Key)
- [Slack](https://github.com/0x41CoreDump/RegHex#Slack)
- [Twitter Client ID](https://github.com/0x41CoreDump/RegHex#Twitter-Client-ID)
- [Twitter Secret Key](https://github.com/0x41CoreDump/RegHex#Twitter-Secret-Key)
- [URL Parameter](https://github.com/0x41CoreDump/RegHex#URL-Parameter)
- [URLs](https://github.com/0x41CoreDump/RegHex#URLs)
- [Credits](https://github.com/0x41CoreDump/RegHex#Credits)

### AWS Client ID
```
(A3T[A-Z0-9]|AKIA|AGPA|AIDA|AROA|AIPA|ANPA|ANVA|ASIA)[A-Z0-9]{16}
```

### AWS MWS Key
```
amzn\.mws\.[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}
```

### AWS Secret Key
```
(?i)aws(.{0,20})?(?-i)['\"][0-9a-zA-Z\/+]{40}['\"]
```

### Base32
```
(?:[A-Z2-7]{8})*(?:[A-Z2-7]{2}={6}|[A-Z2-7]{4}={4}|[A-Z2-7]{5}={3}|[A-Z2-7]{7}=)?
```

### Base64
```
(eyJ|YTo|Tzo|PD[89]|aHR0cHM6L|aHR0cDo|rO0)[a-zA-Z0-9+/]+={0,2}
```

### Facebook Access Token
```
EAACEdEose0cBA[0-9A-Za-z]+
```

### Facebook Client ID
```
(?i)(facebook|fb)(.{0,20})?['\"][0-9]{13,17}
```

### Facebook Secret Key
```
(?i)(facebook|fb)(.{0,20})?(?-i)['\"][0-9a-f]{32}
```

### Github
```
(?i)github(.{0,20})?(?-i)['\"][0-9a-zA-Z]{35,40}
```

### Google API Key
```
AIza[0-9A-Za-z\\-_]{35}
```

### Google Cloud Platform API Key
```
(?i)(google|gcp|youtube|drive|yt)(.{0,20})?['\"][AIza[0-9a-z\\-_]{35}]['\"]
```

### Google Oauth
```
(?i)(google|gcp|auth)(.{0,20})?['"][0-9]+-[0-9a-z_]{32}\.apps\.googleusercontent\.com['"]
```

### IPv4
```
\b(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)(\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)){3}\b
```

### IPv6
```
(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))
```

### Javascript Variables
```
(?:const|let|var)\s+\K(\w+?)(?=[;.=\s])
```

### LinkedIn Client ID
```
(?i)linkedin(.{0,20})?(?-i)['\"][0-9a-z]{12}['\"]
```

### LinkedIn Secret Key
```
(?i)linkedin(.{0,20})?['\"][0-9a-z]{16}['\"]
```

### Slack
```
xox[baprs]-([0-9a-zA-Z]{10,48})?
```

### Twitter Client ID
```
(?i)twitter(.{0,20})?['\"][0-9a-z]{18,25}
```

### Twitter Secret Key
```
(?i)twitter(.{0,20})?['\"][0-9a-z]{35,44}
```

### URL Parameter
```
(?<=\?|\&)[a-zA-Z0-9_]+(?=\=)
```

### URLs
With HTTP Protocol:
```
https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)
```
Without Protocol: 
```
[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)
```

# Credits
- [TomNomNom](https://github.com/tomnomnom) and his repo [gf](https://github.com/tomnomnom/gf)
- [gitleaks](https://github.com/zricethezav/gitleaks)
- https://stackoverflow.com/questions/53497/regular-expression-that-matches-valid-ipv6-addresses
- https://stackoverflow.com/questions/3809401/what-is-a-good-regular-expression-to-match-a-url
- https://stackoverflow.com/questions/44654809/regex-to-match-ip-addresses

