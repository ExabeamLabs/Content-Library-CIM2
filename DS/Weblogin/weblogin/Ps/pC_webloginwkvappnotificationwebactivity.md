#### Parser Content
```Java
{
Name = weblogin-w-kv-app-notification-webactivity
  ParserVersion = "v1.0.0"
  Product = Weblogin
  Vendor = Weblogin
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """status""", """sub=""","""uniq=""", """realm=""", """authref=""" ]
  Fields = [
    """:\d+\s({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}).*?user=(\s|({user}[^\s]+))\s*ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\sstatus=({action}[^\s]+)\s*sub=(\s|({url}({protocol}http|https):({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?)|({sub_status}.*?)\suniq).*?authref=({request_cookie}[^\s]+)\s*wl_authref=({private_cookie}[^\s]+)\s*realm=(({web_domain}[^"]+)?)""",
    """=http.+?({top_domain}[^\/\.\s]*(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+)"""
  ]


}
```