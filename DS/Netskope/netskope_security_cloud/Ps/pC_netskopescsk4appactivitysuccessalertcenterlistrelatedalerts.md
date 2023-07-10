#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-activity-success-alertcenterlistrelatedalerts
  Conditions = [ """"type":"""", """destinationServiceName =Netskope""", """"activity":"ALERT_CENTER_LIST_RELATED_ALERTS"""" ]
  ParserVersion = "v1.0.0"

cef-netskope-activity-1 = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Fields = [
    """"hostname":\s*"({src_host}[^"]+)"""",
    """"timestamp":\s*({time}\d{10})""",
    """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)""",
    """"app":\s*"\[?({app}[^"\]]+)""",
    """"User Name\s*":"({full_name}[^"]+)"""",
    """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"object":\s*"(\s+"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^"]+?))\s*"))""",
    """"user":\s*"(unknown|(({email_address}[^\s@"]+@[^\s@"]+\.[^\s@"]+)|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^\s"\\\/@]+))))"""",
    """"access_method":\s*"({auth_method}[^"]+)"""",
    """"logintype":\s*"({auth_method}[^"]+)"""",
    """"activity":\s*"({operation}[^"]+)"""",
    """"os":\s*"((U|u)nknown|({os}[^"]+))"""",
    """"browser":\s*"((U|u)nknown|({browser}[^"]+))"""",
    """"page":\s*"({web_domain}[^"//]+)""",
    """"url":\s*"({url}[^"]+)"""",
    """"dst_location":\s*"(N/A|({location}[^"]+))"""",
    """"file_size":\s*({bytes}\d+)""",
    """"file_type":\s*"({file_type}[^"]+)"""",
    """"page_site":\s*"({app}[^"]+)"""",
    """"dstport":"\s*({dest_port}\d+)"""",
    """"referer":"({referrer}[^"]+)"""",
    """"action":"({action}[^"]+)"""
  ]
  DupFields = ["domain->email_domain", "file_type->mime"
}
```