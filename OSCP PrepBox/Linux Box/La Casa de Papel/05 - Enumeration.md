# Nmap

```bash
PORT    STATE SERVICE  VERSION                                                                                                                                                        [22/145]
21/tcp  open  ftp      vsftpd 2.3.4                                                            
22/tcp  open  ssh      OpenSSH 7.9 (protocol 2.0)                 
| ssh-hostkey:                                                                                 
|   2048 03:e1:c2:c9:79:1c:a6:6b:51:34:8d:7a:c3:c7:c8:50 (RSA)    
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDNzmarvyIINA+hjsLo2xYn1PUyzuTflhtXQs8S1Z56FzbdzXs6FiwhoRGn63XuGCHqCfEzHmh1cg4HGLfGAMwe+AsdJ8hLd/ISNRECH8yvM+9k78Aio3pe+lYbiWSQWyJrQdeqJXyDJFSd6BR3Cr6/
rwSvE7N3eWeQvxS+fsg5HOER6n8SOnXvqpWYUo+XmZxGzmluNfsqoJ6doJCyW3X4sTImTlpmRmee6iseo9neZO18aHsARxlkHCqUhp1SBzIiik3DurtH1tgrn8ntfNiK3q0FZJmh9qzu0P/L50j8bzlJdvAsLuqbYmVZhqFs0JfBVdyVTFMn4O0J+IqRrX
AF                                                                                             
|   256 41:e4:95:a3:39:0b:25:f9:da:de:be:6a:dc:59:48:6d (ECDSA)   
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBNli8Xx10a0s+zrkT1eVfM1kRaAQaK+a/mxYxhPxpK0094QFQBcVrvrXb3+j4M8l2G/C9CtQRWVXpX8ajWhYRik=
|   256 30:0b:c6:66:2b:8f:5e:4f:26:28:75:0e:f5:b1:71:e4 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIB2uNaKo2PK5cMci4E7dNWQ6ipiEzG3cWUR56qqMZqYR
80/tcp  open  http     Node.js (Express middleware)
|_http-favicon: Unknown favicon MD5: 621D76BDE56526A10B529BF2BC0776CA
|_http-title: La Casa De Papel                                                                 
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
443/tcp open  ssl/http Node.js Express framework
| tls-nextprotoneg: 
|   http/1.1                                
|_  http/1.0                                                                                   
| http-methods:                                                                                
|_  Supported Methods: HEAD                                                                    
| ssl-cert: Subject: commonName=lacasadepapel.htb/organizationName=La Casa De Papel
| Issuer: commonName=lacasadepapel.htb/organizationName=La Casa De Papel
| Public Key type: rsa
| Public Key bits: 2048
| Signature Algorithm: sha256WithRSAEncryption
| Not valid before: 2019-01-27T08:35:30
| Not valid after:  2029-01-24T08:35:30
| MD5:   6ea4 933a a347 ce50 8c40 5f9b 1ea8 8e9a
| SHA-1: 8c47 7f3e 53d8 e76b 4cdf ecca adb6 0551 b1b6 38d4
| -----BEGIN CERTIFICATE-----
| MIIC6jCCAdICCQDISiE8M6B29jANBgkqhkiG9w0BAQsFADA3MRowGAYDVQQDDBFs
| YWNhc2FkZXBhcGVsLmh0YjEZMBcGA1UECgwQTGEgQ2FzYSBEZSBQYXBlbDAeFw0x
| OTAxMjcwODM1MzBaFw0yOTAxMjQwODM1MzBaMDcxGjAYBgNVBAMMEWxhY2FzYWRl
| cGFwZWwuaHRiMRkwFwYDVQQKDBBMYSBDYXNhIERlIFBhcGVsMIIBIjANBgkqhkiG
| 9w0BAQEFAAOCAQ8AMIIBCgKCAQEAz3M6VN7OD5sHW+zCbIv/5vJpuaxJF3A5q2rV
| QJNqU1sFsbnaPxRbFgAtc8hVeMNii2nCFO8PGGs9P9pvoy8e8DR9ksBQYyXqOZZ8
| /rsdxwfjYVgv+a3UbJNO4e9Sd3b8GL+4XIzzSi3EZbl7dlsOhl4+KB4cM4hNhE5B
| 4K8UKe4wfKS/ekgyCRTRENVqqd3izZzz232yyzFvDGEOFJVzmhlHVypqsfS9rKUV
| SPHczaEQld3kupVrt/mBqwuKe99sluQzORqO1xMqbNgb55ZD66vQBSkN2PwBeiR
| PBRNXfnWla3Gkabukpu9xR9o+l7ut13PXdQ/fPflLDwnu5wMZwIDAQABMA0GCSqG
| SIb3DQEBCwUAA4IBAQCuo8yzORz4pby9tF1CK/4cZKDYcGT/wpa1v6lmD5CPuS+C
| hXXBjK0gPRAPhpF95DO7ilyJbfIc2xIRh1cgX6L0ui/SyxaKHgmEE8ewQea/eKu6
| vmgh3JkChYqvVwk7HRWaSaFzOiWMKUU8mB/7L95+mNU7DVVUYB9vaPSqxqfX6ywx
| BoJEm7yf7QlJTH3FSzfew1pgMyPxx0cAb5ctjQTLbUj1rcE9PgcSki/j9WyJltkI
| EqSngyuJEu3qYGoM0O5gtX13jszgJP+dA3vZ1wqFjKlWs2l89pb/hwRR2raqDwli
| MgnURkjwvR1kalXCvx9cST6nCkxF2TxlmRpyNXy4
|_-----END CERTIFICATE-----
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|_  Server returned status 401 but no WWW-Authenticate header.
|_ssl-date: TLS randomness does not represent time
| tls-alpn: 
|_  http/1.1
Service Info: OS: Unix
```


### 21/tcp  open  ftp      vsftpd 2.3.4  (Famous version with has a backdoor)
```bash
$ searchsploit vsftpd 2.3.4 
```