#### Parser Content
```Java
{
Name = "hp-arubawc-cef-radius-traffic-fail-radius"
Product = "Aruba Wireless controller"
Conditions = [
  """CEF:"""
  """|Aruba Networks|ClearPass|"""
  """|RADIUS Failed Authentications|"""
]
ParserVersion = "v1.0.0"

q-aruba-nac-logon = {
  Vendor = HP
  Product = Aruba ClearPass Policy Manager
  TimeFormat = ["yyyy-MM-dd HH:mm:ssZ", "yyyy-MM-dd HH:mm:ss.SSSZ" ]
  Fields = [
    """Common\.Request-Timestamp=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(\.\d+)?[\+\-]\d+)""",
    """\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({host}[\w\-.]+)""",
    """Common\.Username=(({user_type}host)\/({src_host}[\w\-.]+)|([\d]{14})|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_mac}([a-fA-F\d]{2}[\-:]?){5}[a-fA-F\d]{2})|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\+)?({=user}[\w\.\-\!\#\^\~]{1,40}\$?)),""",
    """Common\.Service=({network}[^,]+)""",
    """Common\.Host-MAC-Address=({src_mac}\w+)""",
    """Common\.NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  ]
  DupFields = [ "host->auth_server" 
}
```