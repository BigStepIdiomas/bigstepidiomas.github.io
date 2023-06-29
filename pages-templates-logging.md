---
layout: default
title: Templates - Logging
description: What're ya buyin?
---

<style>
.tag {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  color: #fff;
  font-size: 14px;
  font-weight: bold;
  margin-right: 8px;
  margin-bottom: 10px;
}

/* Add the background colors for each category */
.tag:nth-child(1) { background-color: #007bff; } /* UX Writing */
.tag:nth-child(2) { background-color: #28a745; } /* Technical Specification */
.tag:nth-child(3) { background-color: #dc3545; } /* API Docs */
.tag:nth-child(4) { background-color: #ffc107; } /* Technical Documentation */
.tag:nth-child(5) { background-color: #6f42c1; } /* Knowledge Base */
.tag:nth-child(6) { background-color: #fd7e14; } /* Translation */
.tag:nth-child(7) { background-color: #20c997; } /* English */
.tag:nth-child(8) { background-color: #e83e8c; } /* Installation Guides */
.tag:nth-child(9) { background-color: #6c757d; } /* Help Docs */
.tag:nth-child(10) { background-color: #17a2b8; } /* Troubleshooting */
.tag:nth-child(11) { background-color: #87ceeb; } /* Handbooks */
.tag:nth-child(12) { background-color: #90ee90; } /* Support Docs */
.tag:nth-child(13) { background-color: #ff6666; } /* Project Docs */
.tag:nth-child(14) { background-color: #ffff99; } /* Portuguese */
.tag:nth-child(15) { background-color: #d291bc; } /* Release Notes */
.tag:nth-child(16) { background-color: #ffb347; } /* German */
.tag:nth-child(17) { background-color: #98d8d8; } /* SDK */
.tag:nth-child(18) { background-color: #ffb6c1; } /* Product Discovery */
.tag:nth-child(19) { background-color: #d3d3d3; } /* UX Design */
.tag:nth-child(20) { background-color: #afeeee; } /* Spanish */
.tag:nth-child(21) { background-color: #cd853f; } /* Copywriting */
.tag:nth-child(22) { background-color: #ffa07a; } /* Microcopy */
.tag:nth-child(23) { background-color: #f08080; } /* Educational Material */
.tag:nth-child(24) { background-color: #da70d6; } /* Localization */
.tag:nth-child(25) { background-color: #8470ff; } /* User Guides */
</style>

<span class="tag" style="background-color: #007bff;">UX Writing</span>
<span class="tag" style="background-color: #28a745;">Technical Specification</span>
<span class="tag" style="background-color: #dc3545;">API Docs</span>
<span class="tag" style="background-color: #ffc107;">Technical Documentation</span>
<span class="tag" style="background-color: #6f42c1;">Knowledge Base</span>
<span class="tag" style="background-color: #fd7e14;">Translation</span>
<span class="tag" style="background-color: #20c997;">English</span>
<span class="tag" style="background-color: #e83e8c;">Installation Guides</span>
<span class="tag" style="background-color: #6c757d;">Help Docs</span>
<span class="tag" style="background-color: #17a2b8;">Troubleshooting</span>
<span class="tag" style="background-color: #87ceeb;">Handbooks</span>
<span class="tag" style="background-color: #90ee90;">Support Docs</span>
<span class="tag" style="background-color: #ff6666;">Project Docs</span>
<span class="tag" style="background-color: #ff6666;">Portuguese</span>
<span class="tag" style="background-color: #d291bc;">Release Notes</span>
<span class="tag" style="background-color: #ffb347;">German</span>
<span class="tag" style="background-color: #98d8d8;">SDK</span>
<span class="tag" style="background-color: #ffb6c1;">Product Discovery</span>
<span class="tag" style="background-color: #d3d3d3;">UX Design</span>
<span class="tag" style="background-color: #afeeee;">Spanish</span>
<span class="tag" style="background-color: #cd853f;">Copywriting</span>
<span class="tag" style="background-color: #ffa07a;">Microcopy</span>
<span class="tag" style="background-color: #f08080;">Educational Material</span>
<span class="tag" style="background-color: #da70d6;">Localization</span>
<span class="tag" style="background-color: #8470ff;">User Guides</span>

---
title: template for logging
author: The Good Docs Project 
uri-repo: https://github.com/projectname
company: REPLACEME
product: # Set the product parameter to add the product name here.
app: # Insert the name of the app here.
tags: # Set other global keywords here like app name and product name or any other likely labels. These are comma-separated tags.
---

{Begin your Reference topic in this section. 
For help with writing and structuring a reference article, see the README.md in the template directory for basic guidelines and links.
Check out https://www.markdownguide.org/basic-syntax/ if you get stuck with AsciiDoc syntax.}


# {pipeline} for {app}

## Logging description

|Parameter name|Description|
| :---        | :----       |
|Log pipeline name |Specify the name of the logstash pipeline in this field.|
|Description|Summarise why this log format exists, or why you would look for this log. What you put here is reused in the Log description section and included in HTML description tags.|
|Log format |Specify the format of the log file: XML or JSON.|
|Log transfer method |Single-line curl using MSSQL Service Broker. <br>App writes to a log file which is shipped to logstash using filebeat.|
|Output location |If the output location uses curl, then specify a URL similar to https://logs.{company}.com.au/csdb_appflow. <br>If the output location is to a file, specify the `/path/to/the/logfile`.|


## Logging example

Logging example

```xml
<message>
   <detail>
      <dt>2017-05-22T13:35:27.013</dt>
      <appId>4240263</appId>
      <sourceId>3585996</sourceId>
      <refreshId>0</refreshId>
      <dt2>2017-05-22T13:35:27.013+1000</dt2>
      <action>appReady</action>
      <apiGuid>BB31E8B6-88C8-4DEB-9529-8EFD7F680C0B</apiGuid>
   </detail>
</message>
```

## Log properties

In addition to the mandatory logging properties sent for all log pipelines, the following log properties are sent for this pipeline.

| Property name | Description | Logstash type | Logstash type |
| :---        | :----       |:----   |:----   |
| This example row will give you an idea of what to put in this table csdb_appflow.api-guid| The unique API GUID from a <_company_> application flow. This information is extracted from the <apiGuid> element in the XML log| Choose One string integer float |BB31E8B6-88C8-4DEB-9529-8EFD7F680C0B |





[Back](./)