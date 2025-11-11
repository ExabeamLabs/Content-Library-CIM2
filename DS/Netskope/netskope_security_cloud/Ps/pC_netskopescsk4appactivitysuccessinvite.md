#### Parser Content
```Java
{
Name = netskope-sc-sk4-app-activity-success-invite
  ParserVersion = v1.0.0
  Conditions = [ """"type":""", """"ccl":""", """"activity":""", """"Invite"""" ]

cef-netskope-activity = {
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Fields = [
    """"hostname":\s*"({src_host}[\w\-.]+)""""
    """"timestamp":\s*({time}\d{10})"""
    """requestClientApplication=({app}[^=]+?)\s+(\w+=|$)"""
    """"User Name\s*":\s*"({full_name}[^\"]+)"""
    """"srcip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"object":\s*"'?\s*({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)'?"[^\}]*?"object_type":\s*"(File|Image)""""
    """"object":\s*"'?\s*(({folder_name}[^"\\\/']+)|({file_dir}[^"\/\\']+[\/\\]+[^"]+))"'?[^\}]*?"object_type":\s*"Folder""""
    """"object":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s\"@\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"[^\}]*?"object_type":\s*"User""""
    """"object":\s*"(Unknown Unknown|unknown|Unknown|null|\s*(|({object}[^"]+?)))\s*"[^\}]*?"object_type":\s*"(?!(File|Image|Folder|User))({object_type}[^"]+)""""
    """"object":\s*"({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"[^\}]*?"activity":\s*"File\w+""""
    """"object_type":\s*"(File|Image)"[^\}]*?"object":\s*"\s*({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)""""
    """"object_type":\s*"Folder"[^\}]*?"object":\s*"\s*(({folder_name}[^"\\\/]+)|({file_dir}[^"\/\\]+[\/\\]+[^"]+))""""
    """"object_type":\s*"User"[^\}]*?"object":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s\"@\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?""""
    """"object_type":\s*"(?!(File|Image|Folder|User))({object_type}[^"]+)"[^\}]*?"object":\s*"(Unknown Unknown|unknown|Unknown|null|\s*(|({object}[^"]+?)))\s*""""
    """"user":\s*"(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\s"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))""""
    """"access_method":\s*"({auth_method}[^\"]+)"""
    """"logintype":\s*"({auth_method}[^\"]+)"""
    """"activity":\s*"({access}({operation}[^\"]+))"""
    """"os":\s*"((U|u)nknown|({os}[^\"]+))"""
    """"browser":\s*"((U|u)nknown|({browser}[^\"]+))"""
    """"page":\s*"({web_domain}[^\"\/]+)"""
    """"url":\s*"({url}[^\"]+)"""
    """"dst_location":\s*"(N/A|({location}[^\"]+))"""
    """"file_size":\s*({bytes}\d+)"""
    """"file_type":\s*"({mime}({file_type}[^"]+))"""
    """"page_site":\s*"({app}[^\"]+)"""
    """"app":\s*"\[?({app}[^\"\]]+)"""
    """"dstport\":"\s*({dest_port}\d+)""""
    """"action":\s*"({action}[^"]+)"""
    """"referer":\s*"({referrer}[^"]+)""""
    """"useragent":"({user_agent}[^"]+)""""
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """"activity":\s*"File\w+"[^\}]*?"object":\s*"({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)""""
    """"object":\s*"({file_name}[^"]+?(\.({file_ext}[^"\.\s\\\/]+?))?)"[^\}]*?"activity":\s*"File\w+""""
  
}
```