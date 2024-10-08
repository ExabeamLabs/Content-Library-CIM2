#### Parser Content
```Java
{
Name = "cisco-ise-kv-endpoint-policy-verify-accounting"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss.SSS Z", "MMM dd HH:mm:ss" ]
  Conditions = [
    """CISE_TACACS_Accounting"""
    """AcctReply-Status=Success"""
    """Device Type="""
   ]
  Fields = [
    """({host}[^\s]+)\sCISE_TACACS_Accounting"""
    """Location=Location#All Locations#({location}[^,]+)"""
    """Device Type#All Device Types#({device_type}[^,]+)"""
    """AcctReply-Status=({result}[^,;]+)"""
    """({time}\w{3}\s\d+\s\d\d:\d\d:\d\d)\s"""
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d.\d+\s(\+|\-)\d\d:\d\d)\s""",
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """Remote-Address=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),""",
    """CmdAV=({command}[^,]+)\s],""",
    """Privilege-Level=({privileges}[^,]+),""",
    """({app}TACACS\+ Accounting)""",
    """\sUser=(({email_address}[^\s]+?@[^\s]+?)|({user}[\w\.\-]{1,40}\$?)),"""
    """TACACS\+\s*({operation}Accounting with Command)"""
  ]
  ParserVersion = "v1.0.0"


}
```