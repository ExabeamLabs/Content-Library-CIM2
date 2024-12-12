#### Parser Content
```Java
{
Name = "netskope-sc-cef-app-login-fail-loginfailed"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Conditions = [
  """"activity":"Login Failed""""
  """"ccl":"""
]
Fields = [
  """"hostname":\s*"({src_host}[^"]+)""""
  """"timestamp":\s*({time}\d{10})"""
  """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)"""
  """"app":\s*"\[?({app}[^"\]]+)"""
  """"User Name\s*":"({full_name}[^"]+)""""
  """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"user":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""""
  """"access_method":\s*"({auth_method}[^"]+)""""
  """"logintype":\s*"({auth_method}[^"]+)""""
  """"activity":\s*"({operation}[^"]+)""""
  """"os":\s*"((U|u)nknown|({os}[^"]+))""""
  """"browser":\s*"((U|u)nknown|({browser}[^"]+))""""
  """"page":\s*"({web_domain}[^"\/]+)"""
  """"url":\s*"({url}[^"]+)""""
  """"dst_location":\s*"(N/A|({location}[^"]+))""""
  """"file_size":\s*({bytes}\d+)"""
  """"file_type":\s*"({file_type}[^"]+)""""
  """"page_site":\s*"({app}[^"]+)""""
  """"dstport":\s*"({dest_port}\d+)""""
  """"action":\s*"({action}[^"]+)"""
  """"referer":\s*"({referrer}[^"]+)"""",
  """"useragent":\s*"({user_agent}[^"]+)""""
  """"dstip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "file_type->mime"
]
ParserVersion = "v1.0.0"


}
```