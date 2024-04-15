#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-fail-4625"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4625|"""
  ]
  Fields = [
    """({event_name}An account failed to log on)"""
    """\sexternalId=({event_code}\d+)"""
    """\srt=({time}\d{13})"""
    """\sdvc=({host}[a-fA-F:\d.]+)"""
    """\sdvchost=({host}[^\s]+)"""
    """\sduser=({user}.+?)\s+\w+="""
    """\sdntdom=({domain}.+?)\s\w+="""
    """Security_,ID=({user_sid}[^\s]+)"""
    """\ssrc=(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
    """\scn1=({login_type}\d+)"""
    """\scs5=({auth_package}[^\s]+)"""
    """\sdeviceProcessName =({auth_process}[^\s]+)"""
    """Sub_,Status=({result_code}[^\s]+)"""
    """Account locked out.+?flexString1=({result_code}[^\s]+)"""
    """Key_,Length=({key_length}\d+)"""
  ]
  DupFields = [
    "host->dest_host"
    "result_code->failure_code"
  ]


}
```