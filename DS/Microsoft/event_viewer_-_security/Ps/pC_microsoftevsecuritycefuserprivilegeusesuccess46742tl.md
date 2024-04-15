#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-4674-2-tl"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<data name"""
""""eventid":4674"""
"""xmlns"""
""""activity":"4674 - an operation was attempted on a privileged object.""""
]
Fields = [
"""(?i)TimeGenerated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""(?i)<Keywords>({result}.+?)</Keywords>"""
"""(?i)Computer"+:"+({host}[^"]+)"""
"""(?i)({event_code}4674)"""
"""(?i)<Data Name(\\)?=(\\)?"+SubjectUserSid(\\)?"+>(?:NONE_MAPPED|({user_sid}[^<]+))"""
"""(?i)<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({user}[^<]+))<\/Data>"""
"""(?i)<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({domain}[^<]+))<\/Data>"""
"""(?i)<Data Name(\\)?=(\\)?"+SubjectLogonId(\\)?"+>({login_id}[^<]+)<\/Data>"""
"""(?i)<Data Name(\\)?=(\\)?"+ObjectServer(\\)?"+>(-|({object_server}[^<]+))"""
"""(?i)<Data Name(\\)?=(\\)?"+PrivilegeList(\\)?"+>({privileges}[^<]+)"""
"""(?i)<Data Name(\\)?=(\\)?"+ProcessName(\\)?"+>({process_path}({process_dir}[^<]*?)({process_name}[^\\<]+?))<\/Data>"""
"""(?i)"Activity".+?({event_name}An operation was attempted on a privileged object)"""
"""(?i)<Data Name(\\)?=(\\)?"+ProcessId(\\)?"+>({process_id}[^<]+)<\/Data>"""
"""(?i)<Data Name(\\)?=(\\)?"+ObjectType(\\)?"+>(-|({object_type}[^<]+))"""
"""(?i)<Data Name(\\)?=(\\)?"+ObjectName(\\)?"+>(-|({object}[^<]+))"""
]
DupFields = [
"""host->dest_host"""
]
ParserVersion = "v1.0.0"


}
```