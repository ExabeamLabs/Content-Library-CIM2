#### Parser Content
```Java
{
Name = "apple-macos-str-endpoint-login-success-storingcredential"
Vendor = "Apple"
Product = "macOS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """pam_sm_setcred: storing credential"""
]
Fields = [
  """\d\d\s+\d\d:\d\d:\d\d\s({dest_host}[^\s]+)\s+(?:-|({process_path}[^\s]+?))\[({login_id}\d+).+?\sfor:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^\s.]+))?"""
  """.+\d\d:\d\d:\d\d\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```