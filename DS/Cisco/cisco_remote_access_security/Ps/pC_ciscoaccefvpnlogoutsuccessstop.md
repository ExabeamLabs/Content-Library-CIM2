#### Parser Content
```Java
{
Name = cisco-ac-cef-vpn-logout-success-stop
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Remote Access Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """cisco-av-pair=mdm-tlv=ac-user-agent=AnyConnect""", """Acct-Status-Type=Stop""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
    """UserName =(({email_address}[^@,]+@[^,]+)|(({domain}[^\\,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """Device\sIP\sAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """NetworkDeviceName =({src_host}[^,]+)""",
    """NAS-IP-Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Calling-Station-ID=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({src_host}[\w\-\.]+)),""",
    """NAS-Port=({dest_port}\d{1,9})\D""",
    """Acct-Session-Time=({session_duration}[^,]+)""",
    """Acct-Terminate-Cause=({result_reason}[^,]+)"""
  ]


}
```