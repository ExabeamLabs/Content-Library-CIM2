#### Parser Content
```Java
{
Name = microsoft-evsecurity-leef-endpoint-logout-4647
  Conditions = [ """LEEF:""", """|Microsoft|Windows|""", """|4647|""" ]
  Fields = ${WindowsParsersTemplates.windows-leef-events.Fields}[
  ]

windows-leef-events = {
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
    Fields = [
      """devTime=({time}[^=]+)\s+\w+="""
      """cat=({result}[^=]+?)\s+\w+="""
      """sev=({severity}\d+)"""
      """resource=({dest_host}[^=]+?)\s+\w+="""
      """\susrName =(-|([^@"\s]+@[^@"\s]+)|(({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      """application=({app}[^=]+?)\s+\w+="""
      """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:"""
      """Account Domain:\s+({domain}[^:]+?)\s+Logon ID:"""
      """Logon ID:\s+({login_id}\w+)"""
      """Group Name:\s+({group_name}[^:]+?)\s+Group Domain:\s+({group_domain}[^:]+?)\s+"""
      """Changed Attributes:\s+({attribute}[^:=]+?)\s+Account"""
      """message=({event_name}[^=]+?)\s+Subject:"""
      """\|Microsoft\|Windows\|\w+\|({event_code}\d+)"""
    
}
```