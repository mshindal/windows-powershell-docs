---
external help file: MSFT_NetTCPConnection.cdxml-help.xml
Module Name: NetTCPIP
online version: 
schema: 2.0.0
title: Get-NetTCPConnection
description: 
keywords: powershell, cmdlet
author: brianlic
manager: jasgro
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: FDF635B0-3F62-48AE-BDE6-1DAC120DD52D
---

# Get-NetTCPConnection

## SYNOPSIS
Gets TCP connections.

## SYNTAX

```
Get-NetTCPConnection [[-LocalAddress] <String[]>] [[-LocalPort] <UInt16[]>] [-RemoteAddress <String[]>]
 [-RemotePort <UInt16[]>] [-State <State[]>] [-AppliedSetting <AppliedSetting[]>] [-OwningProcess <UInt32[]>]
 [-CreationTime <DateTime[]>] [-OffloadState <OffloadState[]>] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Get-NetTCPConnection** cmdlet gets current TCP connections.
Use this cmdlet to view TCP connection properties such as local or remote IP address, local or remote port, and connection state.

## EXAMPLES

### Example 1: Get all connections
```
PS C:\>Get-NetTCPConnection
```

This command gets all current TCP connections.

### Example 2: Get established connections
```
PS C:\>Get-NetTCPConnection -State Established
```

This command gets all TCP connections that have an Established state.

### Example 3: Get Internet TCP connections
```
PS C:\>Get-NetTCPConnection -AppliedSetting Internet
```

This command gets all TCP connections that use a TCP applied setting of Internet.

## PARAMETERS

### -AppliedSetting
Specifies an array of values of applied settings.
The cmdlet gets connections that match the settings that you specify.
The acceptable values for this parameter are:

- Internet
- Datacenter
- Compat
- Custom

```yaml
Type: AppliedSetting[]
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, Datacenter, Compat, InternetCustom, DatacenterCustom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
ps_cimcommon_asjob

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreationTime
{{Fill CreationTime Description}}

```yaml
Type: DateTime[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalAddress
Specifies an array of local IP addresses.
The cmdlet gets connections for the addresses that you specify.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: IPAddress

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalPort
Specifies an array of local ports.
The cmdlet gets connections for the ports that you specify.

```yaml
Type: UInt16[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OffloadState
{{Fill OffloadState Description}}

```yaml
Type: OffloadState[]
Parameter Sets: (All)
Aliases: 
Accepted values: InHost, Offloading, Offloaded, Uploading

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwningProcess
{{Fill OwningProcess Description}}

```yaml
Type: UInt32[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteAddress
Specifies an array of remote IP addresses.
The cmdlet gets connections for the addresses that you specify.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemotePort
Specifies an array of remote ports.
The cmdlet gets connections for the ports that you specify.

```yaml
Type: UInt16[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
Specifies an array of TCP states.
The cmdlet gets connections that match the states that you specify.
The acceptable values for this parameter are:

- Closed
- CloseWait
- Closing
- DeleteTCB
- Established
- FinWait1
- FinWait2
- LastAck
- Listen
- SynReceived
- SynSent
- TimeWait

```yaml
Type: State[]
Parameter Sets: (All)
Aliases: 
Accepted values: Closed, Listen, SynSent, SynReceived, Established, FinWait1, FinWait2, CloseWait, Closing, LastAck, TimeWait, DeleteTCB, Bound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShellŪ calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Management.Infrastructure.CimInstance#root\StandardCimv2\MSFT_NetTCPConnection
The `Microsoft.Management.Infrastructure.CimInstance` object is a wrapper class that displays Windows Management Instrumentation (WMI) objects.
The path after the pound sign (`#`) provides the namespace and class name for the underlying WMI object.

## NOTES

## RELATED LINKS


