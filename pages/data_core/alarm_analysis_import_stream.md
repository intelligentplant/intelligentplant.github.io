# Alarm Analysis Import Stream

Alarm Analysis requires an import stream of Alarm & Event data. The
process of importing data is a two-stage process:

    ***Defining the Import Stream**:\\ Configuring a flow of data from an Event Source (e.g. an Alarm Collector database) to Alarm Analysis. This is defined in Data Core configuration.

    ***Configuring Transform Rules**:\\ The source data will require parsing, interpretation, and (in some cases) cleaning rules applied.  This is a specialized task requiring domain expertise. Alarm Analysis includes a configuration tool to assist the process.

The instructions below cover the first (more general) stage and describe
a use-case where the data is imported from a Process Vue Alarm & Event
database on SQL Server.

## 1\. Configure Event Source

Process Vue persists Alarm & Event data to SQL Server. We can set up SQL
Event Source to monitor the Process Vue data base and collect any new
records.

  - \[[https://appstore.intelligentplant.com/wiki/doku.php?id=data\_core:sqleventsource|SQL](https://appstore.intelligentplant.com/wiki/doku.php?id=data_core:sqleventsource%7CSQL)
    Event Source\]

## 2\. Configure Alarm Analysis Event Sink

work in progress...
