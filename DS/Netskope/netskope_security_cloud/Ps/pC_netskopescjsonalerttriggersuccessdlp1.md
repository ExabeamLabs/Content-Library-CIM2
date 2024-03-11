#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-dlp-1
  Conditions = [ """"netskope_pop":"""", """"event-name":"security-threat-detected"""", """"alert_type":"DLP"""" ]
  Fields = ${NetskopeParsersTemplates.cef-netskope-activity.Fields}[
    """"policy":"({alert_name}[^"]+)""",
    """"alert_type":"({alert_type}[^"]+)"""",
    """"dlp_rule_severity":"({alert_severity}[^"]+)""",
    """"dlp_incident_id":({alert_id}\d+)""",
    """"identifying-hash":\{"hash-type":"SHA256"[^\}]+?"hash-value":\s*"({hash_sha256}[^"]+)"""",
    """"md5":\s*"({hash_md5}[^"]+)""""
  ]
  DupFields = ["object->file_name" ]
  ParserVersion = v1.0.0

cef-netskope-activity = {
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Fields = [
""""hostname":\s*"({src_host}[^\"]+)"""
""""timestamp":\s*({time}\d{10})"""
"""requestClientApplication=({app}[^=]+?)\s+(\w+=|$)"""
""""app":\s*"\[?({app}[^\"\]]+)"""
""""User Name\s*":"({full_name}[^\"]+)"""
""""srcip":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
""""object":\s*"(\s+\"|(\s*(Unknown Unknown|unknown|Unknown|null|({object}[^\"]+?))\s*\"))"""
""""user":\s*"(unknown|(({email_address}[^\s@\"]+@[^\s@\"]+\.[^\s@\"]+)|(({domain}[^\s\"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^\s\"@\\\/]+))))"""
""""access_method":\s*"({auth_method}[^\"]+)"""
""""logintype":\s*"({auth_method}[^\"]+)"""
""""activity":\s*"({operation}[^\"]+)"""
""""os":\s*"((U|u)nknown|({os}[^\"]+))"""
""""browser":\s*"((U|u)nknown|({browser}[^\"]+))"""
""""page":\s*"({web_domain}[^\"//]+)"""
""""url":\s*"({url}[^\"]+)"""
""""dst_location":\s*"(N/A|({location}[^\"]+))"""
""""file_size":\s*({bytes}\d+)"""
""""file_type":\s*"({file_type}[^"]+)"""
""""page_site":\s*"({app}[^\"]+)"""
""""dstport\":"\s*({dest_port}\d+)""""
""""action\":"({action}[^\"]+)"""
""""referer":"({referrer}[^"]+)"""",
  
}
```