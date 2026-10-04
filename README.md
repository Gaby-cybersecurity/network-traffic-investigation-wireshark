# Project 2 — Wireshark Network Traffic Investigation

## Project Overview

This project is a hands-on network traffic investigation conducted in a controlled Windows security lab using Wireshark.

The investigation focused on identifying and analyzing network communication within a captured PCAPNG file from a SOC Analyst perspective.

The analysis included identifying HTTP traffic, examining an HTTP GET request, analyzing source and destination hosts, correlating the request with its corresponding response, and reviewing a partial-content file transfer.

## Investigation Objectives

- Analyze a captured network traffic file using Wireshark
- Identify HTTP traffic within the capture
- Identify an actual HTTP GET request
- Analyze source and destination IP addresses
- Examine HTTP request details
- Correlate the HTTP request with its corresponding response
- Analyze a partial-content file transfer
- Review indicators of interest identified during the investigation
- Document investigation evidence and findings
- Practice network traffic analysis techniques used in SOC investigations

## Environment

- Windows security laboratory environment
- Wireshark
- PCAPNG network capture
- Controlled test network traffic

## Investigation Methodology

The investigation followed a structured network traffic analysis process:

1. Review the captured PCAPNG file in Wireshark
2. Identify relevant network protocols
3. Filter and isolate HTTP traffic
4. Examine source and destination hosts
5. Identify an HTTP GET request
6. Analyze the request details
7. Locate and correlate the corresponding HTTP response
8. Examine the transferred content and response behavior
9. Review indicators of interest
10. Document the evidence, timeline, observations, and findings

## Network Traffic Analysis

### HTTP Traffic Identification

The captured traffic was reviewed using Wireshark display filters to identify HTTP communication.

HTTP traffic was selected for deeper investigation because it provided visible request and response information that could be examined at the packet level.

### HTTP GET Request

An HTTP GET request was identified within the captured traffic.

The request was examined to determine:

- Source host
- Destination host
- HTTP method
- Requested resource
- Protocol information
- Associated packet details

The request was then correlated with the traffic that followed it.

### HTTP Response Analysis

The corresponding HTTP response was identified and examined.

The response was correlated with the original HTTP GET request to establish the communication sequence between the client and server.

This provided evidence of the relationship between the request and the resulting server response.

### Partial-Content Transfer

A partial-content response was identified during the investigation.

The traffic was examined to understand how the requested content was transferred and how the response related to the original HTTP request.

This was documented as part of the network communication evidence.

## Source and Destination Analysis

Source and destination information was reviewed throughout the investigation to understand the hosts involved in the observed communication.

The analysis considered:

- Source IP address
- Destination IP address
- Client/server relationship
- Communication direction
- Associated protocols and ports

This helped establish the network flow between the systems involved in the captured traffic.

## IOC Review

Indicators of interest identified during the investigation were documented separately in the repository.

The IOC review was used to organize potentially relevant network indicators and support further investigation.

The indicators were assessed within the context of the controlled laboratory environment rather than automatically classified as malicious.

## Evidence Collected

The investigation produced several forms of supporting evidence:

- PCAPNG network capture
- Wireshark packet analysis
- HTTP request evidence
- HTTP response evidence
- Network traffic observations
- Investigation notes
- Investigation timeline
- IOC review
- SOC incident report

## Investigation Documentation

The repository contains supporting investigation documentation:

- `Investigation-Notes.txt` — investigation observations and analysis
- `Investigation-Timeline.txt` — chronological investigation events
- `IOC-Review.txt` — indicators reviewed during the investigation
- `IOC-Summary.txt` — summary of relevant indicators
- `SOC-Incident-Report.txt` — documented SOC investigation report

## Tools Used

- Wireshark
- Windows
- PCAPNG
- Network traffic analysis
- Wireshark display filters
- Packet inspection techniques

## Skills Demonstrated

- Network traffic analysis
- Packet analysis
- Wireshark filtering
- HTTP analysis
- Protocol identification
- Source and destination IP analysis
- Request and response correlation
- Network evidence collection
- IOC review
- Investigation documentation
- SOC Analyst investigation methodology

## Key Findings

The investigation successfully identified HTTP communication within the captured network traffic.

An HTTP GET request was identified and analyzed, including the participating source and destination hosts.

The corresponding HTTP response was also identified and correlated with the request.

A partial-content transfer was observed and documented as part of the investigation.

The captured traffic and supporting documentation provide evidence that can be reviewed as part of a structured SOC network investigation.

Because the traffic was generated and analyzed within a controlled security laboratory, observations were interpreted within the context of the test environment.

## Conclusion

This project demonstrates practical network traffic investigation using Wireshark in a controlled security lab.

The investigation covered packet inspection, HTTP analysis, source and destination analysis, request/response correlation, content-transfer analysis, IOC review, and evidence documentation.

The project strengthens foundational SOC Analyst skills in network visibility, packet analysis, investigation methodology, evidence handling, and security documentation.

## Project Status

**Completed — Investigation and Documentation**

The network traffic investigation, supporting analysis, IOC review, timeline, and investigation documentation have been completed.

Future improvements may include adding additional screenshots and expanding the analysis with further network security scenarios.
