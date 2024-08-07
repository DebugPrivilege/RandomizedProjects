# Summary

This section provides a mapping of the majority of the ActionTypes from Microsoft Defender for Endpoint (MDE) to the corresponding ETW Providers. The goal of this document is to assist other EDR researchers and developers in understanding how MDE uses ETW Providers to collect data for threat hunting.

There are lots of different ActionTypes, so this for sure not the full list. However, this list may be updated in the near future. 

# ActionTypes

| ActionType | Description | ETW Provider | Event ID |
|------------|-------------|--------------|----------|
| **`MemoryRemoteProtect`** | A process has modified the protection mask for a memory region used by another process. | Microsoft-Windows-ThreatIntelligence | 22 |
| **`DeviceBootAttestationInfo`** | System Guard generated a boot-time attestation report. | 2a3bf1b9-d828-4ccf-bd0a-73fb26ea02a4 | 1 |
| **`DriverLoad`** | A driver was loaded. | Microsoft-Windows-SEC | 24 |
| **`NtAllocateVirtualMemoryRemoteApiCall`** | Virtual Memory was allocated for a remote process | Microsoft-Windows-ThreatIntelligence | 1 |
| **`AccountCheckedForBlankPassword`** | An account was queried for a blank password. | Microsoft-Windows-Security-Auditing | 4797 |
| **`SecurityGroupCreated`** | An security group was created. | Microsoft-Windows-Security-Auditing | 4731 |
| **`ServiceInstalled`** | A service was installed. | Microsoft-Windows-Security-Auditing | 4697 |
| **`NetworkShareObjectAccessChecked`** | An attempt was made to access file or folder on a network share. | Microsoft-Windows-Security-Auditing | 5145 |
| **`NetworkShareObjectDeleted`** | A file or folder hosted on a network share was deleted. | Microsoft-Windows-Security-Auditing | 5144 |
| **`NetworkShareObjectModified`** | A file or folder hosted on a network share was modified. | Microsoft-Windows-Security-Auditing | 5143 |
| **`NetworkShareObjectAdded`** | A file or folder was shared on a network share. | Microsoft-Windows-Security-Auditing | 5142 |
| **`DirectoryServiceObjectCreated`** | An object was added to Active Directory. | Microsoft-Windows-Security-Auditing | 5137 |
| **`DirectoryServiceObjectModified`** | An object in Active Directory was modified. | Microsoft-Windows-Security-Auditing | 5136 |
| **`AntivirusEmergencyUpdatesInstalled`** | Emergency security intelligence updates for Windows Defender Antivirus were applied | Microsoft-Windows-Windows Defender | 2010 |
| **`AntivirusDefinitionsUpdateFailed`** | Security intelligence updates for Windows Defender Antivirus were not applied | Microsoft-Windows-Windows Defender | 2001 |
| **`AntivirusDefinitionsUpdated`** | Security intelligence updates for Windows Defender Antivirus were applied successfully. | Microsoft-Windows-Windows Defender | 2000 |
| **`UserAccountModified`** | A user account was changed. | Microsoft-Windows-Security-Auditing | 4738 |
| **`SecurityGroupDeleted`** | A security-enabled local group was deleted. | Microsoft-Windows-Security-Auditing | 4734 |
| **`UserAccountRemovedFromLocalGroup`** | A member was removed from a security-enabled local group. | Microsoft-Windows-Security-Auditing | 4733 |
| **`UserAccountAddedToLocalGroup`** | A member was added to a security-enabled local group. | Microsoft-Windows-Security-Auditing | 4732 |
| **`UserAccountDeleted`** | A user account was deleted. | Microsoft-Windows-Security-Auditing | 4726 |
| **`AntivirusError`** | Windows Defender Antivirus encountered an error while taking action on malware | Microsoft-Windows-Windows Defender | 1119 |
| **`AntivirusMalwareActionFailed`** | Windows Defender Antivirus attempted to take action on malware but it failed | Microsoft-Windows-Windows Defender | 1118 |
| **`AntivirusMalwareBlocked`** | Windows Defender Antivirus blocked files or activity involving malware potentially unwanted applications or suspicious behavior. | Microsoft-Windows-Windows Defender | 1117 |
| **`AntivirusDetection`** | Windows Defender Antivirus detected a threat. | Microsoft-Windows-Windows Defender | 1116 |
| **`SecurityLogCleared`** | The security log was cleared. | Microsoft-Windows-Security-Auditing | 1102 |
| **`PnpDeviceConnected`** | A plug and play (PnP) device was attached. | Microsoft-Windows-Security-Auditing | 6416 |
| **`PnpDeviceAllowed`** | Device control allowed a trusted plug and play (PnP) device.| Microsoft-Windows-Kernel-PnP-Events | 400 |
| **`PnpDeviceBlocked`** | Device control blocked an untrusted plug and play (PnP) device. | Microsoft-Windows-Kernel-PnP-Events | 402 |
| **`ScreenshotTaken`** | A screenshot was taken. | Microsoft-Windows-Win32k | 1 |
| **`ScheduledTaskCreated`** | 	A scheduled task was created. | Microsoft-Windows-Security-Auditing | 4698 |
| **`ScheduledTaskDeleted`** | A scheduled task was deleted. | Microsoft-Windows-Security-Auditing | 4699 |
| **`ScheduledTaskEnabled`** | A scheduled task was turned on. | Microsoft-Windows-Security-Auditing | 4700 |
| **`ScheduledTaskDisabled`** | A scheduled task was turned off. | Microsoft-Windows-Security-Auditing | 4701 |
| **`OpenProcessApiCall`** | The OpenProcess function was called indicating an attempt to open a handle to a local process and potentially manipulate that process. | Microsoft-Windows-SEC | 19 |
| **`CreateRemoteThreadApiCall`** | A thread that runs in the virtual address space of another process was created. | Microsoft-Windows-SEC | 18 |
| **`AppControlExecutableAudited`** | Application control detected the use of an untrusted executable. | Microsoft-Windows-AppLocker | 8003 |
| **`AppControlExecutableBlocked`** | Application control blocked the use of an untrusted executable. | Microsoft-Windows-AppLocker | 8004 |
| **`AppControlScriptAudited`** | Application control detected the use of an untrusted script. | Microsoft-Windows-AppLocker | 8006 |
| **`AppControlScriptBlocked`** | Application control blocked the use of an untrusted script. | Microsoft-Windows-AppLocker | 8007 |
| **`AppControlPackagedAppAudited`** | Application control detected the use of an untrusted packaged app. | Microsoft-Windows-AppLocker | 8021 |
| **`AppControlPackagedAppBlocked`** | Application control blocked the installation of an untrusted packaged app. | Microsoft-Windows-AppLocker | 8022 |
| **`AppControlScriptAudited`** | Application control detected the use of an untrusted script. | Microsoft-Windows-AppLocker | 8006 |
| **`AppControlAppInstallationAudited`** | Application control detected the installation of an untrusted app. | Microsoft-Windows-AppLocker | 8024 |
| **`AppControlAppInstallationBlocked`** | Application control blocked the installation of an untrusted app. | Microsoft-Windows-AppLocker | 8025 |
| **`AppControlCodeIntegrityPolicyAudited`** | Application control detected a code integrity policy violation. | Microsoft-Windows-AppLocker | 3076 |
| **`AppControlCodeIntegrityPolicyBlocked`** | Application control blocked a code integrity policy violation | Microsoft-Windows-AppLocker | 3077 |
| **`PowerShellCommand`** | A PowerShell alias function filter cmdlet external script application script workflow or configuration was executed from a PowerShell host process. | {a0c1853b-5c40-4b15-8766-3cf1c58f985a} | 7937 |
| **`RemoteWmiOperation`** | A Windows Management Instrumentation (WMI) operation was initiated from a remote device. | Microsoft-Windows-WMI-Activity | 11 |
| **`ProcessCreatedUsingWmiQuery`** | A process was created using Windows Management Instrumentation (WMI). | Microsoft-Windows-WMI-Activity | 22/23 |
| **`NtAllocateVirtualMemoryApiCall`** | Memory was allocated for a process. | Microsoft-Windows-ThreatIntelligence | 6 |
| **`NtProtectVirtualMemoryApiCall`** | The protection attributes for allocated memory was modified. | Microsoft-Windows-ThreatIntelligence | 7 |
| **`SetThreadContextRemoteApiCall`** | The context of a thread was set from a user-mode process. | Microsoft-Windows-ThreatIntelligence | 5 |
| **`QueueUserApcRemoteApiCall`** | An asynchronous procedure call (APC) was scheduled to execute in a user-mode thread. | Microsoft-Windows-ThreatIntelligence | 4 |
| **`NtMapViewOfSectionRemoteApiCall`** | A section of a process's memory was mapped by calling the function NtMapViewOfSection. | Microsoft-Windows-ThreatIntelligence | 3 |
| **`ProcessPrimaryTokenModified`** | A process's primary token was modified. | Microsoft-Windows-SEC | 25 |
| **`UserAccountCreated`** | A local SAM account or a domain account was created. | Microsoft-Windows-Security-Auditing | 4720 |
| **`BrowserLaunchedToOpenUrl`** | A web browser opened a URL that originated as a link in another application. | {30336ed4-e327-447c-9de0-51b652c86108} | 19501 |
| **`WmiRemoteQuery`** | A remote WMI query was performed. | Microsoft-Windows-WMI-Activity | 1 |
| **`DnsQueryRequest`** | A DNS query was performed. | Microsoft-Windows-DNS-Client | 3010 |
| **`WmiBindEventFilterToConsumer`** | A filter for WMI events was bound to a consumer. | Microsoft-Windows-WMI-Activity | 5861 |
| **`ShellLinkCreateFileEvent`** | A specially crafted link file (.lnk) was generated. The link file contains unusual attributes that might launch malicious code along with a legitimate file or application. | N/A | N/A |
| **`FileTimestampModificationEvent`** | File timestamp information was modified. | Microsoft-Windows-SEC | 35 |
| **`ExploitGuardAcgAudited`** | Arbitrary code guard (ACG) in exploit protection detected an attempt to modify code page permissions or create unsigned code pages. | Microsoft-Windows-Security-Mitigations | 1 |
| **`ExploitGuardAcgEnforced`** | Arbitrary code guard (ACG) blocked an attempt to modify code page permissions or create unsigned code pages. | Microsoft-Windows-Security-Mitigations | 2 |
| **`ExploitGuardChildProcessAudited`** | Exploit protection detected the creation of a child process. | Microsoft-Windows-Security-Mitigations | 3 |
| **`ExploitGuardChildProcessBlocked`** | Exploit protection blocked the creation of a child process. | Microsoft-Windows-Security-Mitigations | 4 |
| **`ExploitGuardLowIntegrityImageAudited`** | Exploit protection detected the launch of a process from a low-integrity file. | Microsoft-Windows-Security-Mitigations | 5 |
| **`ExploitGuardLowIntegrityImageBlocked`** | Exploit protection blocked the launch of a process from a low-integrity file. | Microsoft-Windows-Security-Mitigations | 6 |
| **`ExploitGuardSharedBinaryAudited`** | Exploit protection detected the launch of a process from a remote shared file. | Microsoft-Windows-Security-Mitigations | 7 |
| **`ExploitGuardSharedBinaryBlocked`** | Exploit protection blocked the launch of a process from a file in a remote device. | Microsoft-Windows-Security-Mitigations | 8 |
| **`ExploitGuardWin32SystemCallAudited`** | Exploit protection detected a call to the Windows system API. | Microsoft-Windows-Security-Mitigations | 9 |
| **`ExploitGuardWin32SystemCallBlocked`** | Exploit protection blocked a call to the Windows system API. | Microsoft-Windows-Security-Mitigations | 10 |
| **`ExploitGuardNonMicrosoftSignedAudited`** | Exploit protection detected the launch of a process from an image file that is not signed by Microsoft. | Microsoft-Windows-Security-Mitigations | 11 |
| **`ExploitGuardNonMicrosoftSignedBlocked`** | Exploit protection blocked the launch of a process from an image file that is not signed by Microsoft. | Microsoft-Windows-Security-Mitigations | 12 |
| **`ExploitGuardEafViolationAudited`** | Export address filtering (EAF) in exploit protection detected possible exploitation activity. | Microsoft-Windows-Security-Mitigations | 13 |
| **`ExploitGuardEafViolationBlocked`** | Export address filtering (EAF) in exploit protection blocked possible exploitation activity. | Microsoft-Windows-Security-Mitigations | 14 |
| **`ExploitGuardRopExploitAudited`** | Exploit protection detected possible return-object programming (ROP) exploitation. | Microsoft-Windows-Security-Mitigations | 19 |
| **`ExploitGuardRopExploitBlocked`** | Exploit protection blocked possible return-object programming (ROP) exploitation. | Microsoft-Windows-Security-Mitigations | 20 |
| **`FirewallInboundConnectionToAppBlocked`** | The firewall blocked an inbound connection to an app. | Microsoft-Windows-Security-Auditing | 5031 |
| **`FirewallServiceStopped`** | The firewall service was stopped. | Microsoft-Windows-Security-Auditing | 5025 |
| **`AppControlCodeIntegrityDriverRevoked`** | Application control found a driver with a revoked certificate | Microsoft-Windows-CodeIntegrity | 3023 |
| **`AppControlCodeIntegrityImageRevoked`** | Application control found an executable file with a revoked certificate. | Microsoft-Windows-CodeIntegrity | 3036 |
| **`AppGuardCreateContainer`** | Application guard initiated an isolated container. | Microsoft.Windows.HVSI.ContainerService | ? |
| **`AppGuardSuspendContainer`** | Application guard suspended an isolated container. | Microsoft.Windows.HVSI.ContainerService | ? |
| **`AppGuardResumeContainer`** | Application guard resumed an isolated container from a suspended state. | Microsoft.Windows.HVSI.ContainerService | ? |
| **`AppGuardStopContainer`** | Application guard stopped an isolated container. | Microsoft.Windows.HyperV.Compute | ? |
| **`AppGuardLaunchedWithUrl`** | The opening of an untrusted URL has initiated an application guard container. | Microsoft.Windows.HVSI.Manager | ? |
| **`SmartScreenAppWarning`** | SmartScreen warned about running a downloaded application that is untrusted or malicious. | Microsoft-Windows-SmartScreen | 1000 |
| **`SmartScreenUrlWarning`** | SmartScreen warned about opening a low-reputation URL that might be hosting malware or is a phishing site. | Microsoft-Windows-SmartScreen | 1001 |
| **`SmartScreenUserOverride`** | A user has overridden a SmartScreen warning and continued to open an untrusted app or a low-reputation URL. | Microsoft-Windows-SmartScreen | 1002 |
| **`NetworkProtectionUserBypassEvent`** | A user has bypassed network protection and accessed a blocked IP address, domain, or URL. | Microsoft-Antimalware-Service | 55 |
| **`AntivirusScanCompleted`** | A Windows Defender Antivirus scan completed successfully. | Microsoft-Windows-Windows Defender | 1001 |
| **`AntivirusScanCancelled`** | A Windows Defender Antivirus scan was cancelled | Microsoft-Windows-Windows Defender | 1002 |
| **`AntivirusScanFailed`** | A Windows Defender Antivirus scan did not complete successfully. | Microsoft-Windows-Windows Defender | 1005 |
| **`FirewallOutboundConnectionBlocked`** | A firewall or another application blocked an outbound connection using the Windows Filtering Platform. | Microsoft-Windows-Security-Auditing | 5157 |
| **`FirewallInboundConnectionBlocked`** | A firewall or another application blocked an inbound connection using the Windows Filtering Platform. | Microsoft-Windows-Security-Auditing | 5157 |
| **`SmartScreenExploitWarning`** | SmartScreen warned about opening a web page that contains an exploit. | Microsoft-Windows-IE-SmartScreen | 1100 |
| **`WriteToLsassProcessMemory`** | The WriteProcessMemory function was called indicating that a process has written data into memory for another process. | Microsoft-Windows-ThreatIntelligence | 14 |
| **`ReadProcessMemoryApiCall`** | The ReadProcessMemory function was called indicating that a process read data from the process memory of another process. | Microsoft-Windows-ThreatIntelligence | 13 |
| **`AmsiScriptContent`** | Script content was identified by the Antimalware Scan Interface (AMSI). | Microsoft-Antimalware-Scan-Interface | 1101 |
| **`AmsiScriptContentScan`** | Script content was scanned by the Antimalware Scan Interface (AMSI). | Microsoft-Antimalware-Scan-Interface | 1101 |
| **`GetAsyncKeyStateApiCall`** | The GetAsyncKeyState function was called. This function can be used to obtain the states of input keys and buttons. | Microsoft-Windows-Win32k | 1003 |
| **`LdapSearch`** | An LDAP search was performed. | Microsoft-Windows-Ldap-Client | 30 |
| **`GetClipboardData`** | The GetClipboardData function was called. This function can be used obtain the contents of the system clipboard. | Microsoft.Windows.OLE.Clipboard | ? |
| **`PasswordChangeAttempt`** | An attempt to change a user password was made. | Microsoft-Windows-Security-Auditing | 4724 |
| **`LogonRightsSettingEnabled`** | Interactive logon rights on the machine were granted to a user. | Microsoft-Windows-Security-Auditing | 4717 |
| **`PrintJobBlocked`** | Device control prevented an untrusted printer from printing. | Microsoft-Windows-PrintService | 871 |
| **`SafeDocFileScan`** | A document was sent to the cloud for analysis while in protected view. | Microsoft.Office.Security | ? |
| **`UntrustedWifiConnection`** | A connection was established to an open Wi-Fi access point that is set to connect automatically. | Microsoft.Windows.Sense.CollectionEtw | ? |
| **`ControlFlowGuardViolation`** | Control Flow Guard terminated an application after detecting an invalid function call. | Microsoft-Windows-WER-Diag | 5 |
| **`RemoteDesktopConnection`** | A Remote Desktop connection was established. | Microsoft-Windows-RemoteDesktopServices-RdpCoreTS | 131 |
| **`DnsQueryResponse`** | A response to a DNS query was sent. | Microsoft-Windows-DNS-Client | 3020 |
| **`CredentialsBackup`** | The backup feature in Credential Manager was initiated | Microsoft-Windows-Security-Auditing | 5376 |
| **`ScheduledTaskUpdated`** | A scheduled task was updated. | Microsoft-Windows-Security-Auditing | 4702 |
| **`RemovableStoragePolicyTriggered`** | Device control detected an attempted read/write/execute event from a removable storage device. | Microsoft-Antimalware-RTP | 25 |
| **`BluetoothPolicyTriggered`** | A Bluetooth service activity was allowed or blocked by a device control policy. | Microsoft-Windows-Bluetooth-Policy | 7 |
| **`AppControlCodeIntegritySigningInformation`** | Application control signing information was generated. | Microsoft-Windows-CodeIntegrity | 3089 |
| **`AppControlCodeIntegrityPolicyLoaded`** | An application control code integrity policy was loaded. | Microsoft-Windows-CodeIntegrity | 3099 |
| **`AppControlCIScriptAudited`** | A script or MSI file generated by Windows LockDown Policy was audited. | Microsoft-Windows-AppLocker | 8028 |
| **`AppControlCIScriptBlocked`** | A script or MSI file generated by Windows LockDown Policy was blocked. | Microsoft-Windows-AppLocker | 8029 |
| **`AppControlCodeIntegrityOriginAllowed`** | Application control allowed a file due to its good reputation (ISG) or installation source (managed installer). | Microsoft-Windows-CodeIntegrity | 3090 |
| **`AppControlCodeIntegrityOriginAudited`** | Application control would have blocked a file due to its bad reputation (ISG) or installation source (managed installer) if the policy was enforced. | Microsoft-Windows-CodeIntegrity | 3091 |
| **`AppControlCodeIntegrityOriginBlocked`** | Application control blocked a file due to its bad reputation (ISG) or installation source (managed installer). | Microsoft-Windows-CodeIntegrity | 3092 |
| **`AppControlPolicyApplied`** | An application control policy was applied to the device. | Microsoft-Windows-AppLocker | 8001 |
| **`NamedPipeEvent`** | A named pipe was created or opened. | Microsoft-Windows-SEC | 17 |
| **`DpapiAccessed`** | Decription of saved sensitive data encrypted using DPAPI. | Microsoft-Windows-Crypto-DPAPI-Events | 16385 |
| **`RemovableStorageFileEvent`** | Removable storage file activity matched a device control removable storage access control policy. | Microsoft-Antimalware-RTP | 26 |
| **`AuditPolicyModification`** | Changes in the Windows audit policy (which feed events to the event log). | Microsoft-Windows-Security-Auditing | 4719 |
| **`AntivirusTroubleshootModeEvent`** | The troubleshooting mode in Microsoft Defender Antivirus was used. | Microsoft-Antimalware-Service | 60 |
| **`TamperingAttempt`** | An attempt to change Microsoft Defender XDR settings was made. | Microsoft-Antimalware-Service| 67 |
| **`NetworkShareObjectAccessed`** | An network share object was accessed | Microsoft-Windows-Security-Auditing| 5140 |
| **`ClrUnbackedModuleLoaded`** | An CLR Module was loaded reflectively | Microsoft-Windows-DotNETRuntime| 152 |




