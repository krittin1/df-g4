## LABEL

คำสั่ง `LABEL` เป็นคำสั่งที่


```dockerfile
    # Set one or more individual labels
    LABEL com.example.version="0.0.1-beta"
    LABEL vendor1="ACME Incorporated"
    LABEL vendor2=ZENITH\ Incorporated
    LABEL com.example.release-date="2015-02-12"
    LABEL com.example.version.is-production=""
```


```dockerfile
    # Set multiple labels on one line
    LABEL com.example.version="0.0.1-beta" com.example.release-date="2015-02-12"
```

```dockerfile
    # Set multiple labels at once, using line-continuation characters to break long lines
    LABEL vendor=ACME\ Incorporated \
    com.example.is-beta= \
    com.example.is-production="" \
    com.example.version="0.0.1-beta" \
    com.example.release-date="2015-02-12"
```
