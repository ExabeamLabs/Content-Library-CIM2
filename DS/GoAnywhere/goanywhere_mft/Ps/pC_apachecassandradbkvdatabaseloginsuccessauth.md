#### Parser Content
```Java
{
Name = apache-cassandradb-kv-database-login-success-auth
Conditions = [
  """|category:AUTH|"""
  """|type:LOGIN|"""
  """|authenticated:"""
  """|user:"""
  """|operation:"""
]
ParserVersion = "v1.0.0"

goanywhere-events-2 = {
    Vendor = GoAnywhere
    Product = GoAnywhere MFT
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d[+-]\d\d:\d\d)\s({dest_host}[\w\-.]+)""",
      """GoACHremote_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """GoACHlocal_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """GoACHuser_name="(({email_address}[^@"]+@[^\.]+\.[^"]+)|(admin|666666|guest|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
      """GoACHevent_type="({event_name}[^"]+)"""",
    
}
```