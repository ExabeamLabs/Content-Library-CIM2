#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-web
  ParserVersion = v1.0.0
  Conditions = [ """| incident_type="web"|""", """| protocol="HTTP""" ]

symantec-dlp-alert = {
      Vendor = Symantec
      Product = Symantec DLP
      TimeFormat = ["MMMM dd, yyyy HH:mm:ss a","yyyy-MM-dd HH:mm:ss"]
      Fields = [
        """incident_id="({alert_id}\d+)"""",
        """\|\spolicy="({alert_name}[^"]+)"""",
        """\|\sseverity=\s*"({alert_severity}[^"]+)"""",
        """\|\spolicy_rule="({policy_name}[^"]+?)\s*"""",
        """\|\incident_type="({alert_type}[^"]+)""",
        """\|\sUserID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """\|\sprotocol="({protocol}[^"]+)"""",
        """\|\sBusiness_Unit="({additional_info}[^"]+)"""",
        """\|\sfilename="(N/A|unknown|({target}[^"]+?))\s*"""",
        """\|\sfilename="(N/A|unknown|({file_name}[^"]+?\.\w+))""",
        """\|\sRR_Action="({action}[^"]+)""",
        """\|\smatch_count="({match_count}\d+)""",
        """\|\sEP_Machine="({src_host}[^"]+)""",
        """\|\sEP_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        """\|\sEP_Location="({src_location}[^"]+)""",
        """\|\application="({app}[^"]+)"""",
        """\|\device_id="({device_id}[^"]+)"""",
        """\|\sRR_Action="({result}[^"]+)""",
      ]
    }
    symantec-dlp-alert-1 = {
      Vendor = "Symantec"
      Product = "Symantec DLP"
      TimeFormat = [ "MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ" ]
      occured_timeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ"]
      Fields = [
        """({host}[\w\.-]+)\s+DLP\|Symantec\|""",
        """\|incident_id=({alert_id}\d+)""",
        """\|severity=\d+\:({alert_severity}\w+)\|\w+=""",
        """\|occurred_on=({occured_time}[^\|]+?)\s*\|""",
        """\|reported_on=({time}[^\|]+?)\s*\|""",
        """\|policy_name=({alert_name}[^\|]+?)\s*\|""",
        """\|policy_rule=({alert_type}[^\|]+?)\s*\|""",
        """\|Protocol=({protocol}[^\|]+?)\s*\|""",
        """\|blocked=(None|({action}[^\|]+?))\s*\|""",
        """\|host=(?:N\/A|({src_host}[^\|]+?))\s*\|""",
        """\|machine_ip=(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
        """\|deviceId=(?:N\/A|({device_id}[^\|]+?))\s*\|""",
        """\|username=(?:N\/A|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
        """\|filename=(?:N\/A|({file_name}[^\|]+))""",
        """\|attachment_name=(?:N\/A|({file_name}[^\|]+))""",
        """\|filepath=(?:N\/A|({file_path}[^\|]+))""",
        """\|dst=(?:N\/A|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
        """\|recipient=(?:N\/A|({email_recipients}[^\|]+?))\s*\|"""
    symantec-dlp-alert = {
      Vendor = Symantec
      Product = Symantec DLP
      TimeFormat = ["MMMM dd, yyyy HH:mm:ss a","yyyy-MM-dd HH:mm:ss"]
      Fields = [
        """incident_id="({alert_id}\d+)"""",
        """\|\spolicy="({alert_name}[^"]+)"""",
        """\|\sseverity=\s*"({alert_severity}[^"]+)"""",
        """\|\spolicy_rule="({policy_name}[^"]+?)\s*"""",
        """\|\incident_type="({alert_type}[^"]+)""",
        """\|\sUserID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
        """\|\sprotocol="({protocol}[^"]+)"""",
        """\|\sBusiness_Unit="({additional_info}[^"]+)"""",
        """\|\sfilename="(N/A|unknown|({target}[^"]+?))\s*"""",
        """\|\sfilename="(N/A|unknown|({file_name}[^"]+?\.\w+))""",
        """\|\sRR_Action="({action}[^"]+)""",
        """\|\smatch_count="({match_count}\d+)""",
        """\|\sEP_Machine="({src_host}[^"]+)""",
        """\|\sEP_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        """\|\sEP_Location="({src_location}[^"]+)""",
        """\|\application="({app}[^"]+)"""",
        """\|\device_id="({device_id}[^"]+)"""",
        """\|\sRR_Action="({result}[^"]+)""",
      ]
    }
}
```