#### Parser Content
```Java
{
Name = "cisco-duo-csv-app-login-success-successful"
    Vendor = "Cisco"
    Product = "Duo Access"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ ""","SUCCESS","""" ]
    Fields = [
      """SUCCESS","({user}[\w\.\-]{1,40}\$?)""""
      """"\d{10}",(("[^"]+")?,)"(?:n\/a|({auth_method}[^"]+))""""
      """"\d{10}",(("[^"]+")?,){2}"({app}[^"]+)""""
      """"\d{10}",(("[^"]+")?,){3}"(?:0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
    ]
    ParserVersion = "v1.0.0"
  

}
```