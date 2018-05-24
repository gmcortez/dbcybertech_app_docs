The Dashboards
===============

Discovery Event Dashboard
----------------------------

The Discovery Event Dashboard Per Machine monitors the events for new database service, new database conversation, new host identified, and new users identified.  Since the syslog events from the DB-Security appliance are sent every 5 to 10 minutes interval, the dhasboard panels have a default refresh of 10 minutes.

- *New Database Service Identified*:  This panel specifically monitors the ``mds_new_service`` identifier from the events and tabulates key information useful for the operator.  This panel will tell operator if a new database service was created within the network being monitored.
- *New Conversation Identified*:  This panel specifically monitors the ``tally_new_ipseity`` identifier from the events and tabulates key information useful for the operator.  This panel will tell operator if a new client is communicating with an existing database service within the network being monitored.
- *New Host Identified*:  This panel specifically monitors the ``mds_new_host`` identifier from the events and tabulates key information useful for the operator.  This panel will tell operator if a new host containing database services is running within the network being monitored.
- *New Users Identified*:  This panel specifically monitors the ``mds_new_user`` identifier from the events and tabulates key information useful for the operator.  This panel will tell operator if a new database user was created from within the network being monitored.

 To use this dashboard, you have to provide the following input on the top of the dashboard:
  1. Select Index:  select the proper index where the DB-Security event logs are being collected.
  2. Select Sourcetype: selecting the proper sourcetype will help in the efficiency fo the dashboard.  If you are using the `DB Cybertech Add-on for Splunk <https://splunkbase.splunk.com/app/3587/>`_ , then you should use the ``dbn:dbn6300:discoveryEvents`` sourcetype.
  3. Select Machine:  if your network have multiple DB-Security appliances, then this input will search for the past 7 days for DB-Security machines that have events and list it here in the dropdown.  Select the machine that you want to monitor.
  4. Select Time Period:  select the time period that you would like to monitor.  For SOC operations, a 3 to 5 days span is more than enough.  For investigation purposes, a longer time span may be needed.

Screenshot: some image goes here

    .. image:: images/sample.jpg




Application Security Events
----------------------------

The Application Security Events dashboard monitors the events for databse services that are in "protection mode".  New SQL statements events that contains probable application security (like SQL injection) will appear here, SQL statements events that also contains lexical errors will appear in this dashboard.

This dashboard particularly monitors events that contain ``distinct_event`` identifier from the events and tabulates key information useful for the operator.  This will tell the operator if a new SQL statement posseses any threat or lexical errors.

To use this dashboard, you have to provide the following input on the top of the dashboard:
 1. Select Index:  select the proper index where the DB-Security event logs are being collected.
 2. Select Sourcetype: selecting the proper sourcetype will help in the efficiency fo the dashboard.  If you are using the `DB Cybertech Add-on for Splunk <https://splunkbase.splunk.com/app/3587/>`_ , then you should use the ``dbn:dbn6300:sqliEvents`` sourcetype.
 3. Select Machine:  if your network have multiple DB-Security appliances, then this input will search for the past 7 days for DB-Security machines that have events and list it here in the dropdown.  Select the machine that you want to monitor.
 4. Select Time Period:  select the time period that you would like to monitor.  For SOC operations, a 3 to 5 days span is more than enough.  For investigation purposes, a longer time span may be needed.

Screenshot: some image goes here

   .. image:: images/sample.jpg


Insider Threat Events
---------------------

Some texts goes here......


Vital Counter Rates and Health per Machine
------------------------------------------

Some texts goes here......
