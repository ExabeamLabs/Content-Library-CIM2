#### Parser Content
```Java
{
Name = beyondtrust-prividentity-kv-app-activity-privilegedidentity-1
  ParserVersion = "v1.0.0"
  Product = Beyondtrust Privilege Identity
  Conditions = [ """sEventType=""", """sEventID="EVENT_ID_WEBAPP_GENERAL_ACCOUNT_OP"""", """sOriginatingApplicationName ="Privileged Identity"""" ]

lieberman-events = {
      Vendor = BeyondTrust
      Product = BeyondTrust Privileged Identity
      TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
      Fields = [
        """({host}\S+)\s+<Event"""
        """dwAppSpecificEventID="({event_code}\d+)"""
        """sEventID="({event_name}[^"]+)"""
        """sOriginatingApplicationName ="({app}[^"]+)"""
        """sOriginatingSystem="({src_host}[^"]+)"""
        """sOriginatingAccount="(({account_domain}[^\\]+)[\\]+)?({account}[^\s"]+)""""
        """dtPostTime="({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
        """sMessage="({additional_info}[^"]+)"""
        """sLoginName ="(({domain}[^\\]+)[\\]+)?({user}[^"]+)""""
# job_id is removed
        """sIpAddress="({src_ip}[A-Fa-f.:\d]+)"""
        
}
```