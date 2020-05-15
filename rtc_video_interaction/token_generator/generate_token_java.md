# Generating Authentication Token

During service access, token identity authentication must be performed for real-time audio/video interaction service. You need to generate a token on the business server. This section describes how to generate a token for authentication and provides example codes for reference.

Note: Example codes shown on this page derive from Java and apply to the generation and verification of token in the [User Authentication 2.0](/en/platform/other/user_auth.md) version.



## Java Example Codes

- **Generate token**
```
  private static void genToken()
      throws UnsupportedEncodingException {
  
     /*
      * Initialize tokenbuilder, you need to pass in Shangyun to apply for token
      * 
      */
     SCTokenBuilder builder = new SCTokenBuilder( new SCTokenAppSecretProvider() {
  
        @Override
        public String getAppsecret( int appKey ) {
  
           // Certificate corresponding to the items applied for on SunClouds console
           return "1234";
        }
     } );
     /*
      * Parameter:
      *
      * version token Version, integer 
      * 
      * Project id applied by SunClouds, integer
      * 
      * User uid, business definition, string
      *
      * Effective duration, in seconds
      * 
      * token generates the current timestamp
      */
       SCTokenPropertyProvider provider = new SCTokenPropertyProvider(2, 1234, "2483549835", 4*60*60);
       //Configure the parameters required for extended attributes, the specific values are based on service-dependent parameters
       provider.getParameterProperties()
       //
       .addTokenExtendProperty("param1","content")
       //
       .addTokenExtendProperty("param2",2);
  
       //Configure the parameters for permission, the specific values are based on service-dependent parameters for permission
       provider.getPrivilegeProperties()
       //
       .addTokenExtendProperty("privilege1",12345566l)
       //
       .addTokenExtendProperty("privilege2",12345566l);
  
       //Generate token according to attribute configuration
       byte[] token = builder.buildBinanyToken( provider );
       // In order to facilitate network transmission, BASE 64 encode and url_safe mode are used
       Base64 coder = new Base64( 76, new byte[] {}, true );
  
       // The byte array is converted to a string to print
       String tokenStr = coder.encodeAsString( token );
       System.out.println( "gen token:"+ tokenStr );
  }
```

- **Verify token**
```
private static void validToken(String tokenStr) throws UnsupportedEncodingException {

   /*
    * Initialize tokenbuilder, you need to pass in Shangclouds to apply for token
    *
    */
   SCTokenBuilder builder = new SCTokenBuilder( new SCTokenAppSecretProvider() {

      @Override
      public String getAppsecret( int appKey ) {

         // Certificate corresponding to the items applied for on SunClouds console
         return "1234";
      }
   } );
   Base64 coder = new Base64( 76, new byte[] {}, true );

   byte[] token = coder.decode( tokenStr.getBytes( "UTF-8" ) );
   SCToken scToken = builder.validateTokenBytes( token );
   System.out.println( "decode token: " + scToken.toString());
}
```



## Example Codes Downloading

[Click to download](http://resource.sunclouds.com/SunClouds_tokenGenerator_Java_20191216.zip)


