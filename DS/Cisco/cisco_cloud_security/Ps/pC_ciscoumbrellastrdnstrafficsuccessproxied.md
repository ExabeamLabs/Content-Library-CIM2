#### Parser Content
```Java
{
Name = cisco-umbrella-str-dns-traffic-success-proxied
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Cloud Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""","Proxied","1 (A)","NOERROR","""]
  Fields = [
  """({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
  """(\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)(",("(({host}[\w.-]*)|[^,]*)"),"([^,]*,)?)(({full_name}[^"\(\)]+[\s,]+[^"\(\)]+?)?[\s\\\(]+\(((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|\)]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s\\\)",]+"""
   """(\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)",("[^"]*",){5}"({dns_query_type}[^"]+)(",")(|({dns_response_code}[^"]+))(",")(|({dns_query}[^"]*?)\.?)(",")(|({categories}({category}[^",]+)[^"]*))"""",
   """:\d\d:\d\d","[^"\(]+?\(({email_address}[^\s"@]+@({email_domain}[^\s"@\)\.]+\.[^\s"@\)]+))\)?","""
   """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d",("[^"]*?",|[^,]*?,){2}"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)","(|({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?)",(|("[^"]*",))"(|({result}[^",]+))"""" 
]


}
```