# ccnet.datetimelabeller

Datetime labeller for CruiseControl.NET.


## Description

Datetime Labeller for CC.NET makes possible to label your builds with customized date time format.

## Introduction

Create build label with specific date time format.

## Installation

Download ccnet.datetimelabeller.plugin.dll file  from Release into the CruiseControl.NET Installation folder (e.g. C:\Program Files\CruiseControl.NET\server), 
Restart the CruiseControl.NET Service.

1. Start -> Run -> services.msc
2. Right-Click on the CruiseControl.NET Service
3. Restart

Modify your ccnet.config file to effectively use the labeller.

## How to use

Modify your `ccnet.config` file, under the `<project>` node add a lableller as:

```xml
<labeller type="datetimeLabeller">       
  <major>1</major>
  <minor>4</minor>
  <datetimeFormat>MMdd</datetimeFormat>
  </labeller>
```

The full exmaple for `<datatimeForamt/>` please refer to [MSDN DateTime Format](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx). The complete config  options example is here:

```xml
<labeller type="datetimeLabeller">	   
  <major>1</major>
  <minor>4</minor>
  <build>1234</build>
  <!- Optional, will overwrite generated value->
  <datetimeFormat>MMdd</datetimeFormat>
  <!- The .NET format for a DateTime type->
  <prefix>UAT-</prefix>
  <!- Optional->
</labeller>
```