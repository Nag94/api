# Dehash.lt API

You can use our API without any limitations.


# Examples

### GET request:
```bash
$ curl "https://api.dehash.lt/api.php?search=e10adc3949ba59abbe56e057f20f883e"
e10adc3949ba59abbe56e057f20f883e:123456
````

### POST request:  
Note - POST request size limited to 10MB and every line should be same type.
```bash
$ cat md5.txt
e10adc3949ba59abbe56e057f20f883e
25f9e794323b453885f5181f1b624d0b

$ curl -X POST --data-binary @./md5.txt "https://api.dehash.lt/api.php"
25f9e794323b453885f5181f1b624d0b:123456789
e10adc3949ba59abbe56e057f20f883e:123456
```


### JSON Output:
If you prefer getting JSON format instead of hashcat style format add `&json=1` to the URL

```bash
$ curl "https://api.dehash.lt/api.php?search=e10adc3949ba59abbe56e057f20f883e&json=1"
{
    "http:\/\/nitrxgen.net": {
        "results": [
            "e10adc3949ba59abbe56e057f20f883e:123456"
        ]
    }
}
```
