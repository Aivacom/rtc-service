# Generating Authentication Token

During service access, token identity authentication must be performed for real-time audio/video interaction service. You need to generate a token on the business server. This section describes how to generate a token for authentication and provides example codes for reference.

Note: Example codes shown on this page derive from Golang and apply to the generation and verification of token in the [User Authentication 2.0](/en/platform/other/user_auth.md) version.



## Golang Example Codes

- **Generate token**
```
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


- **Verify token**
```
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

## Example Codes Downloading

[Click to download](http://resource.sunclouds.com/SunClouds_TokenGenerator-GoLang-2.0_20190926141139.zip)


