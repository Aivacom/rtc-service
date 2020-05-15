## Generating and Authenticating Token (Golang Version for User Authentication 2.0)
Token Generator supports identity authentication and expiration authentication as well as passthrough of service parameters (service parameters not verified).
The example code described in this version applies to the generation and verification of Token in the [User Authentication 2.0>](https://www.sunclouds.com/cloud/v2/developer/doc.htm?serviceId=101&typeCode=FAQ&title=%E7%94%A8%E6%88%B7%E9%89%B4%E6%9D%83%E8%AF%B4%E6%98%8E&version=2.0) version.

### Golang Example Code: [Click to Download](http://resource.sunclouds.com/SunClouds_TokenGenerator-GoLang-2.0_20190926141139.zip)

#### Example codes
Generate token
```json
appid:=int32(12345)
uid:="1234444"
expiresecs:=int32(46)
tk:=sctoken.NewSCToken(appid,uid,expiresecs)
// Set service parameters
tk.SetParameter("pkey1","pval1")
tk.SetParameter("pkey2","pval2")
// Set service permissions
tk.SetPrivilege("pri1",300)
tk.SetPrivilege("pri2",400)
// Generate token string
token:=tk.BuildToken("appkey1234")
```

#### Verify token
```json
// Parse token string to generate SCToken object
tk,err:=sctoken.ParseToken(token,"appkey1234")
if err!=nil {
	// print err
} else {
	if tk.IsValid(){
		// token valid
		// do something
		
	} else {
		// token has expired
	}
}
```
