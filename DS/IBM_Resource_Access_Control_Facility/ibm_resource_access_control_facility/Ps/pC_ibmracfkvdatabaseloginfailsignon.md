#### Parser Content
```Java
{
Name = ibm-racf-kv-database-login-fail-signon
  ParserVersion = v1.0.0
  Product = IBM Resource Access Control Facility
  Conditions = [ """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS""", """EVNTNAME=Signon""", """EVNTTIME=""", "EVNTDATE=""" ]
   DupFields = ["additional_info->reason"]


}
```