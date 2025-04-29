# Network-Attack-Simulation
SYN flood analysis and DoS attack simulation with TCP handshake and packet log investigation.


This project analyzes a network service interruption caused by a suspected SYN flood attack. Using captured TCP packet data and incident documentation, I investigate the root cause and explain how SYN flooding overwhelms a web server’s resources.



Project Files
- **Incident_Report.pdf**  
  Identifies the nature of the attack, explains the TCP handshake, and how the attack disrupted service.

  TCP log screenshots that illustrate a large number of SYN packets targeting the same destination IP and port.


Attack Identified

Type:  
- Denial of Service (DoS)
- SYN Flood

Evidence:
- Repeated SYN packets in logs from `203.0.113.0` to `192.0.2.1`
- Lack of completed handshakes
- Gateway timeout errors in final HTTP responses


TCP Handshake Recap
1. **SYN:** Client requests connection  
2. **SYN-ACK:** Server acknowledges and reserves resources  
3. **ACK:** Client confirms and completes handshake  

> In this case, the attacker sends a flood of SYN packets **without completing the handshake**, exhausting the server's capacity to respond.


Tools / Concepts Used
- TCP analysis
- Log review
- DoS/SYN flood understanding
- Incident response documentation
- Gateway timeout troubleshooting

