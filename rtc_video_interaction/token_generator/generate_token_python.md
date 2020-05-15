[Definition from wiki: Service description class](http://cwiki.yy.com/pages/viewpage.action?pageId=9619465)
# Generating Authentication Token

During service access, token identity authentication must be performed for real-time audio/video interaction service. You need to generate a token on the business server. This section describes how to generate a token for authentication and provides example codes for reference.

Note: Example codes shown on this page derive from Python and apply to the generation and verification of token in the [User Authentication 2.0](/en/platform/other/user_auth.md) version.



## Python Example Codes

- **Generate token**
```
    app_id = 1296325
    app_secret = bytearray(b'abcdefg')
    uid = "987654321"
    valid_time = 100
    build_timestamp = int(time.time() * 1000)
    // Set service parameters
    parameter = {"pkey1": "pval1", "pkey2": "pval2"}
    // Set service permissions
    privileges = {"pri1": 300, "pri2": 400}
    // Generate token string
    token_str = SCToken().gen(app_id, app_secret, uid, parameter, privileges, build_timestamp, valid_time)
```

- **Verify token**
```
    // Parse token string to generate SCToken object
    app_secret = bytearray(b'abcdefg')
    token_str = "_2dllwAAAHMAADA5AAk5ODc2NTQzMjEAAgAFcGtleTIABXB2YWwyAAVwa2V5MQAFcHZhbDEAAgAEcHJpMQAAAAAAAAEsAARwcmkyAAAAAAAAAZAAAAFsuAVsTAAA6mDjTWxNCdjou_5GSCFCWLtGAgn9Ww"
    
    yt, err = SCToken().parse(token_str, app_secret)
    
    if err != None:
        // print "token parsing failed"
    else:
        if yt.validate():
            // print "token valid”
            // do something
        else:
            //print  "token expired”

```

## Example Codes Downloading

Example codes in Python 2.7: [Click to download](http://resource.sunclouds.com/SunClouds_TokenGenerator-python2.7-2.0_20190926144831.zip)
Example codes in Python 3.0: [Click to download](http://resource.sunclouds.com/SunClouds_TokenGenerator-python3.0-2.0_20190926145828.zip)


