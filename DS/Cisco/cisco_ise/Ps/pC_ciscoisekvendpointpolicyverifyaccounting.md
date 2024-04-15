#### Parser Content
```Java
{
Name = "cisco-ise-kv-endpoint-policy-verify-accounting"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
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
  ]
  ParserVersion = "v1.0.0"


}
```