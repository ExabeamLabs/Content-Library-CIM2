#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-4776"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4776"""
  ]
  Fields = [
    """({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
    """({event_code}4776)"""
    """\srt=({time}\d{13})"""
    """\sshost=({dest_host}[\w\-.]+)"""
    """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
    """dvchost=(?!(?:[A-Fa-f:\d.]+))[^\s.]+(\.({domain}[^\s.]+)[^\s]*)"""
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s.]+)[^\s]*)?\s+\w+="""
    """\scs4=({result_code}\w+)"""
    """dvc=({host}[^\s]+)"""
    """dvchost=({host}[^\s]+)"""
  ]


}
```