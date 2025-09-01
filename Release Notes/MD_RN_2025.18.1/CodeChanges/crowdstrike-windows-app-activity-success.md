# Code Changes for crowdstrike-windows-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'crowdstrike-falcon-sk4-app-activity-eventsimplename-1', 'crowdstrike-falcon-sk4-app-activity-eventsimplename') && !InList(toLower(event_code), 'regsystemconfigkeyupdate','injectedthread','wmicreateprocess') && InList(toLower(os), 'win') |