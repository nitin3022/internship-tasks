Task 1 - Open Port Scan and Risk Assessment

Scanned Devices

Device: 172.20.10.1 

Port            Service                       Risk Level                          Recommendation 

 21              FTP                            High                        Disable FTP/ Use SFTP if needed

 53              DNS                            Medium                       Monitor for unusual traffic. 

49152           Unknown                         Medium                       Identify and audit the service. 

62078         iPhone Sync                        Low                         Acceptable for personal Apple devices. 

Device: 172.20.10.2 (Windows Host)

Port         Service                           Risk Level                           Recommendation 

135           msrpc                              Medium                            Block externally, used by RPC exploits. 

139          NetBIOS                             High                              Disable if not using file sharing. 

445           SMB                                High                              Disable SMBv1, block from external IPs. 

808        ccproxy-http                          Medium                            Check if proxy is intentionally enabled. 

2869       ICSLAP (UPnP)                         Medium                            Disable UPnP on router if unused.  

Conclusion

FTP, NetBIOS, and SMB are serious exposure risks on a local network.

Where services are not in use, they should be disabled or firewalled.

All systems should be patched and monitored to prevent exploitation.
