# Project 2 — Wireshark Network Traffic Investigation

## Project Overview

This project is a hands-on network traffic investigation conducted in a controlled Windows security lab using Wireshark.

The investigation focused on identifying HTTP traffic, analyzing an HTTP request and its corresponding response, and documenting the findings from a SOC Analyst perspective.

## Investigation Objectives

- Analyze a captured network traffic file using Wireshark.
- Identify HTTP traffic.
- Identify an actual HTTP GET request.
- Analyze source and destination IP addresses.
- Examine HTTP request details.
- Identify and correlate the corresponding HTTP response.
- Analyze a partial-content file transfer.
- Document the evidence and findings.

## Tools Used

- Wireshark
- Windows
- PCAPNG network capture
- HTTP protocol analysis

## HTTP Request Finding

An HTTP GET request was identified from:

**Source:** `192.168.100.4`

**Destination:** `199.232.214.172`

**Protocol:** HTTP

**Destination Port:** `80`

**Method:** `GET`

**Host:** `b.c2r.ts.cdn.office.net`

**User-Agent:** `Microsoft-Delivery-Optimization/10.1`

**Request URI:**

`/pr/492359f6-3a01-4f97-b9c0-c6ddf67d60/Office/Data/16.0.20326.20158/stream.x64.x-none.dat`

The requested resource was an Office data file named:

`stream.x64.x-none.dat`

## HTTP Response Finding

The corresponding response was identified in Wireshark as:

**HTTP/1.1 206 Partial Content**

The response was linked to the original request:

**Request in frame:** `3541`

**Content-Length:** `1048576 bytes`

**Content-Type:** `application/octet-stream`

**Content-Range:** `bytes 1371537408-1372585983/2898193638`

The `206 Partial Content` response indicates that the server returned a portion of the requested file rather than the complete file in a single response.

## Key Finding

The HTTP GET request and the corresponding HTTP `206 Partial Content` response were successfully identified and correlated in Wireshark.

The traffic was associated with Microsoft's Office content-delivery infrastructure. The observed traffic was not automatically classified as malicious because the request, destination, hostname, User-Agent, and response provided context consistent with legitimate Office content delivery.

This investigation demonstrates the importance of analyzing network traffic and its context before determining whether activity is malicious.

## Evidence Collected

- Wireshark PCAPNG capture
- HTTP GET request evidence
- HTTP 206 Partial Content response evidence
- PowerShell evidence
- Sysmon evidence
- Investigation notes
- IOC review
- SOC incident report
- Investigation screenshots

## SOC Analyst Skills Demonstrated

- Wireshark packet analysis
- Network traffic filtering
- HTTP request analysis
- HTTP response analysis
- IP and port analysis
- Request/response correlation
- Network evidence collection
- Security investigation documentation
- Context-based traffic analysis

## Lessons Learned

This investigation demonstrated how a SOC Analyst can use Wireshark to move from a large packet capture to a specific network event and correlate an HTTP request with its server response.

It also reinforced that suspicious-looking network traffic should be investigated using multiple pieces of evidence before being classified as malicious.

## Project Structure

```text
Project 2
├── Capture
├── Evidence
├── Investigation
├── IOCs
├── Report
└── README.md
Project Status

Completed